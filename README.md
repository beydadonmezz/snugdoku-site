# snugdoku-site

Public website for **Snugdoku**: home, Privacy Policy, Terms of Use and Support, in English and Turkish. Plain static
HTML plus one CSS file; no JavaScript, cookies, trackers or external requests. Same setup as `beydadonmezz/sledpaws-site`.

Live URL: `https://beydadonmezz.github.io/snugdoku-site/` (privacy `/privacy/`, terms `/terms/`, support `/support/`, Turkish under `/tr/`).

Source: the old Snugdoku game repo, archived on 2026-10-21 at `/Applications/Apps/_arsiv/snugdoku-eski` (`tools/site/build.py`
writes `site/`). Run the commands below from that folder, NOT from `/Applications/Apps/snugdoku` (now the merged app). Publish:

```sh
python3 tools/site/build.py
rsync -a --delete --exclude '.git' --exclude '.DS_Store' site/ /Applications/Apps/snugdoku-site-publish/
git -C /Applications/Apps/snugdoku-site-publish add -A && git -C /Applications/Apps/snugdoku-site-publish commit -m "site: <what changed>" && git -C /Applications/Apps/snugdoku-site-publish push
```
