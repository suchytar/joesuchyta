# Joseph Suchyta — Portfolio Website

Static one-page site. Plain HTML/CSS, no build step.

- `index.html`: the page
- `images/`: project photos

## Hosting: GitHub Pages + Porkbun domain

1. Repo → Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
   The site goes live at `https://suchytar.github.io/joesuchyta/`.
2. In the same Pages settings, enter the custom domain (for example `joesuchyta.com`) and save.
   GitHub adds a `CNAME` file to the repo. After DNS resolves, turn on **Enforce HTTPS**.
3. In Porkbun → Domain Management → your domain → **DNS**, delete the default parking
   records (the `ALIAS`/`CNAME` pointing at `pixie.porkbun.com`), then add:

   | Type  | Host  | Answer                |
   |-------|-------|-----------------------|
   | A     | (blank) | 185.199.108.153     |
   | A     | (blank) | 185.199.109.153     |
   | A     | (blank) | 185.199.110.153     |
   | A     | (blank) | 185.199.111.153     |
   | CNAME | www   | suchytar.github.io    |

DNS usually updates within an hour. HTTPS can take up to a day after that.
