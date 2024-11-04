---
author: gaelle8278
title: Pour commencer ...
---
Nouveau blog mis en place avec [jekyll](https://jekyllrb.com/)

Tuto de prise en main :+1: : https://jekyllrb.com/docs/step-by-step/01-setup/

Jekyll tourne avec Ruby : [RubyInstaller](https://rubyinstaller.org/) pour Windows

Pour customiser le thème Minima : 
- [jekyll](https://github.com/jekyll)
- [minima](https://github.com/jekyll/minima)

Github Action utilisée pour publication du site en tant que GitHub Page

```
# Sample workflow for building and deploying a Jekyll site to GitHub Pages
name: Deploy Jekyll with GitHub Pages dependencies preinstalled

on:
  # Runs on pushes targeting the default branch
  push:
    branches: [$default-branch]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Build with Jekyll
        uses: actions/jekyll-build-pages@v1
        with:
          source: ./
          destination: ./_site
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```


Jekyll permet d'éditer en markdown. Jekyll étant propusée par GitHub [voir la doc GitHub][doc-markdown-github]

[doc-markdown-github] : https://docs.github.com/fr/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

On ne peut pas voyager dans le futur, c'est-à-dire qu'un post dont le titre comporte une date postérieure à la date du jour ne sera pas publié/visible à la date du jour.
Mais c'est une fonctionnalité très pratique pour préparer des articles qui seront publiés le jour J 