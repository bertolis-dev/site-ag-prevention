# CLAUDE.md

Site vitrine public d'**AG Prévention** (www.ag-prevention.com). Il suit les conventions
d'**AG-Connect**, l'outil interne de l'entreprise, qui fait référence.

⚠️ **Ce dépôt est PUBLIC** : n'y écrire aucune donnée interne (identifiants Azure ou
SharePoint, clés, IBAN, noms de clients, contenu de dossiers). Les mentions légales
publiques (SIRET, TVA, RCS, adresse du siège) sont autorisées.

## Échanges
- S'adresser à Éric en le **tutoyant**, ton amical.
- Français soigné, **accents respectés** partout (y compris majuscules : « À », « É »).

## Rédaction (règle GLOBALE, identique à AG-Connect)
- ❌ **Jamais de tiret long « — » ni de point médian « · »** dans un texte lu : pages,
  balises `<title>` et `<meta>`, objets de mail (`mailto:`), messages JavaScript affichés,
  réponses dans la discussion. Remplacer selon le sens : deux-points, virgule,
  parenthèses, « et » / « ou ».
- Le trait d'union des mots composés et des références (« R. 4532-1 », « ISO 45001 »)
  n'est pas concerné.
- Références réglementaires citées exactement (Code du travail, articles R. 4532-x).

## Charte graphique
- Couleurs de la charte (doré, navy, fonds clairs) ; **pas de rouge** hors vraie alerte
  (erreur de formulaire).
- **Contraste lisible** toujours : jamais un texte de la même teinte que son fond.
- Boutons dorés : fond foncé = icône claire, fond clair = icône foncée.

## Formulaire de devis (`devis.html`)
- Il envoie à `https://mobile.ag-prevention.com/api/devis`, qui alimente AG-Connect.
- ⚠️ **Ne jamais renommer les attributs `name=` des champs** : ce sont des clés de
  données lues par AG-Connect (même règle que les clés techniques là-bas). On peut
  changer le libellé affiché, pas le `name`.
- Recherche texte insensible aux accents et à la casse.

## Déploiement
- Site 100 % statique, GitHub Pages. **Push sur `main` = mise en ligne immédiate.**
- Travailler sur une branche, puis Pull Request.
