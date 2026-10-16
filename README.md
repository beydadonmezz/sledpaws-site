# sledpaws-site

Public website for **Sledpaws** (the game; its App Store and Google Play name is **"Sledpaws: Snow Slide"**): home page, Privacy Policy, Terms of Use and Support, in English and Turkish. Plain static HTML plus one CSS file. No build step, no JavaScript, no cookies, no trackers, no external requests; each page sets a strict Content-Security-Policy. Same setup as `beydadonmezz/fishburg-site`.

Live URL: `https://beydadonmezz.github.io/sledpaws-site/`

| Page | English | Turkish |
|---|---|---|
| Home | `/` | `/tr/` |
| Privacy Policy | `/privacy/` | `/tr/privacy/` |
| Terms of Use | `/terms/` | `/tr/terms/` |
| Support | `/support/` | `/tr/support/` |

Developer name: seller name exactly as App Store Connect shows it, **BEYDANUR DONMEZ**; the first mention on each page adds "BEYDANUR DONMEZ (Beydanur Dönmez)".

Effective date of privacy and terms: **16 October 2026**. The texts describe the current build: no account, no ads, no analytics, no in-app purchases, progress only on the device. **Before a build with AdMob or in-app purchases ships, update privacy (§2 to §8), terms (§4) and support, change the effective date, and deploy first** (TASKS.md tracks this).

## Source and publishing

The source lives in the game repo at `site/`; the published copy is the `beydadonmezz/sledpaws-site` repo (GitHub Pages, branch `main`, root).

```sh
git clone https://github.com/beydadonmezz/sledpaws-site.git /Applications/Apps/sledpaws-site-publish   # once
rsync -a --delete --exclude '.git' --exclude '.DS_Store' /Applications/Apps/sledpaws/site/ /Applications/Apps/sledpaws-site-publish/
git -C /Applications/Apps/sledpaws-site-publish status --short
git -C /Applications/Apps/sledpaws-site-publish add -A && git -C /Applications/Apps/sledpaws-site-publish commit -m "site: <what changed>"
git -C /Applications/Apps/sledpaws-site-publish push origin main
```
