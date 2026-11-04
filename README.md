# CrossPoint Calendar

A web generator for e-ink calendar images for [CrossPoint Reader](https://crosspointreader.com/), made for the Xteink X4 Pro (480 × 800).

**Use it here: [aendom.github.io/crosspoint-calendar](https://aendom.github.io/crosspoint-calendar/)**

*[Leer en español](README.es.md)*

![The generator](docs/preview.png)

Pick a design, a year and, if you want, a month. Then download the image and copy it to your reader. Everything runs in your browser: there is no server, no account and nothing to install.

## What you can make

- **Full year**: all 12 months on one screen.
- **One month**: the month large, with the next two months below.
- **Full year + 12 months (ZIP)**: the year image and all 12 month images in one download.

Calendars come in **Spanish or English**, with the week starting on **Monday or Sunday**. Sundays are bold.

## Put it on your reader

1. Download the **BMP**.
2. Copy it to the root of the SD card and name it **`sleep.bmp`**.
3. On the reader, go to **Settings → Display → Sleep Screen** and choose **Custom**.

That's it. It shows every time the reader goes to sleep.

### Change the month from the reader

Download the ZIP and copy the 12 month images to a folder on the SD card, for example `/calendar`. At the start of each month, open the right image in **Browse Files** and set it as the sleep screen from the reader itself. You don't need a computer or Wi-Fi.

Don't put the month images in the `/.sleep` folder. CrossPoint picks a random image from that folder, so you'd get the wrong month.

## Why BMP

The X4 Pro screen shows 4 levels of gray, and CrossPoint draws 2-bit BMP files directly, with no conversion. The generator writes exactly that format (about 94 KB per image), so the preview on the page is exactly what the reader shows. PNG is there for viewing or sharing the calendar.

## Design notes

- **Fonts:** [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) and Plex Sans Condensed for the year design, where the condensed figures give the narrow date columns room. [Inter](https://fonts.google.com/specimen/Inter) for the month design.
- **No gray text.** Weekday labels are solid black because light gray washes out on e-paper.
- **Every month block has six rows**, so the rhythm of the year grid stays the same from month to month.

## Run it yourself

The whole generator is one file, `index.html`. Open it in any browser, or fork this repo and turn on GitHub Pages (**Settings → Pages → Deploy from a branch → `main` / root**).

## License

MIT. The fonts are loaded from Google Fonts under the SIL Open Font License.

Not affiliated with the CrossPoint Reader project.
