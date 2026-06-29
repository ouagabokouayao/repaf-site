# REPAF_SITE_NOINDEX_V0

Site statique REPAF avec indexation bloquée, préparé pour un dépôt Git local.

## Décision

- Site créé avec `noindex, nofollow, noarchive, nosnippet` sur toutes les pages HTML.
- `robots.txt` bloque tous les robots.
- `_headers`, `netlify.toml`, `vercel.json` et `.htaccess` ajoutent `X-Robots-Tag` quand l’hébergeur le permet.
- Aucun formulaire réel intégré.
- Aucun partenaire, membre, chiffre, adresse physique, téléphone personnel ou donnée sensible publié.
- Aucun dossier `docs/` ne doit rester dans le site publiable.
- Ne pas publier, pousser ou déployer sans validation explicite.

## Pages

- `index.html` : Accueil
- `a-propos.html` : À propos
- `mission.html` : Mission
- `rejoindre.html` : Rejoindre
- `ressources-snee-pepite.html` : Ressources SNEE / Pépite
- `synergies.html` : Synergies
- `contact.html` : Contact
- `talents.html` : Talents à venir
- `activites.html` : Activités à venir
- `mentions-legales.html` : Mentions légales provisoires
- `confidentialite.html` : Confidentialité provisoire
- `accessibilite.html` : Accessibilité

## Structure

```text
repaf-site/
├── *.html
├── assets/
│   ├── css/styles.css
│   ├── js/main.js
│   └── img/
├── robots.txt
├── _headers
├── netlify.toml
├── vercel.json
├── .htaccess
├── .gitignore
└── README.md
```

## Git local

Ce dépôt est destiné à préparer le site localement avant une éventuelle création de dépôt distant.

Commandes autorisées localement :

```bash
git status
git log --oneline
```

Commandes à ne lancer qu'après validation explicite :

```bash
git remote add origin <URL_DU_DEPOT>
git push -u origin main
```

## Protections à vérifier avant toute publication

```bash
grep -R 'noindex, nofollow, noarchive, nosnippet' *.html
cat robots.txt
test ! -e docs
```

## À faire après

- Remplacer le logo temporaire si version vectorielle prête.
- Ajouter les liens sociaux uniquement après vérification.
- Remplacer le placeholder formulaire par un lien testé.
- Compléter l’hébergeur dans les mentions légales.
- Relire avant toute ouverture large.
