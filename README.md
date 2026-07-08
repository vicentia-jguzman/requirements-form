# requirements-form

The **public** static form for the VMS requirements interview. Hosted free on
GitHub Pages (no build/deploy credits — question edits are just pushes).

- `index.html` — the form. `?form=<id>` opens one topic; no param shows the menu.
- `questions/forms.json` — the list of topics shown on the menu.
- `questions/<id>.json` — the questions for one topic.

**No secrets live here.** The access code and answer storage are handled by a
Google Apps Script web app (see the private `requirements-hub` repo notes).
Answers post to that endpoint (`ENDPOINT` in `index.html`) and land in a Google
Sheet. Managers only need the Pages URL + the access code.

## Setup (one time)
1. Settings → Pages → Deploy from a branch → `main` / root.
2. Paste the Apps Script `/exec` URL into `ENDPOINT` in `index.html`.
