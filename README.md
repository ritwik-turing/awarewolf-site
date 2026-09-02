# AwareWolf website

A seven-page static site. There is no build step and no framework.

## Edit the AWAKE studies

Open `awake.html` and find `const STUDIES` near the bottom. Each item has five fields:

- `tier`: `finding`, `frontier`, or `interpretation`
- `title`: the lowercase card heading
- `meta`: `journal · month year · n=`
- `line`: one plain-English limitation/takeaway
- `url`: the source link

The HTML immediately above that script is the no-JavaScript fallback. Keep it aligned with the array when publishing a change so the full source list remains available when scripts are blocked.

## Swap the logo for a vector

Keep the same filenames and replace the files in `brand/`, or update the `src` values site-wide:

- `brand/awarewolf_identity_v7.webp` is the current full emblem and `aware._wolf_` lockup.
- `brand/awarewolf_mark_v7.webp` is the current emblem-only navigation mark.
- The original supplied assets remain beside them for provenance and rollback.

Keep the intrinsic proportions. Do not add CSS filters or recolour the art. The current CSS caps the identity lockup at 520 px.

## Deploy to Netlify

Drag this `awarewolf` folder into Netlify Drop, or connect the repository and set the publish directory to this folder. Leave the build command empty. `netlify.toml` already declares the current folder as the publish directory.

## Pages

- `index.html` — home
- `name.html` — the name
- `names.html` — the nine names
- `standard.html` — the quantum standard
- `play.html` — PLAY
- `awake.html` — AWAKE
- `pack.html` — the pack
