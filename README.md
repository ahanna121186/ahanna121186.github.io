# Andrew Hanna: academic website (Quarto + GitHub Pages)

This folder is a complete starter website. This guide explains what each piece does and how to get it online.

## What's in here

| File / folder | What it does |
|:--|:--|
| `_quarto.yml` | Site-wide settings: title, navigation menu, theme. Edit this to add or rename pages. |
| `index.qmd` | Home page: bio, photo slot, link buttons, highlights. |
| `research.qmd` | Publications, manuscripts under review, projects in progress, grants. |
| `teaching.qmd` | Courses, ratings, awards, certifications. |
| `talks.qmd` | Invited and refereed presentations. |
| `service.qmd` | Awards, professional and university service. |
| `cv.qmd` | CV summary plus download button. |
| `files/Hanna_CV.pdf` | Your CV, linked from the site. Replace it when you update your CV. |
| `styles.scss` | Colors and small visual tweaks. |
| `.github/workflows/publish.yml` | The "robot" that builds and publishes the site automatically. |
| `.gitignore` | Tells Git which files not to track (build leftovers). |

**What is a `.qmd` file?** It's a Quarto Markdown file: plain text with simple formatting symbols (`##` for headings, `**bold**`, `[link text](url)`). Each one becomes a page. Later, the same format can run R code and show results, which makes it useful for methods tutorials.

**How the pieces connect:** you edit `.qmd` files, Quarto turns them into HTML pages using the settings in `_quarto.yml` and `styles.scss`, and GitHub Pages serves those pages at `https://YOUR-USERNAME.github.io`.

## Step 1: Replace the placeholders

Search all files for `YOUR-USERNAME` and replace it with your GitHub username. It appears in `_quarto.yml`, `index.qmd`, and `research.qmd`. (On GitHub's website you can edit files with the pencil icon.)

## Step 2: Create the repository (if you haven't)

1. On GitHub, click **New repository**.
2. Name it exactly `YOUR-USERNAME.github.io`. This special name is what makes it your personal site.
3. Set it to **Public**. Don't add a README, since this folder has one.

## Step 3: Upload these files

Easiest route, no software needed:

1. Unzip this folder on your computer.
2. In your new repository, click **Add file > Upload files**.
3. Drag in the *contents* of the folder (not the folder itself). Make sure the hidden `.github` folder comes along. If your computer hides it, enable "show hidden files" (Mac: `Cmd + Shift + .`), or use GitHub Desktop (below).
4. Scroll down and click **Commit changes**.

Alternative with GitHub Desktop (free app): clone the repository, copy the files into the cloned folder, then commit and push. This is a good habit to learn, since it's how you'll manage paper repos later.

## Step 4: Turn on GitHub Pages

1. In the repository, go to **Settings > Pages**.
2. Under **Build and deployment > Source**, choose **GitHub Actions**.
3. Go to the **Actions** tab. You should see "Publish site" running. After 1-3 minutes it turns green.
4. Visit `https://YOUR-USERNAME.github.io`.

If the first run failed because Pages wasn't enabled yet, open the Actions tab, click the failed run, and choose **Re-run all jobs**.

## Everyday editing

Open any `.qmd` file on GitHub, click the pencil, edit, and click **Commit changes**. The site rebuilds itself in a couple of minutes. To update your CV, upload a new PDF named `Hanna_CV.pdf` into the `files` folder.

## Optional: preview on your computer

Install [Quarto](https://quarto.org/docs/get-started/) (RStudio users: it's likely already bundled), open the folder, and run `quarto preview` in a terminal, or press the Render button in RStudio. The site opens in your browser and refreshes as you save.

## Things to decide or fill in

- **Photo:** save a headshot as `files/profile.jpg` and un-comment the `image:` line in `index.qmd`.
- **Google Scholar and ORCID:** un-comment those lines in `index.qmd` and add your URLs.
- **Teaching philosophy:** a placeholder is in `teaching.qmd`.
- **Phone number** is deliberately left off the public site.
- **Under-review and in-progress papers** are listed without journal names. Add them back if you prefer.
- **Reference list** from your CV is deliberately not published.

## Later ideas

- A **Resources** page with R/lavaan example scripts for factor analysis, parceling, and model fit, linked to repos.
- One GitHub repository per paper (R scripts, simulated or de-identified data, a README on how to reproduce results), linked from the Research page and paired with OSF if you preregister.
- A custom domain such as `andrewhanna.com` (GitHub Pages supports this).

## Privacy reminder

Everything in a public repository is public, including its history. Never commit identifiable participant data, IRB-restricted data, or consulting data covered by an agreement.
