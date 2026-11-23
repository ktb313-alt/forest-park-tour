# Forest Park Trail Tour

A self-guided 180° VR tour of the Forest Park trail. It runs in any modern browser, and in VR headset browsers (Meta Quest, Apple Vision Pro).

## Put it on GitHub Pages

1. On github.com, create a new **public** repository (for example `forest-park-tour`).
2. Upload in six batches from the **GitHub-upload-batches** folder next to this one. For each of `batch-1` to `batch-6`, choose **Add file → Upload files**, open the batch folder, select everything inside it, drag it onto the page, then choose **Commit changes**. Each batch is under 100 MB, and batches 2 to 6 each hold a `walk` folder that GitHub merges into one.
   (On a Mac, press Cmd+Shift+. in Finder to see `.nojekyll` in batch-1. The site works without it.)
3. Check that the repository has `index.html` at the top level, plus `front/` and `walk/` folders.
4. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, then **Save**.
5. After a minute or two the tour is live at `https://<your-username>.github.io/<repository-name>/`.

## What's in here

- `index.html`: the tour (the 3D library loads from cdnjs.cloudflare.com).
- `front/`: the view at each of the 9 stops (2048×2048, front half of the 360° frame).
- `walk/`: the walking video between stops, 2048×2048 at 14 Mbps, in 9.5 MB pieces that play back in order.

The site is about 480 MB. GitHub Pages allows sites up to 1 GB and about 100 GB of downloads a month, which is roughly 200 full walk-throughs.

To change a stop's name or note, edit the `STOPS` list near the top of the script in `index.html`.
