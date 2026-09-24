# lyia-redirect

Redirige `lyia.io` (domaine sans www) vers `https://www.lyia.io`, en conservant le chemin.

Le domaine est acheté chez Wix, qui ne permet pas de faire pointer le domaine nu vers Cloudflare Pages. Ce dépôt est donc servi par GitHub Pages : les enregistrements A de `lyia.io` pointent vers `185.199.108.153`, `.109.153`, `.110.153` et `.111.153`, et GitHub fournit le certificat HTTPS.

`404.html` est une copie de `index.html` : toute adresse inconnue, donc toute page de l'ancien domaine, est redirigée vers la même page sur `www.lyia.io`.
