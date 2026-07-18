# Trite Site

Trite Site was a satire/humor blog that used to live at [trite.site](https://trite.site). The
original content was lost, so this repo restores it from the [Wayback
Machine](https://web.archive.org/web/20180902000000*/trite.site) and rebuilds it as a static
[Astro](https://astro.build) site, deployed via GitHub Pages.

All 10 archived posts and the About page were recovered from Wayback Machine snapshots (captured
2018-08 to 2018-12) and converted to Markdown. Images and a few in-post links still point back at
their `web.archive.org` snapshot URLs, since the original media files weren't separately archived.

## Structure

```text
/
├── src/
│   ├── content/blog/     restored posts, one Markdown file per post
│   ├── layouts/          shared page layout
│   └── pages/            home, about, and per-post routes
└── public/CNAME          custom domain (trite.site) for GitHub Pages
```

## Commands

| Command           | Action                                       |
| :----------------- | :------------------------------------------- |
| `npm install`       | Install dependencies                         |
| `npm run dev`       | Start local dev server at `localhost:4321`   |
| `npm run build`     | Build production site to `./dist/`           |
| `npm run preview`   | Preview the build locally                    |

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site with
`withastro/action` and publishes it to GitHub Pages. The `public/CNAME` file points the custom
domain `trite.site` at the deployed Pages site once DNS is configured.
