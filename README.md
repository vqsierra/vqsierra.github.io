# Personal website

This site uses Quarto. Edit `index.qmd`, `teaching/index.qmd`,
`writing/index.qmd`, and `_quarto.yml`, then run:

```sh
quarto render
quarto preview
```

Commit the source changes **and the regenerated `docs/` directory**.
GitHub Pages publishes the committed HTML; its default build does not render
Quarto source files. Editing only a `.qmd` file will leave the live site unchanged.

The root `CNAME` file is included in Quarto resources so every render preserves
`docs/CNAME` and the `delasierra.io` custom domain.
