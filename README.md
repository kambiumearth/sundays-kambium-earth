# Wilderness Skills Community Sundays: static page

A plain HTML and CSS version of sundays.kambium.earth. There's no build step: open `index.html` in a browser to preview it.

## Photos (in `images/`)

| File | What goes there |
|---|---|
| logo.webp | Kambium logo (transparent background) |
| favicon.png | Small square icon |
| hero.jpg | Hands holding the tinder bundle (current hero) |
| glance.jpg | Tall photo: adults and children together at the fire |
| sundays-wide.jpg | Wide photo: children on the stick shelter |
| families.jpg | Family circle |
| details.jpg | Gear or packed lunch on a rainy day |
| joshua.jpg / melina.jpg | Square portraits |
| joshua-melina.jpg | The black and white photo of you both |
| band.jpg | Wide photo: hands at the fire |

Extra photos already uploaded and free to use: card-fire.jpg, card-bowdrill.jpg, card-group.jpg, smoke.jpg.

If a file is missing, a striped box with a label shows in its place. Keep each photo under about 400 KB (about 2000px wide is plenty).

## Adding or swapping a photo

1. Upload the photo into `images/` (Add file → Upload files) with the exact file name from the table above. Uploading a file with the same name replaces the old one.
2. To use a different name, find the matching `<img src="images/...">` in `index.html` and change the name there.
3. To add an extra photo anywhere, paste this where you want it, between two sections or inside one:

```html
<figure class="photo wide-photo"><img src="images/your-photo.jpg" alt="Short description of the photo"></figure>
```

## Adding video

**Option 1: your own video file.** Export a short clip, under about 20 MB (720p MP4, 30 to 60 seconds), and save it as `video/sundays.mp4` with a still frame saved as `images/video-poster.jpg`. Then paste:

```html
<figure class="photo wide-photo">
  <video src="video/sundays.mp4" poster="images/video-poster.jpg" controls playsinline preload="metadata" style="width:100%;height:100%;object-fit:cover"></video>
</figure>
```

For a silent looping background clip, as in a hero, swap `controls` for `autoplay muted loop`.

**Option 2: YouTube or Vimeo.** Upload the video there, copy the embed link and paste:

```html
<figure class="photo" style="aspect-ratio:16/9">
  <iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" title="Community Sundays" allow="fullscreen" style="width:100%;height:100%;border:0"></iframe>
</figure>
```

GitHub refuses single files over 100 MB, so anything longer belongs on YouTube or Vimeo.

## How it's hosted

- Repository: github.com/kambiumearth/sundays-kambium-earth, published with GitHub Pages from the `main` branch.
- The `CNAME` file holds the address `sundays.kambium.earth`. Don't delete it.
- DNS at Infomaniak: a CNAME record `sundays` points to `kambiumearth.github.io`.
- To change anything: open the file on GitHub, click the pencil, edit and "Commit changes". The live page updates in about a minute.

## Editing

- All text is in `index.html`.
- All colours and spacing are in `style.css`, in the `:root` block at the top.
- Every booking link goes straight to Ticket Tailor ticket selection for 29 November (where the Winter Arc bundle also shows). It is `https://events.kambium.earth/checkout/new-session/id/9314775/chk/a66d615f0cc90706e5b39bc8201bd95f/`. Search for `new-session` to change them all at once.
- To add a testimonial, search `index.html` for "To add a second" and copy the q-card block next to it. Use real quotes only.
