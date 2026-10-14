---
name: html5-gamedev
description: Writes pure HTML5 canvas games using vanilla JavaScript and CSS without external frameworks. Focuses on robust game loops, delta time management, input handling, and collision detection.
---

# HTML5 Game Development Instructions

When writing game code for this project:
- **Core Loop:** Always use `requestAnimationFrame` with a delta time (`dt`) calculation measured in seconds to ensure frame-rate independent movement.
- **Architecture:** Keep code modular. Separate input handlers, game state updates, and canvas rendering functions.
- **Canvas Rendering:** Clear the canvas cleanly on every frame using `ctx.clearRect(0, 0, canvas.width, canvas.height)` before drawing entities.
- **Input Management:** Use a persistent state object tracking `keydown` and `keyup` listeners to support smooth multi-key movement (e.g., diagonal movement).
