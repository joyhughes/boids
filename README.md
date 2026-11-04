# Boids

Craig Reynolds' flocking model (1987) in the browser. Each boid steers by three local rules: separation, alignment and cohesion. It only sees neighbours within a radius and inside a field-of-view cone.

Live: https://joyhughes.github.io/boids/

Choose a 2D world (the window) or 3D (a box with an orbiting camera); `#3d` in the URL opens 3D directly. Plain JS in a single `index.html`, with no build step. Mouse modes: predator, attract, obstacle, and inspect (shows a boid's view and its steering forces). Keys: Space pause, S step, R scatter, H hide panel.
