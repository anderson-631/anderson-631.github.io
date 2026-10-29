# Anderson He — Engineering Portfolio

Plain HTML + CSS. No build step: what's in this folder is the website.

```
index.html       home page (project grid)
stackdaq.html    one page per project
to1.html
style.css        all styling; colors and font are at the top
images/          grid thumbnails
models/          .glb files for the 3D viewers
```

## Preview on your computer

The 3D viewers won't load if you just double-click `index.html` (browsers block
loading local model files that way). Run a tiny local server instead, from this folder:

```
python -m http.server
```

then open http://localhost:8000. (Or use the "Live Server" extension in VS Code.)

## Replace the TO1 thumbnail

Save your screenshot as `images/to1_thumbnail.png`, overwriting the placeholder.
If you save it as a different name or format (e.g. `.jpg`), update the `src` of
that card in `index.html`.

## Add a project

1. Put the model in `models/` and a thumbnail in `images/`.
2. Copy `stackdaq.html` to `newproject.html`. Change the `<title>`, heading, meta line,
   the `src` on `<model-viewer>`, the paragraphs, and the skills list.
3. In `index.html`, copy one `<li>` card, point it at the new page and image, and
   place it before the "To be continued" card.
4. In every project page, add a link to the new project under **Other Projects**
   (and add links to the others on the new page).

## 3D viewer settings

Each viewer is a `<model-viewer>` tag. Useful attributes:

- `camera-orbit="0deg 55deg auto"`: starting angle (spin, tilt, distance; distance can be a % like `80%` to zoom in)
- `auto-rotate`: delete it to stop the slow spin
- Docs: https://modelviewer.dev/docs/
