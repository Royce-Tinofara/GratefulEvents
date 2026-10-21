# Grateful Gatherings Gallery

Static website for the **Grateful Experience** — a night of thanksgiving worship. It lists upcoming
events with their flyers, the events hosted so far, a photo gallery, merch and contact details.

Plain HTML and CSS: no build step, no framework, no JavaScript.

> I want to create a website for grateful experience, you can be able to see the upcoming events, the event hosted and gallery of the grateful events hosted, the merch and some things which may be necessary, the link https://www.facebook.com/eleanabandamakombe  do not focus more on Eleana Makombe focus more on the Grateful experience page

This project was built with [Lovable](https://lovable.dev).

**Live app**: https://grateful-gatherings-gallery.lovable.app

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Home — hero, next stop, upcoming events, events hosted |
| `events.html` | Upcoming events with flyers and the full list of events hosted |
| `gallery.html` | Photo gallery |
| `merch.html` | Merch |
| `about.html` | About and contact |
| `404.html` | Shown for unknown URLs |
| `images/` | Logo, photos, event flyers and favicon |
| `css/styles.css` | Stylesheet loaded by every page |
| `css/tailwind.css` | Tailwind source used to compile `css/styles.css` |
| `robots.txt` | Search engine rules |

## Events

`events.html` and `index.html` list the upcoming events with their flyer, followed by the events
hosted. Every venue is written as *venue, city, country*.

| Event | Date | Venue |
| --- | --- | --- |
| Grateful Experience Zimbabwe | Sat 05 Dec 2026, 12:00 | Harare International Conference Centre, Harare, Zimbabwe |
| Grateful Unplugged | Fri 19 Feb 2027 | Bulawayo City Hall, Bulawayo, Zimbabwe |
| Grateful Experience Australia | 18 Sep 2026 | Westgate Indoor Sports, Altona North, Victoria, Australia |
| Grateful Experience 4.0 | 30 May 2026 | The International Convention Centre, Birmingham, United Kingdom |
| Grateful Experience 2025 | Dec 2025 | Harare International Conference Centre, Harare, Zimbabwe |
| Grateful Concert 3.0 | 31 May 2025 | The International Convention Centre, Birmingham, United Kingdom |
| Grateful Experience 2024 | Dec 2024 | Harare, Zimbabwe |
| Grateful Experience 2023 | Nov 2023 | Harare, Zimbabwe |

Flyers live in `images/` as `event-grateful-*.jpg`. Drop a new flyer in that folder and point the
card at it. When an event has no flyer yet, the card shows a "Flyer coming soon" panel.

The dates, venues and flyers were taken from the public listings for these events — the NdeipiZim
poster wall for the Harare night and the Eventbrite listings for the UK and Australia editions —
because Facebook does not allow automated reads of the profile. The Facebook page remains the
source of truth for anything not yet announced publicly.

## Viewing and deploying

Open `index.html` in a browser, or upload the whole folder to any static host — Netlify,
Cloudflare Pages, Vercel, GitHub Pages or plain shared hosting. Hosts that map `events.html` to
`/events` give clean URLs; every link in the site is relative, so the folder also works in a
sub-directory.

## Changing the styles

`css/styles.css` is the compiled stylesheet, generated from `css/tailwind.css` with the same theme
as the live site, so the local pages look like https://grateful-gatherings-gallery.lovable.app. It is
plain CSS and can also be edited by hand.

To change the theme or add utilities, edit `css/tailwind.css` and recompile:

```sh
npm install --no-save tailwindcss @tailwindcss/cli tw-animate-css
npx @tailwindcss/cli -i css/tailwind.css -o css/styles.css --minify
```

The Tailwind theme (fonts, colours, radius) lives in `css/tailwind.css`. Tailwind picks up the
class names straight from the HTML pages, so a new class only needs the stylesheet recompiling.
