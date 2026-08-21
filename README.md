# code3b.github.io

The public site for **The Neon Arrows** — a landing page, the privacy policy and
terms, and `app-ads.txt`.

Separate from the game repository on purpose. GitHub Pages needs a public repo,
and the game's source is not public — so this holds only what is meant to be
read by anyone: three static files, no build step, no dependencies.

| File | Serves | For |
|---|---|---|
| `index.html` | `/` | Homepage. Google's OAuth verification requires one |
| `privacy/index.html` | `/privacy/` | Privacy policy and terms, linked from the app and Play |
| `app-ads.txt` | `/app-ads.txt` | AdMob. **Must** be at the domain root — which is the whole reason this repo exists |

## Updating the policy

The source of truth is `privacy/index.html` here. It was generated from
`legal/combined-for-web.md` in the game repository; edit it here from now on, so
the published page and its source cannot drift apart.

Push to `main` and GitHub Pages redeploys within about a minute.

## Why not Google Sites

The policy used to live on a Google Sites page, which worked for Play but could
never host `app-ads.txt`: that file has to sit at the root of a domain you
control, and `sites.google.com` is Google's. The same requirement applies to
OAuth verification, which needs a homepage and privacy policy on a verified
domain.

One repo solves both.
