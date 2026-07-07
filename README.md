name: generate animation

on:
  schedule:
    - cron: "0 0 * * *" # roda todo dia à meia-noite (UTC)
  workflow_dispatch: # permite rodar manualmente pela aba Actions
  push:
    branches:
      - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - name: checkout
        uses: actions/checkout@v4

      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk@v3
        with:
          github_user_name: Cainareiss
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: push para a branch output
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
