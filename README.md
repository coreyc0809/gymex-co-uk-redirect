# gymex-co-uk-redirect

Owns `gymex-fitness.co.uk` on GitHub Pages and forwards every path to the same
path on **https://gymex.fitness** (the real site lives in `gymex-web`).

- One stub per old page (canonical + meta refresh + JS) so Google moves rankings.
- `404.html` forwards everything else (`/r/CODE`, `/rank/ID`, …).
- `.well-known/` is served as real files, **not redirected** — installed app builds
  only trust `gymex-fitness.co.uk` for universal/app links. Keep it in sync with
  `gymex-web/.well-known/` and never delete this repo while old builds exist.
