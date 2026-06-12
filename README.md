# Van Langen Labs Website

Single-page landing site hosted on GitHub Pages, featuring an animated WebGL2 logo and a static fallback for browsers without WebGL2 support.

## Technologies Used

- HTML5: semantic structure for content, links, and fallback image.
- CSS3: responsive layout using `clamp()`, media queries, glass/neon styling, and subtle hover/focus states.
- Vanilla JavaScript (ES6+): rendering setup, texture loading, and animation loop.
- WebGL2 + GLSL ES 3.00 shaders: custom vertex and fragment shaders for refraction, caustics, glow, and sparkle effects.
- Canvas API: full-screen render target for shader output.
- Progressive enhancement: automatic fallback to a static logo on `file://` or when WebGL2 is unavailable.
- External links with security best practices: `target="_blank"` combined with `rel="noopener noreferrer"`.

## Key Implementation Details

- Shader-driven visual effects are implemented in `docs/logo.js`.
- Structure and page content are in `docs/index.html`.
- Styling is in `docs/styles.css`.
- For texture loading, same-origin is used by default, and CORS mode is only enabled for truly cross-origin URLs.

## Run Locally

Use a local HTTP server (required for correct texture/image loading in WebGL):

- Via VS Code Task: run `Serve docs (py)` or `Serve docs (python)`.
- Via F5: use `Launch docs site (py)` or `Launch docs site (python)`.

The site will be available at: `http://localhost:8000`

## Project Structure

- `docs/index.html`: page structure
- `docs/styles.css`: layout and visual styling
- `docs/logo.js`: WebGL2 rendering and animation
- `.vscode/tasks.json`: tasks for starting the local server
- `.vscode/launch.json`: F5 launch profiles