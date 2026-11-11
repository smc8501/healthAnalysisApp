# Health Analysis App

A small, browser-based health analysis demo. It lets users enter patient details and view counts by condition and gender, and look up basic information about diabetes, thyroid conditions, and high blood pressure.

This is a front-end demonstration, not a medical tool. Patient entries are kept only in the current page session and are not saved or sent to a server. Condition descriptions are informational and should not be used as a substitute for professional medical advice.

## Features

- Add a patient's name, gender, age, and condition.
- View an in-page patient total and breakdown by condition and gender.
- Search for information on supported conditions, including symptoms, prevention, and treatment.
- Open a contact page with a demonstration form.

## Project files

The app files are in [`healthAnalysis/`](healthAnalysis/):

- `index.html` — patient entry, report, and condition search page.
- `health_analysis.js` — browser-side patient summary and condition lookup logic.
- `health_analysis.json` — condition information used by the search feature.
- `health_analysis.css` — shared styling.
- `health_contact.html` — contact form demo.
- `*.jpg` — condition illustrations.

## Run locally

The condition search loads a local JSON file with `fetch`, so serve the directory over HTTP rather than opening the HTML file directly. From the repository root, run:

```bash
cd healthAnalysis
python3 -m http.server 8000
```

Then visit <http://localhost:8000> in your browser. You can also use another local static-file server.

There is no build step, package manager, or backend service required.

## Limitations

- Patient entries are stored in memory and disappear when the page is reloaded.
- The contact form displays a confirmation alert; it does not transmit a message.
- The condition lookup only matches the listed condition names.
- The included health content is a simple demo and is not medical advice.
