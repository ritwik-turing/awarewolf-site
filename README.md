# AwareWolf brandkit and website

A complete brandkit plus a seven-page static site. There is no build step and no framework.

For the full implementation, asset, maintenance, deployment, rollback, and QA record, read [`HANDOFF.md`](HANDOFF.md).

## Source of truth

Open `awarewolf_brand-system_v3.html`. This is the current 14-chapter brand system and replaces v2 for all new work. It defines the meaning, voice, visual identity, colour roles, typography, motion, content architecture, applications, checks, and source map.

The approved system is built around these fixed ideas:

- One symmetric wolf: Śiva on the left, Nārāyaṇa on the right.
- Agni and Jal are the elemental fields. The quantum field bridges the two; it is not repeated as separate decoration.
- The brand is spiritually open and scientifically agnostic about metaphysical mechanisms. Science and tradition may rhyme; neither is presented as proof of the other.
- Aware presence is the practical thesis: Ritwik is great at many things and stays present, keeps getting up, and gets better at the others.
- Sacred artifacts stay inside the complete identity unless the content is specifically about them. Their materials should feel real: wood, hide, stone, clay, living plant, forged metal, fire, and water.
- The public handle is exactly `@aware._wolf_`. Inside the artwork, `aware` is Jal and `._wolf_` is Agni. Never repair or rebuild it with live text.

`brand/tokens.css` is the machine-readable palette. New UI uses the semantic `--aw-shiva*`, `--aw-narayan*`, `--aw-quantum*`, and `--aw-panchaloha` tokens. The old vermilion/gold/lab tokens are retired.

The reusable site motif is `.field-mark`: two open Agni/Jal phase curves crossing a thin quantum seam. It replaces the old crescent motif. It is not a miniature logo and must not acquire sacred artifacts.

## Edit the AWAKE studies

Open `awake.html` and find `const STUDIES` near the bottom. Each item has five fields:

- `tier`: `finding`, `frontier`, or `interpretation`
- `title`: the lowercase card heading
- `meta`: `journal · month year · n=`
- `line`: one plain-English limitation/takeaway
- `url`: the source link

The HTML immediately above that script is the no-JavaScript fallback. Keep it aligned with the array when publishing a change so the full source list remains available when scripts are blocked.

## Identity files and future masters

Keep the same filenames and replace the files in `brand/`, or update the `src` values site-wide:

- `brand/awarewolf_identity_v15.webp` is the current full emblem and `aware._wolf_` lockup. It is the approved radiant surrealist identity: a precisely symmetric Shiva/Narayana wolf, Kailash and seven-hooded Ananta Shesha as matched backdrops, Nataraja fire and Kṣīra Sāgara as the rim, and one continuous quantum field carrying only `Ĥψ` at the centre.
- `brand/awarewolf_mark_v15.webp` is the current emblem-only navigation crop.
- `brand/awarewolf_favicon_v15.png` is the 64×64 browser icon derived from the official mark crop.
- `brand/awarewolf_identity_v15_master.png` is the exact 1254×1254 approved master artwork shipped with the brandkit. Do not load this large source file on a webpage; derive future formats from it non-destructively.
- Sacred artifacts use materially honest construction: living lotus, wood-and-hide damaru, carved-wood eight-spoke Dharmachakra, terracotta Shakti trikoṇa, sandstone Ik Onkar, rustic basalt liṅgam, river-worn Shaligram, and hand-forged aged weapons including Kaumodakī between the lotus and Shaligram.
- The original supplied assets remain beside them for provenance and rollback, but they are not current brand assets.

The website UI continues to use `brand/tokens.css` as its source of truth. The artwork's broader natural-pigment palette is part of the identity image, not permission to introduce new UI colours. Keep the quantum bridge continuous across the two halves; never repeat it as unrelated decoration on each side.

Keep the intrinsic proportions. Do not add CSS filters or recolour the art. The current CSS caps the identity lockup at 520 px. The two website-ready v15 files are each below 60 KB.

Do not auto-trace the master into a vector. Its material texture and surreal transitions are part of the identity. If larger production work is needed, commission a faithful high-resolution recreation from the approved composition, then export new web derivatives without changing the existing names until every reference is ready to move together.

## Founder photography

- `brand/ritwik-founder-portrait-v3.webp` is the current founder portrait for bios, press kits, profile images, and creator introductions. It keeps the supplied outdoor city-and-bay portrait and replaces the superseded shirt graphic with the complete v15 identity.
- `brand/ritwik-founder-portrait-v3-master.png` is the 1084×1451 production master with the corrected v15 shirt print. Do not load this large file on webpages.
- `brand/ritwik-founder-square-v1.webp` is archived. Do not use it in new work.
- Keep the original 3:4 portrait whenever the placement allows. A tighter platform crop is permitted only when the face and complete shirt graphic remain visible.
- Do not further regenerate, beautify, replace the background, recolour the shirt, or separate the shirt emblem from its exact `aware._wolf_` handle.
- The shirt uses the complete latest v15 identity, including its sacred-material composition, continuous quantum bridge and exact trailing underscore. For every standalone identity use, return to the v15 files above rather than extracting the photographed print.
- The current web derivative is 640×857 and below 60 KB.

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

All seven pages share `styles.css`, which imports `brand/tokens.css`. Home, PLAY, and AWAKE stay on the quantum-night ground in both OS colour schemes; reading pages stay on bone.

## Release checklist

- Open every page at 360 px and confirm there is no horizontal page overflow.
- Confirm every internal link and local image resolves.
- Confirm every Sanskrit line has `lang="sa"` and an English line directly beneath.
- Confirm headlines render lowercase, focus is visible, and motion is opacity-only at 0.4 seconds or less.
- Confirm quantum cyan is used only for evidence and the field mark; panchaloha is not used for buttons or generic links.
- Confirm the v15 identity is not stretched, recoloured, filtered, mirrored, or reconstructed.
- Confirm there is no stock or generated b-roll outside the approved identity artwork.
