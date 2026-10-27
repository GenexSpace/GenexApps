# Genex internal app directory

Open **index.html** in a modern browser. No build, installation, or server is needed.

The page includes all nine apps in a Clean style: neutral surfaces, consistent cards, generated icons, search, category filters, keyboard navigation, and a responsive mobile layout. Icons and CSS are embedded in the HTML. Google Fonts enhance the typography when online; system fonts work offline.

## Add app links

Search `index.html` for `const APP_LINKS` and paste the full URLs between the quotes:

```js
const APP_LINKS = {
  hrm: '',         // HRM Portal
  policy: '',      // Policy
  knowledge: '',   // Knowledge Base
  writeassist: '', // WriteAssist App
  meeting: '',     // Meeting Room
  tasks: '',       // Task Tracker
  inventory: '',   // Inventory
  social: '',      // SocialMedia Manager
  scribe: ''       // Scribe Tool — school program report generator
};
```

Configured apps open in a new tab. Apps with an empty URL show a “link coming soon” message. Only HTTP and HTTPS links are accepted.

Press `/` to focus search. Press Escape in search to clear it. The app details dialog also closes with Escape.

Icon generation prompts and source information are recorded in `assets/icon-prompts.md`.

`assets/clean.css` is the editable stylesheet source. After changing it, replace the contents of the inline `<style>` block in `index.html` with the updated CSS to keep the standalone file in sync.

## Hosting

The page works on GitHub Pages from the root of the default branch. `.nojekyll` keeps the site static, with no build step.
