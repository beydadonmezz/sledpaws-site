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

Effective date of privacy and terms: **21 October 2026**. The texts describe the monetised build: no account; an age question at first start (under 13 / under the age of digital consent / no answer = child: child-directed non-personalised ads, no ATT prompt, limited analytics); Google AdMob ads with AdMob mediation (optional rewarded ads; interstitials at most every 4th run, never before run 5, never after completing a map; Remove Ads turns them off); Google UMP consent in the EEA/UK/CH, ATT on iOS after consent, choices in the game's Settings → Privacy; Firebase Analytics, Crashlytics and Remote Config; in-app purchases (gem packs, starter pack, Remove Ads, restore) through the App Store and Google Play only; progress only on the device (no cloud save); a KVKK Aydınlatma Metni (privacy §13). **The mediated ad networks are listed in privacy §4 (`#ad-networks`, currently only Google AdMob): add a list item there (en + tr) and change the date before a new network goes live.** Any other change to ads, analytics, purchases or data handling: update privacy, terms and support first, change the date, and deploy before the build ships.

## Source and publishing

The source lives in the game repo at `site/`; the published copy is the `beydadonmezz/sledpaws-site` repo (GitHub Pages, branch `main`, root).

```sh
git clone https://github.com/beydadonmezz/sledpaws-site.git /Applications/Apps/sledpaws-site-publish   # once
rsync -a --delete --exclude '.git' --exclude '.DS_Store' /Applications/Apps/sledpaws/site/ /Applications/Apps/sledpaws-site-publish/
git -C /Applications/Apps/sledpaws-site-publish status --short
git -C /Applications/Apps/sledpaws-site-publish add -A && git -C /Applications/Apps/sledpaws-site-publish commit -m "site: <what changed>"
git -C /Applications/Apps/sledpaws-site-publish push origin main
```
