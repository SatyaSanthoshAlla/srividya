# GramPath AI — GitHub Pages Prototype

A responsive, static web app for Telugu + English career discovery for students in Classes 9–12.

## Deploy on GitHub Pages
1. Create a new public GitHub repository named `grampath-ai` (or another name).
2. Upload `index.html`, `manifest.webmanifest`, and `sw.js` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, then click **Save**.
6. Wait for the deployment and open the URL shown in the Pages section.

## Run locally
Run `python -m http.server 8000` from this folder, then open `http://localhost:8000`. A service worker requires localhost or HTTPS; opening the HTML file directly will still show most features.

## Features
- Profile form and up-to-three interests
- Transparent rule-based career matching
- Personalized pathway and saved checklist progress
- Official portal directory (not live vacancy data)
- Teacher/facilitator roster
- English/Telugu UI label switching
- Browser speech input/output where supported
- LocalStorage and JSON export
- Basic offline PWA caching

## Important limitations
This is a front-end prototype, not a production AI system. There is no LLM or live data integration. Opportunity cards link to official portals; they do not verify current eligibility, deadlines, or openings. Voice support varies by browser/device. Data stays in the current browser and does not sync between users/devices.

## Next production stage
Add a Spring Boot API, authentication and role-based access, a PostgreSQL database, and a Python/FastAPI retrieval service. Ground answers in approved source documents with source URLs and last-verified timestamps. Keep eligibility rules deterministic and reviewable. Do not put API keys in GitHub Pages JavaScript; route secret-bearing calls through a backend.
