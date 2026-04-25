## Project Map

Use this map before exploring the codebase. Prefer editing known files directly instead of running broad searches.

### Core files
- `index.html`: main game shell, menu, screens, modals, card generator iframe entry.
- `styles.css`: global UI, cards, battle layout, map, tutorial, dev tools.
- `js/cards.js`: base card library, card ids, card art aliases, `getCardArtPath`.
- `js/ui.js`: main render functions, `createCardElement`, card visual rendering, card art `<img>` handling.
- `js/game.js`: game state, run flow, combat flow, turn logic.
- `js/effects.js`: card effect resolution, damage, shield, draw, mana, generated effects.
- `js/map.js`: map generation, pathing, node types, shops/events/elites.
- `js/relics.js`: relic pool, relic effects, relic reward logic.
- `js/custom-cards.js`: custom/generated cards, localStorage cards, card image storage/sync.
- `js/dev-tools.js`: dev card manager, enabled/disabled cards, starter deck editor.
- `card-generator/index.html`: card generator UI.
- `card-generator/script.js`: generator logic, export JSON, image/splash/template handling.
- `card-generator/style.css`: generator visual layout.

### Common task routing
- Card art/splash bug: `js/cards.js`, `js/ui.js`, `js/custom-cards.js`, `card-generator/script.js`.
- Card visual/layout bug: `styles.css`, `js/ui.js`.
- Card effect/balance bug: `js/cards.js`, `js/effects.js`.
- Structure/field bug: `js/game.js`, `js/ui.js`, `styles.css`.
- Map/path/shop/event bug: `js/map.js`, `js/game.js`.
- Relic bug: `js/relics.js`, `js/game.js`.
- Tutorial bug: `js/ui.js`, `js/game.js`, `styles.css`.
- Dev tools/custom deck bug: `js/dev-tools.js`, `js/custom-cards.js`, `js/cards.js`.

### Behavior
- Do not run broad exploration unless the target files above are insufficient.
- Prefer inspecting only the listed files relevant to the task.
- Do not print full files unless explicitly asked.
- Apply incremental patches.
- Avoid rewriting whole files.
