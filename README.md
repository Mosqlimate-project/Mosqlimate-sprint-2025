# Editing this site
This site is built using Hugo, a static site generator. The site is hosted on GitHub Pages, which automatically builds and deploys the site when changes are pushed to the `master` branch.

## Adding new content
Hugo uses Markdown files to create content for your website. To create a new page, run the following command in your terminal:

```bash
hugo new path/to/new-page.md
```

This will create a new Markdown file in the specified path. Open the file and start editing the content using Markdown syntax.

Build the site: Once you've made your changes, run the following command to build your website:

```bash
hugo
```


This will generate the static HTML files for your website in the public directory.

Preview the site: To preview your website locally, run the following command:

```bash
hugo server
```

This will start a local development server. Open your web browser and navigate to the URL provided by Hugo to see your website.

## Deploying changes
Once you're happy with your changes, commit them to your local repository and push them to GitHub. GitHub Pages will automatically build and deploy your site.

