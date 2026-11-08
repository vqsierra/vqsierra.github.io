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

The In-Action carousel in `in-action/index.qmd` displays eight photos from
`in-action/photos/`, with captions from `in-action/photos/descriptions.txt`.
Web copies are resized to a maximum dimension of 1800 pixels; keep the original
photos in your source folder. Originals can hold GPS coordinates, so remove all
metadata before adding a web copy (`photos/` is git-ignored for this reason). Keep image alt text, captions, slide counts, and
image dimensions in sync when adding or replacing a photo. Run `quarto render`
and commit the source and `docs/` output.

## CV

The homepage CV link points to `delaSierra_CV.pdf`, which is included in the
Quarto resources. Replace this file when updating the CV, then render and commit
both the source PDF and `docs/delaSierra_CV.pdf`.

## Additional article PDFs

Put PDFs in `writing/` and add a `[PDF](filename.pdf)` link after the matching
citation in `writing/index.qmd`. DOI links are used for the new articles until
their PDFs are supplied; the existing PDF links remain in place.

## Links page and QR code

`links/index.html` is the link-in-bio page at `delasierra.io/links/`. It is a
hand-written HTML file, not a Quarto page, so it has no site menu and loads
fast on phones; Quarto copies the `links/` folder into `docs/` as a resource.
Edit the cards and icons in that file directly, then run `quarto render`.

The QR code (`links/qr-delasierra-links.svg` for print, `.png` for everything
else) points to `https://delasierra.io/links/`, so it never needs to change
when the links do. `l.html` also makes the short link `delasierra.io/l`,
which redirects to the links page.

Cover and card pictures are web copies in `links/` with camera metadata
removed; the originals stay in the git-ignored `photos/links/` folder.
