## UseR - Urbana-Champaign Website Overview

Contained within this repository is the website source code that generates
<https://UrbanaChampaignUseR.github.io/>.

### Website Details 

Generally speaking, the website is made using the following tools:

- The backend of the site is powered by [`hugo`](https://gohugo.io/), which
  enables the static generation of files from [`markdown`](https://daringfireball.net/projects/markdown/) documents.
- Hosting for the website is through [Netlify](https://www.netlify.com). 
- To locally preview the website and convert `.Rmd` files to `.md` files, the [`blogdown`](https://github.com/rstudio/blogdown) package is employed which provides an interfaces with [`rmarkdown`](https://cran.r-project.org/web/packages/rmarkdown).
- Theming is based on the [`hugo-material theme`](https://github.com/cboettig/hugo-material).

### Materials

Short talks and hackathon files are stored in separate repositories. 
These repositories are split by the year in which the talk was given, 
e.g. `talks-2019`, through a [`git` submodule](https://github.blog/2016-02-01-working-with-submodules/).

To create a new submodule, first create a new repository on GitHub.

```
https://github.com/new
```

Then, within the `website` repository, construct a link via:

```bash
git submodule add git@github.com:UrbanaChampaignUseR/talks-<YYYY>.git static/talks/talks-<YYYY>
```

where `<YYYY>` represents the year without `<>`.


To refresh the submodule, use:

```bash
git submodule update --init --remote --merge --recursive
```

