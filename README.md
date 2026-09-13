# Département R&D

Documentation technique des projets du département R&D, générée avec [MkDocs](https://www.mkdocs.org/) et le thème [Material](https://squidfunk.github.io/mkdocs-material/).

## Lancer la documentation en local

```bash
pip install -r requirements.txt
mkdocs serve
```

Puis ouvre http://127.0.0.1:8000 dans ton navigateur. Le site se recharge automatiquement à chaque modification d'un fichier.

## Structure

- `docs/index.md` — page d'accueil (portfolio des projets)
- `docs/projects/<nom-du-projet>/` — un dossier par projet, avec un gabarit commun : aperçu, architecture, conception électronique, modélisation 3D, nomenclature, suivi, téléchargement
- Chaque dossier de projet a son propre fichier `.pages` qui définit son titre et l'ordre de ses pages (plugin `awesome-pages`) — pas besoin de toucher `mkdocs.yml` pour ajouter un projet

## Ajouter un nouveau projet

1. Crée un dossier `docs/projects/<nom-du-projet>/`
2. Copie le gabarit d'un projet existant (les mêmes pages : `index.md`, `architecture.md`, `conception-electronique.md`, `modelisation-3d.md`, `nomenclature.md`, `suivi.md`, `telechargement.md`)
3. Ajoute un fichier `.pages` pour définir le titre et l'ordre des pages
4. Ajoute une ligne dans le tableau de `docs/index.md`

## Déploiement

Le site n'est pas encore publié. Pour le publier sur GitHub Pages : `mkdocs gh-deploy`.
