# 🎉 canvas-confetti (custom fork)

This fork of `canvas-confetti` introduces three additional options to enhance visual effects, especially for **flat emoji particles** (`flat: true`).

## 🔧 New Options

### `rotate` (boolean, default: `false`)
Allows flat confetti (`flat: true`) to **rotate in 2D space**, giving emoji shapes a more natural animated look.

- Has no effect unless `flat: true` is set.
- Disabled by default.

```js
rotate: true
```

---

### `rotationSpeed` (number, optional)
Manually controls how **fast flat confetti rotate** (in radians per frame).

- If not provided, a random speed is chosen by default.
- Only applies when `rotate: true` is set.

```js
rotationSpeed: 0.05  // smaller = slower rotation
```

---

### `fadeStart` (number between 0 and 1, default: `0`)
Controls **when the particle starts to fade out** (opacity drops toward 0).

- `0` = fade starts from the beginning (default behavior)
- `1` = no fading, fully opaque for the full lifespan
- `0.8` = fade starts at 80% of the particle's lifespan

```js
fadeStart: 0.8
```

---

## ✅ Example

```js
confetti({
  shapes: [myEmojiShape],
  flat: true,
  rotate: true,
  rotationSpeed: 0.03,
  fadeStart: 0.9,
  particleCount: 50,
});
```

---

These additions are fully backward-compatible with the original `canvas-confetti`.
