# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

This repository is a small, static Portuguese-language website for showcasing 3D-printing filament colors. It has no framework, package manager, build pipeline, or automated test setup.

- `filamentos.html` is the page markup and contains the catalog data plus the JavaScript that builds filament cards in `#filamentGrid`.
- `filamentosStyle.css` provides the page's visual styling and responsive layouts.
- `midia/filamentos/` contains locally stored product images referenced by the catalog in the HTML. Keep those relative paths aligned when changing image names or locations.
- `README.md` currently contains only the project title.

The page is Portuguese (`pt-BR`). Catalog content is maintained in the `filamentos` array in `filamentos.html`; `criarCardFilamento` maps each entry to a card, and `renderizarFilamentos` inserts the cards into the grid. There is no separate data or JavaScript module.

## Development commands

There are no configured build, lint, or test commands. To preview the page, either open `filamentos.html` directly in a browser or serve the repository root locally:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000/filamentos.html`. Stop the server with `Ctrl+C`. There is no single-test command because no test runner or test suite is configured.
