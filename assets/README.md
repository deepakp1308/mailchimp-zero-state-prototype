# Maya avatar assets

This is where realistic avatar assets live. The widget tries them in order:

## Drop-in slots (the component auto-detects):

1. **`maya-avatar-realistic.mp4`** — looping idle video (silent, no audio). 2-3 second loop, 720p or higher, square aspect (1:1), centered head/bust.
2. **`maya-avatar-speaking.mp4`** — looping speaking video (mouth moving). Same format as above.
3. **`maya-avatar-realistic.webp`** — single high-quality portrait (square crop). Used when video isn't available; the component layers CSS-driven mouth/eye effects on top.
4. **`maya-avatar-realistic.jpg`** — final fallback. Same dimensions and crop.

## Recommended sources for production assets

- **Tavus / HeyGen / D-ID / Synthesia** — generate a real-time talking-head avatar with API; export idle + speaking loop clips.
- **Synthesia studio** — pre-render full speech videos per script.
- **Custom record** — film a real person (with model release) at 720p/1080p with neutral background, ~3s idle loop and ~6s speaking loop.

## Hooking up a real avatar SDK

The component exposes `window.MayaAvatar` with these methods:

```js
MayaAvatar.setState('idle' | 'speaking' | 'listening' | 'happy' | 'calm')
MayaAvatar.speak(text, voiceChunks)   // current path: browser TTS
MayaAvatar.connectSDK({ provider, apiKey, avatarId })  // future hook
```

To swap in a real-time avatar provider (Tavus / HeyGen / D-ID), implement
`MayaAvatar.connectSDK()` in `index.html` and have it replace the `<video>` /
SVG layers with the provider's `<iframe>` or WebRTC stream.
