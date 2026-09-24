# lyia-redirect

Redirige `lyia.io` (domaine sans www) vers `https://www.lyia.io`, en conservant le chemin (redirection permanente 301).

Le domaine est acheté chez Wix, qui ne permet pas de faire pointer le domaine nu vers Cloudflare Pages. Ce dépôt est servi par **Netlify** (site `lyia-redirect`) : l'enregistrement A de `lyia.io` pointe vers `75.2.60.5` et le CNAME `go.lyia.io` vers `lyia-redirect.netlify.app`. Sur Netlify, `go.lyia.io` est le domaine principal et `lyia.io` un alias : avec `lyia.io` en principal, Netlify exigerait que `www.lyia.io`, hébergé sur Cloudflare, pointe aussi vers lui. Netlify fournit le certificat HTTPS (Let's Encrypt, renouvelé automatiquement) et applique `_redirects` / `netlify.toml`.

Déploiement : `netlify deploy --prod --dir . --site lyia-redirect --no-build`.

`index.html` et `404.html` restent en secours (redirection côté navigateur). GitHub Pages a été abandonné : son certificat est resté bloqué (`bad_authz`).
