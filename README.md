
<!-- README.md is generated from README.Rmd. Please edit that file -->

# trackdown - R package for enhancing collaborative writing <img src="man/figures/logo.png" align="right" width="120" />

<!-- badges: start -->

[![Project Status: Active – The project has reached a stable, usable
state and is being actively
developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![R-CMD-check](https://github.com/ekothe/trackdown/actions/workflows/check-standard.yaml/badge.svg)](https://github.com/ekothe/trackdown/actions/workflows/check-standard.yaml)
[![codecov](https://codecov.io/gh/ekothe/trackdown/branch/develop/graph/badge.svg?token=E6GR3JAHV6)](https://codecov.io/gh/ekothe/trackdown)
<!-- badges: end -->

## Overview

The `trackdown` package offers a simple answer to collaborative writing
and editing of R Markdown (or Sweave) documents. Using `trackdown`, the
local `.Rmd` (or `.Rnw`) file is uploaded as plain-text in Google Drive
where, thanks to the easily readable Markdown (or LaTeX) syntax and the
well-known online interface offered by Google Docs, collaborators can
easily contribute to the writing and editing of the document. After
integrating all authors’ contributions, the final document can be
downloaded and rendered locally.

All the documentation is available at
<https://ekothe.github.io/trackdown/>.

## Installation

This package is not already available on CRAN. To install the
development version from GitHub run the following code:

``` r
# install.packages("remotes")
remotes::install_github("ekothe/trackdown",
                         build_vignettes = TRUE)
library(trackdown)
```

## The trackdown Workflow

When collaborating on the writing of a `.Rmd` (or `.Rnw`) document it is
important to consider separately code and narrative text:

-   **Code** - Collaborative code writing is done efficiently following
    traditional **Git** workflow based on an online repository (e.g.,
    GitHub or GitLab)
-   **Narrative Text** - Collaborative writing of the narrative text is
    done efficiently on **Google Docs** where the familiar and simple
    online interface allows multiple users to simultaneously write and
    edit the same document

Thus, the workflow main idea is very simple: upload the `.Rmd` (or
`.Rnw`) document to Google Drive for collaborative writing of the
narrative text in Google Docs and download the document locally to
continue working on the code using Git. This iterative process of
uploading to and downloading from Google Drive continues until the
desired results are obtained. The workflow can be summarized as:

> Collaborative **code** writing using **Git** and collaborative writing
> of **narrative text** on **Google Docs**

<!-- pakgdown code-->
<!-- <iframe width="800" height="450" src="https://www.powtoon.com/embed/bWtc2qqbZ5F/" align="middle" frameborder="0" allowfullscreen></iframe> -->
<!-- Github code -->
<center>
<a href="https://www.powtoon.com/embed/bWtc2qqbZ5F/" target="_blank">
<img src="man/figures/video-thumbnail.png" align="center" style = "border: none; float: center;">
</a>
</center>

### Functions

The package `trackdown` offers different functions to manage the
workflow:

-   `upload_file()` - upload a file for the first time to Google Drive
-   `update_file()` - update the content of an existing file in Google
    Drive with the contents of a local file
-   `download_file()` - download edited version of a file from Google
    Drive updating the local version
-   `render_file()` - download and render a file from Google Drive

### Special Features

The Package `trackdown` offers special features to facilitate the
collaborative writing and editing of a document on Google Docs. In
particular, it is possible to:

-   **Hide Code** - The header code (YAML or LaTeX settings) and code
    chunks are removed from the document when uploaded to Google Drive
    and automatically restored when downloaded. This prevents
    collaborators from inadvertently making changes to the code that
    might corrupt the file and it allows collaborators to focus only on
    the narrative text ignoring code jargon.
-   **Upload Output** - The actual output (i.e., the resulting complied
    document) can be uploaded in Google Drive together with the `.Rmd`
    (or `.Rnw`) document. This helps collaborators to evaluate the
    overall layout, figures and tables and it allows them to use
    comments to propose and discuss suggestions.
-   **Google Team Drive** - The documents can be uploaded on your
    personal Google Drive or on a shared Google Team Drive to facilitate
    collaboration.

### Advantages of Google Docs

Google Docs offers a familiar, intuitive, and free online interface that
allows multiple users to simultaneously write and edit the same
document. In Google Docs it is possible to:

-   easily track changes
-   add comments to propose and discuss suggestions
-   check spelling and grammar errors (also using Grammarly)

Moreover, Google Docs allows anyone to collaborate on the document as no
programming experience is required, they only have to focus on the
narrative text ignoring code jargon.

Note that a Google account is not required for all collaborators
(although recommended to access all Google Docs features). Only the
person who manages the `trackdown` workflow requires a Google account to
upload files in Google Drive. Other collaborators can be invited to
contribute to the document using a shared link (See
[Instructions](https://support.google.com/drive/answer/2494822?co=GENIE.Platform%3DDesktop&hl=en&oco=0)).

### Documentation and Vignettes

All the documentation is available at
<https://ekothe.github.io/trackdown/>.

To know more about the `trackdown` see:

-   `vignette("trackdown-features")` - for detailed description of the
    function arguments and features
-   `vignette("trackdown-workflow")` - for a workflow example and a
    discussion about collaboration on narrative text and code
-   `vignette("trackdown-tech-notes")` - for details regarding technical
    aspects as authentication and file management

## Contributing to `trackdown`

The `trackdown` package is an ongoing project, surely there are many
issues to fix and features to propose. Anyone is welcome to contribute
to the development.

Please note that this project is released under a [Contributor Code of
Conduct](https://www.contributor-covenant.org/). By contributing to this
project, you agree to abide by its terms.

See [Community
guidelines](https://github.com/ekothe/trackdown/blob/develop/CONTRIBUTING.md)
for further information.

#### Future Plans

-   Improve compute time by parallelizing the code
-   Implement design analysis in the case of linear regression models

## Citation

To cite `trackdown` in publications use:

A BibTeX entry for LaTeX users is