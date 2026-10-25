# Head Tilt and Letter Mental Rotation

A dependency-free browser experiment designed for deployment on GitHub Pages.

## What it includes

- Adult/consent confirmation and anonymous participant ID
- Counterbalanced response-key mapping selectable by the researcher
- Randomized order of upright and 45-degree right-head-tilt blocks
- 4 practice trials and 40 experimental trials per posture
- Balanced orientations (0, 60, 120, 180 degrees), normal/mirrored versions, and 5 repetitions
- Millisecond reaction timing using `performance.now()`
- Trial-level CSV download with posture, orientation, version, accuracy, and RT
- No server-side data collection

## Deploy with GitHub Pages

1. Create a GitHub repository and upload `index.html`, `style.css`, and `experiment.js` to its root.
2. In the repository, open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)`, then save.
5. Open the Pages URL shown by GitHub after deployment.

GitHub Pages expects an entry file such as `index.html` at the top level of the publishing source.

## Run locally

Open `index.html` directly, or from this folder run:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Recommended lab procedure

- Use Chrome or Edge on a laptop/desktop with a physical keyboard.
- Keep browser zoom at 100% and close unrelated tabs/apps.
- Use full-screen mode where practical.
- Assign IDs such as P01-P14 and alternate the mapping selection across participants.
- Confirm head posture before each block and stop if the participant reports discomfort.
- Immediately save each downloaded CSV using the anonymous ID.

## Data note

The site stores completed trial rows in page memory and generates a local CSV download. Refreshing or closing the page before download loses the session. GitHub Pages is static hosting, so it does not receive experiment responses.

## Research note

Before collecting participants, obtain the required ethics approval, replace the brief consent language with institution-approved wording, pilot timing on the actual lab device, and define exclusion/data-cleaning rules in advance.
