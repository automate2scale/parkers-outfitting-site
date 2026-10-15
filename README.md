# Parker's Outfitting website

The whole site is one file. `site.html` and `index.html` are identical copies of it.

| File | Used by |
|---|---|
| `site.html` | The GHL page at go.tennesseeoutdoorretreats.com/home. The loader there uses `data-page="site"`. |
| `index.html` | Any static host, such as Netlify or GitHub Pages, and the future parkersoutfitting.com. |
| `images/` | The site photos, as WebP at 480, 800 and 1200 px wide. The hero also has an 1800 px version. |
| `netlify.toml` | Netlify settings, used only if the site is hosted on Netlify. |
| `GHL-home-head-code.html` | Code for the GHL page head. |

## How it works

Each page is a `<div class="page" data-page="...">` block inside the one file. A small script shows the block that matches the URL hash and updates the page title and meta description.

| Page | Link |
|---|---|
| Home | `#home` |
| Waterfowl Hunts | `#waterfowl-hunts` |
| Lodging | `#lodging` |
| License Info | `#license-info` |
| Gallery | `#gallery` |
| FAQ | `#faq` |
| Guest Info | `#guest-info` |
| Book | `#book` |

All CSS is scoped under `#po-page`, so it does not clash with GHL styles. Images load from jsDelivr through `srcset`, so phones get the smaller files.

## Making a change

1. Edit `index.html`.
2. Copy it over `site.html` so the two stay identical.
3. Commit both files.
4. Clear the CDN cache by opening `https://purge.jsdelivr.net/gh/automate2scale/parkers-outfitting-site@main/site.html`.

## GHL loader

The GHL page holds one Custom Code element containing the loader snippet. It fetches
`https://cdn.jsdelivr.net/gh/automate2scale/parkers-outfitting-site@main/site.html` and renders it in `#po-root`.

Built and maintained by Automate2Scale.
