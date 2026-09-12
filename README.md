# Personal website
**Note to self from last run/troubleshooting**
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

## Action photos

The three slides in `action/index.qmd` are labeled placeholders. Add images to
`action/`, replace each `field-placeholder` div with an image such as
`<img src="community.jpg" alt="Description of the scene">`, and update the
figcaption with its caption and photo credit. Keep the slide wrappers for the
carousel controls. Run `quarto render` and commit the source and `docs/` output.

## Additional article PDFs

Put PDFs in `writing/` and add a `[PDF](filename.pdf)` link after the matching
citation in `writing/index.qmd`. DOI links are used for the new articles until
their PDFs are supplied; the existing PDF links remain in place.
