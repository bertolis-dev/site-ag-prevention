# Site vitrine AG Prévention

Page vitrine publique d'**AG Prévention** (coordination SPS, prévention HSE, audit sécurité).

- Site **100 % statique** (HTML/CSS + images), sans dépendance serveur.
- Hébergé sur **GitHub Pages** et servi sur le domaine **https://www.ag-prevention.com**.
- Déploiement **automatique** à chaque push sur `main` (GitHub Pages, source « Deploy from a branch » → `main` / racine).

## Structure

```
index.html          Page unique
img/                Logos, favicon, visuel d'accueil, image de partage (og)
CNAME               Domaine personnalisé (www.ag-prevention.com)
.nojekyll           Désactive le traitement Jekyll (site statique pur)
```

## Modifier le site

Éditer `index.html` (ou les images de `img/`), commiter et pousser sur `main` :
GitHub Pages republie automatiquement. Compter 1 à 2 minutes après le push.

> Activation initiale (une seule fois) : dépôt → **Settings → Pages →
> Build and deployment → Source : « Deploy from a branch » → Branch : `main` /
> `(root)` → Save**. Puis renseigner le domaine `www.ag-prevention.com`.

## DNS (chez OVH)

Pour le domaine `ag-prevention.com` :

- `www`  → enregistrement **CNAME** vers `bertolis-dev.github.io.`
- `@` (apex) → 4 enregistrements **A** vers les IP GitHub Pages :
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
  (et, en option, les **AAAA** IPv6 correspondantes).

GitHub redirige alors automatiquement l'apex vers `www` et délivre le HTTPS.
