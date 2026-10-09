# VASRÉ — The Art of Indian Elegance

Single-page saree boutique website.

- `index.html` is fully self-contained: all styles, scripts and product photos are inside the file.
- The banner opens with a saree-drape reveal: a red-and-gold paisley saree slides across the screen and is lifted away from the corner to reveal the banner. The same reveal plays each time the banner photo changes.

## Run it
Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Showroom video
The walk-through video currently streams from Higgsfield. To host it yourself, add it as `assets/showroom.mp4` and change the `src` of the `<video id="vid">` tag in `index.html` to `assets/showroom.mp4`. For the smoothest scrubbing, encode every frame as a keyframe:

```bash
ffmpeg -i showroom.mp4 -c:v libx264 -g 1 -crf 22 -pix_fmt yuv420p -movflags +faststart -an assets/showroom.mp4
```

## Deploy on GitHub Pages
Settings → Pages → Source: `main` branch, `/ (root)`.
