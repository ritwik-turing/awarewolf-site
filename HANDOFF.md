# AwareWolf — complete project handover

**Status:** production / live

**Owner and voice:** Ritwik Chakradhar

**Public handle:** [@aware._wolf_](https://www.instagram.com/aware._wolf_/)

**Live site:** [ritwik-turing.github.io/awarewolf-site](https://ritwik-turing.github.io/awarewolf-site/)

**Repository:** [github.com/ritwik-turing/awarewolf-site](https://github.com/ritwik-turing/awarewolf-site)

**Current release at handover:** `f645e1c`

**Handover date:** 3 September 2026

This is the implementation, maintenance, deployment, and brand-governance handover for the public AwareWolf website and brandkit. A future designer or developer should be able to take over from this document without reconstructing decisions from chat history.

## 1. First five minutes

The project is a zero-build static site: plain HTML, CSS, and JavaScript. Google Fonts is the only runtime dependency. Do not add a package manager, framework, CMS, bundler, or component library unless the project is explicitly re-scoped.

From this folder:

```sh
python3 -m http.server 8765
```

Open `http://localhost:8765/`. There is no install command and no build command.

The production files live directly in the repository root. Pushing `main` updates the current GitHub Pages deployment. The same folder can also be deployed to Netlify without a build step.

## 2. Source-of-truth order

When two files or instructions appear to conflict, use this order:

1. [`awarewolf_brand-system_v3.html`](awarewolf_brand-system_v3.html) — the complete 14-chapter brand system. It supersedes v2.
2. [`brand/tokens.css`](brand/tokens.css) — the machine-readable UI palette and type tokens.
3. The approved v15 master identity and current founder master listed in the asset manifest below.
4. The current seven HTML pages, [`styles.css`](styles.css), and [`site.js`](site.js).
5. Older files in `brand/` — provenance and rollback only; never current references.

Do not use chat transcripts or an archived image as a substitute for the current brand system.

## 3. The brand contract

### Core proposition

AwareWolf lives where scientific discipline, Sanatan thought, and play meet. The thesis is **aware presence**: Ritwik is great at many things; at the others he stays present, gets up, adjusts, and becomes better. Never frame him as someone who loses, is bad at things, or turns failure into an identity.

Science and tradition may **rhyme, not prove each other**. The brand is spiritually open and scientifically agnostic about metaphysical mechanisms. Never say that quantum physics proves scripture, that a deity is a quantum object, or that distinct traditions are secretly identical.

### Voice

- First person when Ritwik speaks.
- Lowercase display copy and headings.
- Plain, direct, curious, warm, playful, and evidence-literate.
- State the caveat before the conclusion.
- Preserve Ritwik's confidence: “i stay present. i notice. i get better.”
- Fixed closing phrases: “stay awake. stay wild.” and “play… everything.”
- Do not use: “manifest,” “vibration,” “frequency,” “unlock,” “journey,” or “transform.”
- Do not write generic mystical or synthetic-sounding copy.

### Identity meaning

- One precisely symmetric wolf: Shiva on the left and Narayana on the right.
- Agni and Jal are the elemental fields.
- One continuous quantum field bridges the two halves. It is not separate decoration on both sides.
- The rim, sacred artifacts, natural materials, Kailash, Ananta Shesha, and central `Ĥψ` are a locked composition. Chapter 07 specifies the complete reading.
- The exact public handle is `@aware._wolf_`. Inside the identity, `aware` belongs to Jal and `._wolf_` belongs to Agni. The trailing underscore is mandatory.
- Natural materials are intentional: living lotus; wood and hide damaru; carved wood eight-spoke Dharmachakra; terracotta Shakti trikoṇa; sandstone Ik Onkar; rustic basalt lingam; river-worn Shaligram; and hand-forged Trishul, Sudarshana, and Kaumodaki.

### Never do this

- Never recolour, filter, stretch, mirror, knock out, or rebuild the v15 identity.
- Never typeset the AwareWolf wordmark or repair its punctuation with live text.
- Never detach sacred artifacts from the complete identity for generic decoration.
- Never auto-trace the master into a vector; the material textures and surreal transitions are part of the artwork.
- Never add lotus, monk, galaxy, glowing brain, Om, trident, or other spiritual imagery to the website UI. Sacred imagery belongs to the approved identity or to specifically sourced content.
- Never use stock imagery or generated b-roll as ambient decoration.

## 4. Project map

| Path | Role | Maintenance note |
| --- | --- | --- |
| [`index.html`](index.html) | Home | Night cover, v15 lockup, thesis, Sanskrit triad, pillars, PLAY/AWAKE calls, manifesto, footer. |
| [`name.html`](name.html) | The name | Bone reading page; four textual readings of the name. |
| [`names.html`](names.html) | The nine names | Bone reading page; nine full-width Sanskrit/science/rule rows. |
| [`standard.html`](standard.html) | The quantum standard | Bone reading page; finding/frontier/interpretation framework and language rules. |
| [`play.html`](play.html) | PLAY | Night interactive picker, all 21 activities, reel script, and no-JS path. |
| [`awake.html`](awake.html) | AWAKE | Night studies page; editable JavaScript array plus matching no-JS fallback. |
| [`pack.html`](pack.html) | The pack | Bone community page; no form, account, or email capture. |
| [`styles.css`](styles.css) | Shared website presentation | Imports tokens first, then Google Fonts; all site components and responsive rules live here. |
| [`site.js`](site.js) | PLAY behavior | Random picker only in current markup; prevents an immediate repeated result. |
| [`brand/tokens.css`](brand/tokens.css) | Design tokens | Exact UI colours and type families. Do not introduce ad-hoc colour values in site CSS. |
| [`awarewolf_brand-system_v3.html`](awarewolf_brand-system_v3.html) | Brandkit | Public, standalone 14-chapter source of truth. Keep synchronized with approved identity changes. |
| [`netlify.toml`](netlify.toml) | Netlify configuration | Publishes `.` with an empty build command and supplies basic security headers. |
| [`README.md`](README.md) | Quick operating notes | Shorter companion to this handover. |
| `brand/` | Current and archived assets | Current files are explicitly listed below. Treat every other image as archived. |
| `media/` | Local user-owned working material | Untracked at handover. Do not stage, delete, or deploy it without explicit owner approval. |

## 5. Page and behavior matrix

| Page | Surface | Primary purpose | JavaScript | Without JavaScript |
| --- | --- | --- | --- | --- |
| Home | Night | Explain the thesis and route visitors | None | Complete |
| The name | Bone | Explain the name through four textual references | None | Complete |
| The nine names | Bone | Pair nine traditional names with disciplined scientific rhymes | None | Complete |
| The quantum standard | Bone | Establish the evidence standard | None | Complete |
| PLAY | Night | Choose one activity and carry the reel experience into the site | Random picker | All 21 activities remain available in native `details` elements, with a `noscript` instruction |
| AWAKE | Night | Publish sources with limitations and tier labels | Renders the study array | A full duplicate fallback list remains visible |
| The pack | Bone | Explain participation and community behavior | None | Complete |

The shell is repeated directly in each page by design. With only seven static pages, keeping it native avoids a build system. When navigation changes, update all seven pages and verify `aria-current="page"` on each.

## 6. Current asset manifest

### Approved assets

| Asset | Dimensions | Bytes | SHA-256 | Use |
| --- | ---: | ---: | --- | --- |
| `brand/awarewolf_identity_v15_master.png` | 1254×1254 | 3,516,365 | `96adc1a0008a133174ddf63588a776e0f346a3f2f6ccd534ecf8ba5136667251` | Approved production master. Never load directly on the website. |
| `brand/awarewolf_identity_v15.webp` | 640×640 | 57,168 | `1c1bcc4d859a6d8860676e10d3c89b7c98a2b3493af7a98e78fe6a772c2c21ce` | Full website identity and exact handle. Maximum rendered width: 520 px. |
| `brand/awarewolf_mark_v15.webp` | 192×192 | 9,762 | `768935eb2c293a6f55bf521ba093425ff3bf2bd7bf2252e686f383c1ec202a9f` | Navigation mark and avatar source. |
| `brand/awarewolf_favicon_v15.png` | 64×64 | 10,125 | `9450fce249075c427d74151e75ccf648e035e4a83c06076b2eda0b12914bbb65` | Browser icon. |
| `brand/ritwik-founder-portrait-v3-master.png` | 1084×1451 | 1,975,857 | `5caf624f60437b3e91e8dd5b607da0393aca5243264c491296b4c5c327dacf81` | Current founder production master with the complete v15 shirt identity. Never load directly on a webpage. |
| `brand/ritwik-founder-portrait-v3.webp` | 640×857 | 35,882 | `5fbe42cbd02601553e0436dbfaf687a3f60c33196f21aecfef8a1bce63e03381` | Founder bios, press kit, and creator introduction. |

The full-resolution founder deliverable is also available on the current owner's machine at `/Users/ritwikmac/Downloads/Ritwik_Aware_Wolf_Shirt_v15.png`. The repository master is the durable project copy.

### Archived assets

Files named `awarewolf_identity_v6.webp` through `v14`, matching `awarewolf_mark_v6.webp` through `v14`, the original alpha/white/source files, and `ritwik-founder-square-v1.webp` remain for provenance and rollback. They are not approved for new work. Do not infer current status from modification time; only this manifest defines current assets.

### Asset replacement procedure

1. Keep the approved master unchanged; make derivatives from a copy.
2. Preserve intrinsic aspect ratio and do not crop any handle character.
3. Produce a WebP derivative below 60 KB.
4. Give the new generation a new versioned filename rather than silently overwriting v15.
5. Update every HTML reference, intrinsic `width`/`height`, descriptive alt text, the brand-system chapter 07/12 entries, README, and this manifest together.
6. Verify the image at 360 px and on a 2× desktop display.
7. Compare the final artifact visually with the master before committing.

`cwebp` is installed on the current Mac. Use a temporary output while tuning quality; do not overwrite the approved derivative until it has passed visual and size checks:

```sh
cwebp -quiet -q 72 -m 6 -resize 640 640 brand/new_identity_master.png -o /tmp/new_identity.webp
stat -f '%z bytes' /tmp/new_identity.webp
```

If the 1254 px identity master is insufficient for print, commission a faithful higher-resolution recreation. Do not fabricate a vector from the raster.

## 7. Design tokens and usage

All website colours must come from [`brand/tokens.css`](brand/tokens.css).

| Token | Value | Approved role |
| --- | --- | --- |
| `--aw-shiva` | `#DA8835` | Agni accent on night |
| `--aw-shiva-ink` | `#89370F` | Agni accent on bone |
| `--aw-narayan` | `#226D8A` | Jal accent on bone |
| `--aw-narayan-ink` | `#205163` | Pressed Jal blue on bone |
| `--aw-narayan-light` | `#5AAFD0` | Jal accent on night |
| `--aw-quantum` | `#4FCAD7` | Evidence and field seam on night only |
| `--aw-quantum-ink` | `#146D76` | Evidence on bone only |
| `--aw-panchaloha` | `#C28A45` | Frontier tags and spoken emphasis only; never a generic control |
| `--aw-lotus` | `#C97467` | Identity artwork only |
| `--aw-terracotta` | `#9A5A26` | Identity artwork only |
| `--aw-basalt` | `#212729` | Identity material and primary ink |
| `--aw-wood` | `#5F4933` | Identity artwork only |
| `--aw-night` | `#091625` | Primary night ground |
| `--aw-night-2` | `#11364A` | Raised night surface |
| `--aw-line` | `#205163` | Night dividers and borders |
| `--aw-bone` | `#F1E8D6` | Primary reading ground |
| `--aw-bone-2` | `#E6D9C3` | Raised bone surface |
| `--aw-bone-3` | `#D0AD8B` | Secondary text on night and interpretation tier |
| `--aw-ink` | `#212729` | Primary reading text |
| `--aw-stone` | `#5E5F56` | Secondary reading text |

Target distribution is 70% ground, 20% ink, 5% Agni, and 5% Jal. Quantum is evidence-only. Panchaloha is frontier/spoken-only. Lotus, terracotta, basalt, and wood are artwork materials, not a general website palette.

The audited contrast ratios are:

- Agni on night: 6.55:1
- Shiva ink on bone: 6.59:1
- Jal on bone: 4.76:1
- Jal light on night: 7.35:1
- Quantum on night: 9.33:1
- Quantum ink on bone: 4.96:1
- Panchaloha on night: 6.08:1
- Stone on bone: 5.31:1

Do not substitute the same accent across both surfaces. The `body.reading` and `body.night` variables deliberately select accessible surface-specific values.

## 8. Typography, layout, and components

### Typography

- Display and all headings: Anton, weight 400, lowercase.
- Body: Karla, regular/medium/bold.
- Sanskrit: Tiro Devanagari Sanskrit.
- Fallbacks are declared in tokens and must remain usable if Google Fonts fails.
- Every Sanskrit span must have `lang="sa"` and an English translation immediately beneath it.

### Layout

- Mobile-first, minimum acceptance viewport 360 px.
- Shared content shell: `min(viewport - 2rem, 72rem)` on mobile; `min(viewport - 4rem, 72rem)` from 48 rem.
- Main breakpoint: 48 rem. The standalone brand-system document uses its own 900 px breakpoint.
- Section padding: 5 rem vertically.
- Header minimum height: 4.5 rem.
- Body copy measure: 66 characters.
- Full identity: never wider than 520 px.
- On mobile the navigation remains one horizontally scrollable line beneath the mark. It does not depend on JavaScript.
- Night pages remain night and reading pages remain bone in both OS colour schemes through explicit `color-scheme` and body backgrounds.

### Reusable components and states

- `.field-mark`: two open Agni/Jal phase curves crossing a thin quantum seam. It is the only reusable site motif. Never close it into a circle or add sacred artifacts.
- `.card`: bone or night raised surface selected by the body theme.
- `.tier-finding`: quantum/evidence.
- `.tier-frontier`: panchaloha/frontier.
- `.tier-interpretation`: bone-3/interpretation.
- `.call`: full-card link; first door uses Agni, second uses Jal.
- `.play-button` / `.button`: Agni action with night text.
- `.accordion details`: native disclosure state; do not replace with a script-only accordion.
- Links: inherit by default; use the surface's Jal/pressed accent on hover.
- Buttons: opacity reduces to `.86` on hover.
- Focus: 3 px visible accent outline with 4 px offset.
- There are no loading, disabled, error, authentication, form, or empty-data states in the current product.

### Motion

Only opacity, text colour, and background-colour transitions are used, at 0.25 seconds. No movement, parallax, spinning, pulsing, or decorative animation. `prefers-reduced-motion: reduce` removes transitions and smooth scrolling.

## 9. Accessibility contract

- WCAG AA contrast is the minimum.
- Keep the skip link and the `main` target.
- Keep semantic heading order, landmark elements, native buttons, links, summaries, and details.
- Keep the main navigation's accessible label and correct `aria-current` value.
- Decorative field marks use `aria-hidden="true"`.
- Identity alt text describes the composition; the navigation mark alt is concise. Do not use the filename as alt text.
- AWAKE's generated list is an `aria-live="polite"` region.
- Never communicate a claim tier by colour alone; the written tier label must remain visible.
- Keyboard focus must be visible on every control.
- The site must stay fully readable at 200% zoom and at 360 px without page-level horizontal overflow.

## 10. Content maintenance

### AWAKE studies

In [`awake.html`](awake.html), edit `const STUDIES` near the end. Each item uses:

```js
{
  tier: 'finding',
  title: 'lowercase title',
  meta: 'journal · month year · n=',
  line: 'one plain limitation or takeaway',
  url: 'https://primary-source.example/'
}
```

Allowed tiers are exactly `finding`, `frontier`, and `interpretation`:

- **finding:** peer-reviewed result or authoritative primary report; say what was actually observed.
- **frontier:** credible active hypothesis or unsettled work; never present it as consensus.
- **interpretation:** scripture, philosophy, metaphor, or Ritwik's reading; never present it as experimental evidence.

The static fallback immediately above the script duplicates the same 11 entries. Update the array **and** fallback in the same commit. The current renderer uses `innerHTML`, so content must be maintainer-controlled; do not connect it directly to untrusted user input.

Use primary sources whenever possible. For scientific claims, include the journal and date, sample size or evidence type, and the important limitation. Recheck links and time-sensitive claims before publication. The source standard and canonical spiritual/iconographic references live in chapter 14 of the brand system.

### PLAY activities

The random-picker source is the `sports` array in [`site.js`](site.js). The permanent no-script/browser-readable list is the 21 `details` blocks in [`play.html`](play.html). Add, remove, rename, or rewrite an activity in both places.

The picker must continue to:

- run only after a user action;
- avoid returning the same result twice in succession;
- use text content rather than injecting selected data as HTML;
- leave the native all-activities list usable at all times.

### Sitewide copy changes

For navigation, handle, footer, asset version, or terminology changes, search all HTML first:

```sh
rg -n 'aware\._wolf_|awarewolf_mark_v15|awarewolf_favicon_v15|main navigation' --glob '*.html'
```

Preserve lowercase headings, exact Sanskrit spelling, `lang="sa"`, immediate translations, claim tiers, and the manifesto unless the brand owner explicitly approves a source-of-truth change.

## 11. Performance and privacy

- Target under one second on a good 4G connection and prioritize Instagram's in-app browser.
- Website image derivatives must remain at or below 60 KB. Large masters must never appear in an HTML `src`.
- Always provide intrinsic image dimensions to reduce layout shift.
- No analytics, trackers, cookies, accounts, forms, APIs, storage, or email capture exist at handover.
- External runtime requests are limited to Google Fonts and links a visitor deliberately opens.
- Netlify supplies `nosniff`, strict-origin-when-cross-origin referrer policy, and same-origin framing headers. GitHub Pages does not read `netlify.toml`; confirm equivalent platform behavior if those headers become a hard requirement.

## 12. Deployment

### Current production: GitHub Pages

The public site is deployed from the repository's `main` branch and repository root. A normal release is:

```sh
git status --short
git diff --check
git add HANDOFF.md README.md index.html name.html names.html standard.html play.html awake.html pack.html styles.css site.js brand/tokens.css brand/<explicit-current-files>
git commit -m "Describe the release"
git push origin main
```

The explicit add list is intentional. Do not use `git add .` while the owner-only `media/` folder is present.

After pushing, allow GitHub Pages time to publish, then verify:

```sh
for page in '' name.html names.html standard.html play.html awake.html pack.html awarewolf_brand-system_v3.html; do
  curl -fsS -o /dev/null -w '%{http_code}  %{url_effective}\n' "https://ritwik-turing.github.io/awarewolf-site/${page}"
done
```

Append `?v=<short-commit>` when sharing a just-deployed page to bypass a stale browser cache. This is only cache-busting; it is not a different deployment.

### Netlify alternative

Either drag the repository folder into Netlify Drop or connect the repository with:

- Build command: empty
- Publish directory: `.`
- Production branch: `main`

[`netlify.toml`](netlify.toml) already encodes the empty build and publish directory plus headers. No environment variables are required.

## 13. Verification before every release

Run the smallest mechanical checks first:

```sh
node --check site.js
git diff --check
find brand -maxdepth 1 -type f \( -name '*.webp' -o -name '*.png' \) -print0 | xargs -0 stat -f '%N %z bytes'
```

Then serve locally and inspect all eight documents: the seven pages plus the brand system.

### 360 px acceptance pass

- No page-level horizontal overflow.
- Navigation can be reached and scrolled horizontally.
- No clipped headings, labels, Sanskrit, handle punctuation, or controls.
- All local images load with the correct aspect ratio.
- The full identity is never rendered above 520 px or stretched.
- PLAY works with JavaScript; its full list works without JavaScript.
- AWAKE has identical content with JavaScript enabled and disabled.
- Night and bone surfaces remain fixed under light and dark OS preferences.

### Content and brand pass

- Every internal link resolves.
- Every page has a unique useful title and description.
- Every page has one main landmark and a logical heading structure.
- Every Sanskrit span has `lang="sa"` and English directly beneath.
- Every display heading reads lowercase.
- Finding/frontier/interpretation labels match the claims they carry.
- Quantum cyan appears only on evidence and the field mark.
- Panchaloha is not used for generic links or buttons.
- Agni and Jal remain minor accents rather than grounds.
- No unapproved stock imagery, icons, illustrations, or motifs were added.
- The exact `@aware._wolf_` handle is intact everywhere.
- The identity has not been recoloured, filtered, mirrored, reconstructed, or detached from its composition.

### Public pass

- All production URLs return HTTP 200.
- Hard-refresh and test the cache-busted URL.
- Confirm the deployed web asset checksum matches the committed derivative when an image changed.
- Open the site in a real mobile browser or Instagram in-app browser when possible, not only responsive desktop mode.

The last full audit before this handover passed local-link, image-reference, language, Sanskrit-translation, lowercase-heading, alt-text, unique-ID, JavaScript syntax, whitespace, and 360×800 real-Chrome checks. All eight public documents returned HTTP 200, and every web image remained below 60 KB.

## 14. Known limitations and risks

- The approved identity master is a 1254 px raster, not a vector. It is sufficient for current web use but not arbitrary large-format print.
- The header/footer shell is duplicated across seven HTML files. This is deliberate for zero-build simplicity, but sitewide changes require careful search-and-update.
- AWAKE duplicates records for progressive enhancement. Drift between the array and fallback is the main content-maintenance risk.
- No automated CI is configured; release checks are currently local and manual.
- Scientific sources and external URLs can age or change. Review them before any new scientific claim or major campaign.
- Google Fonts is an external dependency. System fallbacks preserve function, but the exact visual voice depends on the font request succeeding.
- Archived assets share the `brand/` folder with current assets. Always use this manifest and versioned filenames.
- The GitHub Pages publishing setting is managed outside the repository. If the site stops deploying after a successful push, check repository Pages settings and Actions status.
- The founder portrait's shirt artwork is a deliberate edit of the supplied outdoor photo. Preserve the approved v3 master and do not repeatedly regenerate the person, background, face, or clothing.

## 15. Rollback and release history

Git is the rollback mechanism. Do not delete approved masters or rewrite history. Revert a release with a new commit after confirming the exact target.

Important milestones:

| Commit | Meaning |
| --- | --- |
| `f645e1c` | Founder portrait updated with the final v15 shirt identity |
| `7b73044` | Full brandkit aligned with the final identity |
| `2d74e7f` | Final v15 surrealist identity adopted |
| `2dcefcc` | Tonal balance refined in v14 |
| `bf85fb8` | Quantum bridge shaped as a wave packet |
| `7a5d8c4` | Quantum bridge simplified to Hamiltonian psi |
| `f6fb117` | PLAY reframed around aware presence |

Useful inspection commands:

```sh
git log --oneline --decorate -20
git show <commit> --stat
git diff <older-commit>..<newer-commit> -- brand/ awarewolf_brand-system_v3.html styles.css
```

## 16. Definition of done

A future AwareWolf website or brandkit release is complete only when:

- the change agrees with the 14-chapter v3 brand system;
- current assets, tokens, pages, README, and this handover agree;
- the scientific claim tier and source are honest;
- the design remains accessible, mobile-first, lightweight, and useful without JavaScript;
- the v15 identity and exact handle remain intact;
- all local and production checks pass;
- only intentional project files are committed; and
- the live GitHub Pages URL shows the committed release.

When the brand system is silent, choose the quieter option.
