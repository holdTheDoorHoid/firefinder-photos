# Firefinder mirrored photos

This folder is a mirror of photos linked from fire-lookout tower pages on
[Firefinder](https://holdthedoorhoid.github.io/firefinder/), an open-source map of every US
fire lookout. It is generated and kept up to date by `pipeline/mirror_photos.py` in the
[Firefinder repository](https://github.com/holdTheDoorHoid/firefinder), and served from here so
the original sites are not burdened and pages load reliably.

## What is here

```
photos/<hh>/<sha1>.webp      full-size copy, long side capped, ~quality 72
photos/<hh>/<sha1>.t.webp    thumbnail, long side <= 360px, ~quality 60
```

Files are named by the content hash of the processed image, so a photo reused across
multiple source sites or multiple towers is stored once. Which source URL maps to which
file, plus each photo's size, pixel dimensions, and processing status, is recorded in
`data/photos_manifest.json` in the Firefinder repository (not duplicated here).

Every image has been re-encoded to WebP, re-oriented from its original EXIF orientation tag,
converted to sRGB, and stripped of embedded metadata (EXIF, XMP, ICC profile, and anything
else that might identify the person or device that took the photo). Nothing else about the
photo has been altered.

## Licensing — read this before reusing anything here

**These photos are not covered by Firefinder's own licenses.** Firefinder's code is
GPL-3.0, its database is ODbL 1.0, and its own written history is CC BY-SA 4.0 — none of
that applies to the images in this folder. Each photo keeps its own original rights, owned
by whoever took it or whoever the source site credits. Firefinder mirrors them (resized,
re-encoded, and with metadata stripped, as described above) with credit, so that a scattered and
often disappearing record of lookouts is not lost. Mirroring is not a claim to any rights over
them, and we have not obtained permission for most of them: if a photo is yours, see below.

Every photo's credit (photographer and/or source site) is recorded in
`data/photos_manifest.json` and shown next to the photo on its Firefinder tower page, with a
link back to the page it was mirrored from. Always check the credit line and source link
before reusing a photo from here.

## Ask for a different credit, or ask for a photo to be removed

If a photo here is yours, or you represent whoever took it, Firefinder will credit it the
way you want or remove it — promptly, no questions asked.

Open an issue titled **"Takedown: `<tower name>`"** at:

**https://github.com/holdTheDoorHoid/firefinder/issues/new**

Include a link to the Firefinder tower page the photo appears on (or the tower's name) and
which photo you mean (its caption or credit line is enough). No technical detail is needed,
just enough for us to find it.
