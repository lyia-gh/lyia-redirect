# lyia-redirect

Redirige `lyia.io` (domaine sans www) vers `https://www.lyia.io`, en conservant le chemin (redirection permanente 301).

Le domaine est acheté chez Wix, qui ne permet pas de faire pointer le domaine nu vers Cloudflare Pages. Ce dépôt est servi par **Netlify** : l'enregistrement A de `lyia.io` pointe vers `75.2.60.5`, Netlify fournit le certificat HTTPS et applique `_redirects` / `netlify.toml`.

`index.html` et `404.html` restent en secours (redirection côté navigateur). GitHub Pages a été abandonné : son certificat est resté bloqué (`bad_authz`).
