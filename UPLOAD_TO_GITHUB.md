# Publish the Ipswich project to GitHub

Recommended repository name: `ipswich-ai-data-centre-gis`

## GitHub Desktop

1. On GitHub, create a **public** empty repository named `ipswich-ai-data-centre-gis`.
2. Do not add a README, licence or `.gitignore` during creation; they are already included.
3. Unzip this folder.
4. Open GitHub Desktop and choose **File -> Add local repository**.
5. Select the unzipped `ipswich-ai-data-centre-gis` folder. If prompted, choose **Create a repository**.
6. Commit the files and publish to `Hope328/ipswich-ai-data-centre-gis`.
7. Ensure **Keep this code private** is not selected.

## How the finished map is displayed

The repository already contains two versions of Map 1:

- `docs/assets/ipswich-study-area-map.png` - displayed directly in the README and website.
- `maps/Map-1-Study-Area-and-Infrastructure.pdf` - full-resolution version opened when a viewer clicks the README image.

The root `README.md` uses this Markdown pattern:

```markdown
[![Ipswich study area and infrastructure map](docs/assets/ipswich-study-area-map.png)](maps/Map-1-Study-Area-and-Infrastructure.pdf)
```

This lets a recruiter see the map immediately without downloading anything, while preserving a clickable high-resolution PDF.

## Enable the project website

1. Open the repository on GitHub.
2. Go to **Settings -> Pages**.
3. Choose **Deploy from a branch**.
4. Select branch `main` and folder `/docs`.
5. The expected address is `https://hope328.github.io/ipswich-ai-data-centre-gis/`.

The website displays the real Map 1 across the page. Clicking it opens `docs/assets/ipswich-study-area-map.pdf`.

## Add the next finished map

For each new map:

1. Export a web PNG at approximately 2,500-3,500 pixels wide.
2. Export a full-resolution PDF.
3. Place both in `docs/assets/` for the website.
4. Keep another PDF copy in `maps/` for repository organisation.
5. Add the PNG near the top of `README.md` and link it to the PDF.
6. Replace the relevant unchecked deliverable with `[x]` only after the output is complete.
