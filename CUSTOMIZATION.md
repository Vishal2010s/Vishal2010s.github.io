# Step 2 — Design and customization

This portfolio uses plain HTML, CSS and a small amount of JavaScript. There is no installation or build step. Open `index.html` in your browser to preview it.

## Understand the three files

* `index.html` holds your content: introduction, six project cards, skills, experience and contact.
* `css/style.css` controls colors, spacing, cards and responsive layouts. Start with the `:root` color tokens.
* `js/script.js` opens/closes the mobile menu and updates the copyright year. Content remains available without it.

`assets/favicon.svg` is the browser-tab icon. The hero illustration is inline SVG, so no external image or font service is required. `.nojekyll` tells Pages to serve this static site directly.

## 1. Make your first edit

Find `Hi, I’m` in `index.html`, edit the introduction, save, then refresh your browser. HTML describes the content; CSS describes its appearance. Try changing `--accent` in the CSS to understand how a design token affects the whole site.

## 2. Update a project

Find its title inside a `<article class="project">` block. Edit the title, paragraph, technology tags and links there. A demo link's `href` is its real destination; its `aria-label` describes the destination to screen-reader users. Keep both in sync. New-tab links use `rel="noopener noreferrer"`.

`data/projects.json` is a reference snapshot of the original projects, not a runtime data source. Editing it alone does not update the page. Keeping cards in HTML makes the work visible without JavaScript. If you update a URL, update the snapshot too to keep it useful as a reference.

All six projects now have Streamlit demo links. The five original URLs are preserved exactly; the Health Insurance Policy Assistant URL was supplied by the owner. Update a demo only with its verified address.

## 3. Add your résumé

1. Save the final PDF as `assets/Vishal-S-Resume.pdf`.
2. Find `<span class="resume-placeholder">Résumé — coming soon</span>`.
3. Replace that span with:

```html
<a class="button secondary" href="assets/Vishal-S-Resume.pdf" download>Download résumé ↓</a>
```

Preview the PDF and confirm the download before publishing. No broken PDF link is included in the current site.

## 4. Add contact and career details

The GitHub profile comes from the original page. No email, LinkedIn URL, employer, job dates or achievements have been invented. Add your verified email using `href="mailto:your-real-address"` and your exact LinkedIn URL when ready; replace the contact placeholder text. Add factual role titles, employer names and dates in the experience section. The 11-year experience statement was retained from the original page; review it before deployment.

## 5. Deploy with GitHub Pages

The repository must be named **Vishal2010s.github.io**, without a trailing dot. The public address is **https://vishal2010s.github.io/**.

1. Review the changed files and merge the portfolio redesign pull request into `main`, or upload these files preserving `css/`, `js/` and `assets/` folders. `index.html` must be at the repository root.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then **Save**. If the repository already uses a custom Pages Actions workflow, inspect that workflow before switching sources.
4. Check the **Actions** tab for the Pages deployment result. Open the site after a successful deployment and refresh it.
5. Test all six demo links, GitHub links, mobile navigation and your résumé once added. A Streamlit wake-up/sign-in page does not prove that the app itself is healthy.

If you see a 404, verify the exact repository name, selected branch/folder, root `index.html`, and successful Pages deployment. Relative asset paths allow this page to work locally and on Pages. GitHub Pages hosts the portfolio; the Python applications continue to run on Streamlit.

Official instructions: [publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [creating a Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Learning checkpoint

Before your next step, try changing one sentence, one color and one project tag. Preview at phone and desktop widths, navigate with Tab, and explain the difference between an internal link (`#projects`), a local file path (`css/style.css`) and an external URL. Commit these small edits with a clear message so you can track and reverse them.
