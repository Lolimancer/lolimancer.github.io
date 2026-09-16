# Virtual Museum

A small walkable 3D gallery that runs entirely in the browser (Three.js). It has
three connected rooms — an entrance hall plus a north gallery and an east
gallery branching off it — so it's not just one box room, and there's a short
walk (with a turn) between each wing.

## Running it

Browsers block ES module imports and `fetch()` of local image files when you
open an HTML file directly (`file://...`), so serve the folder instead of
double-clicking it:

```bash
cd virtual-museum
python3 -m http.server 8000
```

Then open **http://localhost:8000** in your browser and click "CLICK TO ENTER".

(Any other local static server works too — `npx serve`, VS Code's
"Live Server" extension, etc.)

## Controls

* **Mouse** — look around
* **W A S D** / arrow keys — walk
* **Click** a painting — step up for a closer look, with its title shown
* **Click again**, or **Esc** — step back and keep walking

## Swapping in your own pictures

Just replace the files in the `images/` folder. They're named:

```
images/img1.jpg
images/img2.jpg
...
images/img9.jpg
```

Overwrite any of them (keep the same filename) and refresh the page — that
picture updates everywhere it's used in the museum. There are 27 frames on
the walls but only 9 image slots; each image is reused on a few frames
(`img1.jpg` on frame 1, 10, 19..., `img2.jpg` on frame 2, 11, 20..., etc.),
so replacing one file changes several frames at once.

Tips:

* Portrait images around a 3:4 ratio (e.g. 900×1200) fit the frames best.
Other ratios still work, just slightly stretched.
* JPG or PNG both work.
* If a file is missing or fails to load, that frame shows a soft
placeholder instead of breaking.

### Using more than 9 images

Open `index.html` and near the top of the `<script type="module">` block
change:

```js
const IMAGE\\\_COUNT = 9;
```

to however many `imgN.jpg` files you're providing, then add the matching
files to `images/`. You can also edit the `TITLES` array just below it to
change the captions shown when a painting is in focus.

### Changing the room layout / where paintings hang

The building is defined by two small data tables in `index.html`:

* `wallDefs` — the walls themselves (position, length, and an optional
doorway `gap`)
* `paintingDefs` — one entry per frame (`x, y, z` position, `nx, nz` facing
direction, and width/height)

Both are plain arrays, so you can add a room by adding wall segments and a
doorway gap, then add more `paintingDefs` entries along its walls.

