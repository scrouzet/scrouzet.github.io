# Personal website and blog (Hugo + PaperMod)

Ce repository contient mon site perso et blog, construit avec Hugo et le theme PaperMod.

## Prerequisites

- Hugo extended (version recente)
- Git

## Lancer en local

```bash
hugo server
```

Le site est ensuite disponible sur `http://localhost:1313`.

## Ecrire un nouvel article

Creer un nouveau fichier Markdown dans `content/posts/`, par exemple:

```bash
hugo new posts/mon-nouvel-article.md
```

Puis editer le front matter:

- `title`
- `date`
- `draft` (mettre `false` pour publier)
- `description`
- `tags`

## Newsletter Buttondown

Configurer l'utilisateur Buttondown dans `hugo.toml`:

```toml
[params.buttondown]
username = "votre-username-buttondown"
```

## Publication automatique

Chaque push sur `main` declenche `.github/workflows/hugo.yml` qui:

1. Build le site Hugo
2. Deploy sur GitHub Pages

Assurez-vous que dans les settings GitHub du repo:

- Source = GitHub Actions (et non l'ancien mode branche/Jekyll)
