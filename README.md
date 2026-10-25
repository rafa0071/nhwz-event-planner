# Sustainability Week Planner

A lightweight event planner for Sustainability Week Zurich, written in plain HTML, CSS and JavaScript. No frameworks, no build step.

**Live demo:** https://rafa0071.github.io/nhwz-event-planner/

## Features

- **Programme**: all events, browsable by day, with filters for campus, category and language
- **My Week**: saved events grouped by day, stored in the browser (`localStorage`), with a warning when two saved events overlap
- **Event detail**: cancellation label, embedded Google Map, address and registration link
- Responsive from 360 px phones to desktop, keyboard accessible, automatic light and dark mode

## Run it

Open `index.html` in any modern browser. That's it.

To serve it locally instead:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Data

All events live in the `EVENTS` array at the top of the script. Each event has:

| Field | Example |
|---|---|
| `id` | `"e01"` |
| `day` | `"2027-03-01"` (ISO date) |
| `start`, `end` | `"09:30"`, `"10:30"` |
| `title`, `summary` | text |
| `campus`, `room`, `address` | `"ETH Zentrum"`, `"HG F 30"`, `"Rämistrasse 101, 8092 Zürich"` |
| `category` | `"Climate"` |
| `language` | `"EN"` or `"DE"` |
| `cancelled` | `true` / `false` |
| `url` | registration link |

Filters, days and labels are generated from the data, so new campuses, categories or days appear automatically. The current events are sample data for demonstration.

## License

MIT. No third-party code; fonts are served by Google Fonts under the SIL Open Font License.
