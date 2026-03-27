# Editing this site
This site is built using Hugo, a static site generator. The site is hosted on GitHub Pages, which automatically builds and deploys the site when changes are pushed to the `main` branch.

## Project structure

All website content lives inside the pages/ directory. Hugo uses Markdown files (`.md`) to generate pages.

## Syncing your local repository

If the project uses submodules, make sure they are properly initialized and updated:

```bash
git submodule init
git submodule update
```

## Adding new content

To create a new page, run the following command in your terminal:

```bash
cd pages
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

