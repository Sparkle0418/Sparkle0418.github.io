# Huaihan Shan’s personal website

A responsive, one-page academic website for GitHub Pages. It uses plain HTML and CSS, with no packages to install or build step.

Expected public address after GitHub Pages is enabled: **https://sparkle0418.github.io/**.

## Current content

The site includes About, Research, CV, and Contact sections. The biography identifies Huaihan Shan as a PhD student at Chicago Booth with interests in digital economics, industrial organization, and causal inference. The contact section links to `huaihan@uchicago.edu` and the GitHub profile. Research papers and the CV are pending; add them when ready. There are no invented papers or credentials, and no broken CV download link.

## Preview locally

Open `index.html` directly in a browser, or run this command from the repository:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then visit http://127.0.0.1:8000. Stop the server with Ctrl+C.

## Update your content

- **Biography:** edit the two paragraphs beneath your name in `index.html`.
- **Research:** edit the interests in the `research` section and replace the availability notice with your papers when ready. A sample paper entry is below.
- **CV:** create a `files` folder, place your PDF at `files/cv.pdf`, and replace the availability text using the link example in the HTML comment.
- **Email:** update the email link in the `contact` section and the `email` field in the structured data near the top of `index.html`.
- **Appearance:** edit the color variables at the top of `styles.css`.

Example research entry (replace every example value before adding it):

```html
<article>
  <h3>Paper title</h3>
  <p>Coauthors and current status</p>
  <p>A brief description of the research question and findings.</p>
  <a class="text-link" href="files/paper.pdf">Read paper (PDF)</a>
</article>
```

If you include a PDF link, add the corresponding PDF to the repository too. A title and description without a link is fine while a paper is in progress.

## Publish on GitHub Pages

The local files do not publish themselves. Once you are ready to share the content:

1. Commit and push the website files to the `main` branch of `Sparkle0418/Sparkle0418.github.io`.
2. Open the repository on GitHub and go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select **main** and **/(root)**, then **Save**.
5. Visit the public address above after deployment finishes. GitHub notes that publishing can take up to 10 minutes.

After this setup, pushing updates to `main` updates the website. The empty `.nojekyll` file tells GitHub Pages to serve these static files without Jekyll processing. Keep it in the repository. A custom Actions workflow is unnecessary for this site.

Official instructions: [Configure a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) and [Create a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Search visibility

The page title, visible heading, description, and structured data identify **Huaihan Shan**, independently of the GitHub username. `robots.txt` and `sitemap.xml` allow crawlers to discover the homepage. Search indexing and rankings are not guaranteed or immediate; this repository does not submit the site to a search engine automatically.

If you later use a custom domain, update the canonical URL, Open Graph URL, structured-data URL, `robots.txt`, and `sitemap.xml` together.
