# Render deployment guide

This project is plain HTML, CSS and JavaScript. Deploy it as a **Render Static Site**; it does not need a web service, build step, Python runtime, API key or database.

## Dashboard setup

1. Push `index.html`, `render.yaml` and the documentation to the root of a GitHub repository.
2. In Render, choose **New + → Static Site** and connect the repository and branch.
3. Set the **Publish Directory** to `.` (the repository root).
4. Leave the **Build Command** empty.
5. Create the site and wait for the deployment URL.

Alternatively, create a Render Blueprint from the repository and let Render read `render.yaml`. The Blueprint configures a static site published from `.` with no build command.

## Verify after deployment

- Open the generated `onrender.com` address in a private browser window.
- Check the profile, quiz, pathway save, college filters, what-if comparison, quest progress and demo Mentor.
- Check a narrow/mobile viewport and the browser console.
- Refresh and confirm browser-local persistence on that same browser/device.
- Use **Reset demo data** only when you want to clear that browser's saved demo state.

## Troubleshooting

- If the page is not found, confirm `index.html` is at the repository root and the publish directory is `.`.
- If an old page appears, trigger a fresh deploy and hard-refresh.
- If a feature fails, inspect the browser console. This app has no server logs or build output.
- Do not upload `.env` files, API keys or personal student data. No external service credentials are used.
