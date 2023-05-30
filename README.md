# hello-quarto

This is a an example of a basic [quarto](https://quarto.org) website.

GitHub Actions provide CI/CD to render and publish to GitHub Pages.

## Setup notes

Stack used:

- R 4.2.2 (2022-10-31) -- "Innocent and Trusting"
- RStudio 2022.12.0+353 "Elsbeth Geranium"
- Quarto 1.3.272
- Packages: tidyverse, palmerpenguins, gt

Alternative: Use [posit cloud](https://posit.cloud) or [podman/docker](https://rocker-project.org/images/versioned/rstudio.html)

Publishing using GitHub Actions:

For a CI/CD setup for publishing to GitHub Pages, see these links for setup:

- [GitHub Pages setup](https://quarto.org/docs/publishing/github-pages.html)
- [CI setup](https://quarto.org/docs/publishing/ci.html#rendering-for-ci)
- [Installing required packages](https://github.com/quarto-dev/quarto-actions/blob/main/examples/example-03-dependencies.md)

For an alternative, see [this setup](.github/workflows/publish-site.yaml).

## Demo

### Documents

- Open the simple Quarto document called `index.qmd` and edit it using the RStudio Visual Editor.
- Bold palmerpenguins and add link to https://allisonhorst.github.io/palmerpenguins/.
- Add code chunk options:
  - `fig-alt`
  - `echo: false` in `execute` in the YAML
  - `code-fold`
  - teaching tip: `echo: fenced`
- Add a figure and a table and cross reference them
- Add a citation: 10.1371/journal.pone.0090081

### Slides

- Change `format: revealjs`
- Add section headings: First level headings Introduction and Analysis, under Analysis a second level heading called Modeling
- Add columns to slides
- Reveal code with `echo: true`
  - teaching-tip: `code-line-numbers`
- Change `output-location` of figure

### Websites

- Add another document `about.qmd`
- Add `quarto.yml` 

```
project:
  type: website

website:
  title: "Hello Quarto"
  navbar:
    left:
      - index.qmd
      - about.qmd
```

- Render
- Add other formats to index.qmd:

```
format:
  html: default
  pdf: default
```

- `publish quarto`
