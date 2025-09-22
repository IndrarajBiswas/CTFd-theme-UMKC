# CTFd Theme – UMKC

A custom theme for CTFd inspired by the University of Missouri–Kansas City colors. It is based on the official `core-beta` theme and keeps parity with the latest CTFd front-end stack (Bootstrap 5, Alpine.js, Vite) while introducing a neon blue/gold aesthetic, retro typography, and a hacker friendly UI treatment.

## Features
- Dark UMKC palette with animated gradients and glassmorphism highlights.
- Space Mono navigation typography with uppercase menu items consistent across every page.
- Retro pixel fonts (Press Start 2P / VT323) throughout challenges and hero sections.
- Styled jumbotron, buttons, tables, and forms to match the hacker vibe.
- Footer credit for venkatt.com baked in by default.

## Requirements
- CTFd **v3.8+** (same baseline as `core-beta`).
- Node 18+ / npm for building assets (uses Vite and Sass).

## Quick Install
Clone the repository into your CTFd themes directory and run a build so the static assets are generated:

```bash
cd /opt/CTFd/CTFd/themes
git clone https://github.com/IndrarajBiswas/CTFd-theme-UMKC.git umkc
cd umkc
npm install
npm run build
```

Then log in as an administrator and switch to the `umkc` theme from **Admin Panel → Config → Themes**.

## Development Workflow
1. Install dependencies once with `npm install`.
2. Make edits in `assets/` or `templates/`.
3. Run `npm run build` (or `npm run dev` for a watch build) to regenerate `static/`.
4. Restart your CTFd instance (or the `ctfd` container) to pick up the changes.

## Directory Layout
```
assets/            # SCSS, JS, images processed by Vite
static/            # Compiled JS/CSS served by CTFd (output of npm run build)
templates/         # Jinja templates overriding core-beta
package.json       # Vite/Sass build configuration
vite.config.js     # Vite entry points and copy rules
```

## Credits
- Theme design & customization: [venkatt.com](https://venkatt.com/)
- Base theme & framework: [CTFd](https://github.com/CTFd/CTFd)
