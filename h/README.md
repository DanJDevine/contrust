# CONTRUST Website

This is a Quarto website skeleton for the CONTRUST academic project. It is set up to publish for free with GitHub Pages using GitHub Actions.

## How To Edit The Site

Edit the `.qmd` files in a text editor:

- `index.qmd`: homepage
- `project.qmd`: project overview, methods, funding, and larger logos
- `team.qmd`: team members and homepage links
- `outputs.qmd`: publications, working papers, presentations, and public engagement
- `news.qmd`: project updates
- `contact.qmd`: contact details

Edit site-wide settings in `_quarto.yml`. This controls the navigation tabs, site title, GitHub links, and the GitHub Pages URL placeholders.

Edit the design in `assets/styles.css`. The main colours are defined at the top of that file:

```css
--maroon: #5b1a18;
--gold: #f1bb7b;
--rose: #fd6467;
--rust: #d67236;
```

The real logo files are stored in `assets/img/erc-logo.png` and `assets/img/southampton-logo.png`. The small combined navbar version is `assets/img/navbar-logo-strip.png`; the Project page uses trimmed display copies at `assets/img/erc-logo-display.png` and `assets/img/southampton-logo-display.png`.

## Preview Locally

From this folder, run:

```bash
quarto preview
```

Render a final local build with:

```bash
quarto render
```

The rendered site is written to `_site/`. You do not need to upload `_site/` manually because the GitHub Actions workflow renders it on GitHub.

## Upload To GitHub

1. Create a new public GitHub repository, for example `contrust`.
2. Replace `YOUR-GITHUB-USERNAME` in `_quarto.yml` with your GitHub username.
3. From this folder, initialise git and push:

```bash
git init
git add .
git commit -m "Add CONTRUST website"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/contrust.git
git push -u origin main
```

4. On GitHub, open the repository and go to **Settings > Pages**.
5. Set **Build and deployment > Source** to **GitHub Actions**.
6. Open the **Actions** tab and run the **Publish website** workflow, or push another commit.

For a repository named `contrust`, the site will usually appear at:

```text
https://YOUR-GITHUB-USERNAME.github.io/contrust/
```

## Update Later

After editing pages, run:

```bash
quarto render
git add .
git commit -m "Update website"
git push
```

GitHub Actions will rebuild and redeploy the site automatically.
