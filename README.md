# ADA coloring template library

A folder of SVG templates plus `catalog.json`. Host it anywhere that serves static files over HTTPS
(GitHub Pages is free). In the ADA app: Profile → Coloring template library → paste the address.

## Publish on GitHub Pages
1. Create a new public repository (for example `ada-templates`) and upload the contents of this folder
   (`catalog.json` and the `svgs/` folder) to the repository root.
2. Repository → Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
3. After a minute your library is at `https://<your-user>.github.io/ada-templates`.
   Check that `https://<your-user>.github.io/ada-templates/catalog.json` opens in a browser.

## Add a template
1. Add an SVG to `svgs/`. Use only closed shapes: `path`, `circle`, `ellipse`, `rect`, `polygon`, `polyline`
   (optionally inside `<g>`). Every closed shape becomes a region the user can color. Draw a full-size
   background shape first so the background can be colored too. Use `viewBox="0 0 400 400"`.
   Colors, styles, scripts and links in the file are ignored by the app.
2. Add an entry to `catalog.json`:
   `{"id":"my-id","title":"My Template","category":"Nature","tags":["tree"],"svg":"svgs/my-id.svg","license":"CC0","source":"you"}`
3. Commit and push. The app picks it up the next time the Coloring Book opens.

## Licensing
Only add art you made or that is public domain / CC0, or that you have written permission to redistribute.
Record the license and source in the catalog entry. The templates in this folder were generated for ADA and are CC0.
