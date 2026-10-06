# Parker's Outfitting: pasting the site into GHL

Each `.html` file is one page and is self-contained. The CSS, fonts, schema, logo and scripts are all inside the file.

## Setup for each page (10 total)

1. In **Sites → Websites**, create a page with the path shown in the comment at the top of its file.
2. Add one full-width **section**. Set its padding to 0 and remove any row or column padding.
3. Drop in a **Custom Code** element and paste in the whole file.
4. Open **Page settings → SEO** and paste the Title and Description from the comment at the top of the file.
5. Turn off the GHL default header and footer for the page. Each file has its own.

| File | Page path |
|---|---|
| home.html | `/` (set it as the home page) |
| reelfoot-lake-duck-hunts.html | `/reelfoot-lake-duck-hunts` |
| private-ground-duck-hunts.html | `/private-ground-duck-hunts` |
| lodging.html | `/lodging` |
| rates-packages.html | `/rates-packages` |
| hunt-info.html | `/hunt-info` |
| gallery.html | `/gallery` |
| faq.html | `/faq` |
| guest-info.html | `/guest-info` |
| book.html | `/book` |

The internal links depend on those exact paths. If you change a path, change it in every file.

## Before going live

- **Logo.** The logo is embedded at the bottom of each file in a `LOGO` constant. To serve it from the GHL Media Library, upload it there and replace the `data:` string with the media URL.
- **Booking calendar.** The calendar on `book.html` is the widget from the Tennessee Outdoor Retreats sub-account. Before launch, check that its branding and confirmation emails say Parker's Outfitting. Cell phone should be a required field.
- **Photo slots.** The striped boxes are placeholders: home, Reelfoot, private ground, lodging, and nine on gallery. Replace each one with an `<img>`, using the suggested filename and alt text shown in the slot.
- **301 redirects.** Point `/corporate-retreats/` and the other old WordPress URLs at the closest new page.
- **Google Business Profile.** Update it to match the site.
