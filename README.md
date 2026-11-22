# Premiere website

The landing page, privacy policy and terms of service for the Premiere Discord bot. It's plain HTML and CSS, so it runs on GitHub Pages with no build step.

## Before publishing

Replace these placeholders:

| Placeholder | File | Replace with |
|---|---|---|
| `YOUR_APPLICATION_ID` | `index.html`, in the `discord-application-id` meta tag near the top | Your Application ID (Discord Developer Portal → General Information) |
| `CONTACT_EMAIL` (two places each) | `privacy.html`, `terms.html` | An email address or support server invite people can use to reach you |

The invite buttons read the application ID from the meta tag, so you only set it once. If you'd rather not rely on JavaScript, also replace `YOUR_APPLICATION_ID` in the two button links in `index.html`.

The privacy policy and terms describe exactly what the bot stores and does. Read them before publishing, since you're the one responsible for them. They're a starting point, not legal advice.

## Publish on GitHub Pages

1. Create a public repository and put these files at its root.
2. In the repository, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
3. After a minute the site is live at `https://<your-username>.github.io/<repository>/`.
4. In the Discord Developer Portal, under **General Information**, set **Terms of Service URL** to `…/terms.html` and **Privacy Policy URL** to `…/privacy.html`.

## Files

- `index.html`: landing page with invite buttons, example alerts and commands
- `privacy.html`, `terms.html`: the policies
- `style.css`: shared styles
- `assets/`: logo, favicon, link-preview image (`og.png`) and example alert cards
- `.nojekyll`: tells GitHub Pages to serve the files as they are
