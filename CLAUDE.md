# CLAUDE.md

**Read [wd42-hq/CLAUDE.md](https://github.com/vadorg/wd42-hq/blob/main/CLAUDE.md) first:** working rules, map, product decisions. This file only covers this repo.

## Project

wd42-assets: a **public** repo. Media for template buyers and video previews for the site. Served via jsDelivr.

## Language

Everything in this repo is public, so everything is in English: README, CLAUDE.md, file names, descriptions, commit messages, and any text inside files (for example SVG comments). No Cyrillic.

## Structure

```
templates/<name>/<file>   template assets for the buyer (images, video, 3D)
previews/<name>.mp4       video preview for the site card
```

`<name>` matches the folder in `wd42-content/templates/`.

## Key decisions

- Media only. No prompts, template code, meta.md, keys or personal data: everyone can see this repo
- Files are added by the `assets` or `publish` script from wd42-content. Until the scripts exist, add them by hand following the same rules
- Max file size 20 MB. Images: svg, png, jpg, webp or avif. Video: mp4 (H.264). 3D: glb (preferred), gltf with its bin, usdz, obj, fbx, stl, ply, drc. SVG, gltf and obj files must contain no Cyrillic text
- Always link with a commit: `https://cdn.jsdelivr.net/gh/vadorg/wd42-assets@<commit>/templates/<name>/<file>`
- Never rewrite history (no force push, no rebase of main): sold prompts link to commits
- Never delete or overwrite a file. A new version gets a new file name
