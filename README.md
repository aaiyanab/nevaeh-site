# Nevaeh — Creative Branding Studio

Static one-page site. No build step, no dependencies — plain HTML, CSS, and a little JavaScript.

## Files

```
index.html            The entire site (markup, styles, scripts)
images/               Logo, brand board, and client images
favicon.png           Browser tab icon
apple-touch-icon.png  Icon for phone home screens
og-image.jpg          Preview image when the link is shared
```

## Local preview

Double-click `index.html`, or serve it properly:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Note: the contact form only submits successfully from a real domain. Locally it will
show an error — that's expected.

## Deploy

Push to GitHub, then import the repo at vercel.com. Vercel detects a static site
automatically; leave every build setting blank. Full walkthrough in the chat.

## Contact form

Runs on Formspree (form ID `mgogdove`). Submissions land in the inbox linked to
that Formspree account and are archived in the Formspree dashboard.

To point the form at a different account, change one line near the bottom of
`index.html`:

```js
const FORMSPREE_ID = 'mgogdove';
```

Leave it as an empty string and the form falls back to opening the visitor's
email app instead.

## Common edits

| What to change | Where |
| --- | --- |
| Prices, package contents | Search `Signature Packages` in `index.html` |
| À la carte rates | Search `À La Carte Services` |
| Email address | Search `hello@nevaeh.studio` (appears twice) |
| Colors | The `:root` block at the top of the `<style>` section |
| Client images | Replace files in `images/`, keeping the same filenames |
| Social preview URL | Search `YOUR-DOMAIN` near the top |
