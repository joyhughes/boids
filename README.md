# Boids

Craig Reynolds' flocking model (1987) in the browser. Each boid steers by three local rules: separation, alignment and cohesion. It only sees neighbours within a radius and inside a field-of-view cone.

Live: https://joyhughes.github.io/boids/

Choose a 2D world (the window) or 3D (a box with an orbiting camera); `#3d` in the URL opens 3D directly. Plain JS in a single `index.html`, with no build step. The controls sit beside the view, or below it on narrow screens. Hide them with H for a full-size view.

- **Predators:** a few hunters that flock together and catch boids. Eaten boids are replaced so the population stays constant. Boids and predators can co-evolve: boids inherit separation, alignment, cohesion and flee weights from long-lived survivors, and every 30 s the predator with the lowest kill rate is replaced by a mutant of the best. All of these weights share a fixed steering budget, so evolution can only reallocate agility, not increase it. Boids are solid bodies, and the confusion effect stops giving extra protection beyond 20 neighbours.
- **Sheepdogs:** herding after Strömbom et al. (2014). The dogs collect stragglers and drive the flock into a corner pen. With learning on, each round tests a small change to their herding parameters and keeps it if the flock is penned faster.
- **Drone show:** the boids fly into lit formations. Shapes: a Chinese dragon, a waving Canadian flag, a face, butterfly, Saturn, jack-o'-lantern, Diwali lamp, menorah, Christmas tree, snowflake, crescent and star, DNA double helix, heart, trefoil knot, fireworks, galaxy, your own text, or an uploaded image. In 3D, the dragon, face, pumpkin (with its face carved in), heart, butterfly, menorah, lamp and crescent are real 3D models. Each is built from blended spheres, ellipsoids, tubes and extruded outlines, with drones spread evenly over the surface. Text, the snowflake and images become extruded or relief solids, and the flag is a rippling sheet.
- **Record video:** captures the simulation canvas to MP4/WebM. Mouse modes: predator, attract, obstacle, and inspect (shows a boid's view and its steering forces). Keys: Space pause, S step, R scatter, H hide panel.
