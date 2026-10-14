---
name: canvas-animation
description: Generates high-performance 2D canvas animations, particle effects, and smooth interpolation routines for web applications.
---

# Canvas Animation Instructions

When writing animations for this project:
- **Particle Systems:** Implement lightweight particle arrays with properties for position, velocity, lifespan, and fading alpha values.
- **Easing & Interpolation:** Use smooth mathematical transition functions (like linear interpolation `lerp` or ease-out formulas) for UI elements or camera tracking.
- **Performance:** Avoid memory allocation inside the render loop (e.g., reuse objects instead of creating new instances inside `requestAnimationFrame`) to prevent garbage collection stutter.
