# SAPCodeMonkey — Full Site Update

**Package date:** July 2026
**What this is:** the complete, current website. Every file here replaces or adds to what's in your GitHub repo. Deploy the whole folder and the site is fully up to date.

---

## What changed in this update

**New: Articles section (12 pages).** Fifteen long-form articles plus an index hub at `articles.html`. Each article has a brand hero banner, an inline diagram, verified source links, and cards linking to its deck and video. This is the "read it" layer that sits alongside watching the video and downloading the deck — and it's what search engines index.

**New: Decks & guides page (`resources.html`).** A filterable download page for all eleven slide decks, reading from `resources.json`.

**Updated: navigation on every page.** The nav is now consistent site-wide:

> Home · Archive · Articles · Decks & guides · Collaborate

(Fiori spotlight and Clean Core are reachable from the home page body and remain in the header on the older pages.)

**Updated: sitemap.** Now lists all 17 pages including every article, so search engines find them.

---

## How to deploy

You upload files to your GitHub repo the same way you have before — through the GitHub web interface, dragging files in. You cannot drag a folder; drag the *files*.

**Step 1 — upload every file in this folder** to the root of your repo (`sapcodemonkey-web/sapcodemonkey`), overwriting when prompted. The new files are the eleven `article-*.html`, `articles.html`, `resources.html`, and `resources.json`; the rest are updates to files already there.

**Step 2 — create the `decks/` folder and upload the PowerPoints.** This is the one manual piece. The articles and the resources page link to decks at `decks/…pptx`, and those files aren't in the repo yet. In GitHub: Add file → Create new file → type `decks/placeholder.txt` (this creates the folder) → commit. Then open the `decks/` folder → Add file → Upload files → drag in all eleven `.pptx` decks from your outputs. Until you do this, the download and "companion deck" buttons will 404.

**Step 3 — confirm.** Give GitHub Pages a minute, then visit the site. Check that Articles appears in the nav, that an article opens with its diagram, and that a deck downloads.

---

## One link to verify before you rely on it

Ten of the eleven articles have fully web-verified source links. One link — the SU25 reference in the security article (`article-security-admin.html`) — is marked "Please verify" in the text, because deep SAP Help URLs move between releases. Open that article, click the SU25 source, and if it's moved, search "SU25" on help.sap.com for the current page. Everything else is confirmed live.

---

## File manifest

### Core pages
| File | What it is |
|---|---|
| `index.html` | Home |
| `archive.html` | Searchable topic archive |
| `articles.html` | **New** — articles index hub |
| `resources.html` | **New** — deck download page |
| `resources.json` | **New** — deck metadata (edit to add decks later) |
| `fiori-spotlight.html` | Fiori transition explainer |
| `clean-core.html` | Clean Core explainer |

### Articles (all new)
| File | Track |
|---|---|
| `article-skills-by-role.html` | Career |
| `article-hcm-deadlines.html` | Career |
| `article-srm-ivalua.html` | Career |
| `article-clean-core.html` | Config |
| `article-treasury.html` | Config |
| `article-workflow-future.html` | Config |
| `article-workflow-admin.html` | Config |
| `article-security-admin.html` | Config |
| `article-f110-payment-run.html` | Config |
| `article-claude-vs-joule.html` | Tech |
| `article-btp-governance.html` | Architecture |

### Supporting files
| File | What it is |
|---|---|
| `sitemap.xml` | Updated — all 17 pages |
| `robots.txt` | Search-engine directives |
| `topics.json` | Archive data |
| `CNAME` | Your domain (do not change) |
| `mascot-*.png`, `og-image.png` | Brand images |

### You add
| Folder | Contents |
|---|---|
| `decks/` | The eleven `.pptx` files (Step 2 above) |

---

## Adding an article or deck later

**A new deck:** upload the `.pptx` to `decks/`, then add one entry to `resources.json` (copy an existing block, change the fields). The resources page picks it up automatically.

**A new article:** it's a standalone HTML file — send me the script or topic and I'll generate it to match, then you upload the one file and I'll give you the two-line edits for `articles.html` and `sitemap.xml`.

---

*Independent SAP commentary. Not affiliated with SAP.*
