
<!-- README.md is generated from README.Rmd. Please edit that file -->

bunnies and reports, oh my!

# packages-report

## Bonus activity prompt

-   Combine your work analyzing your R packages and what we’ve learned
    re: GitHub and R Markdown
-   This `README.Rmd` gives a scaffold for using the work you did
    earlier to make a little report.
-   Given our previous work, I’m using pre-computed results and
    including a pre-made figure, leaving the R code down in scripts
    below `R/`. But know that, in other contexts, you could inline all
    that code in chunks here. Depends on downstream usage and the
    project context.
-   Locally, do `README.Rmd` –\> `README.md` with the “Knit” button or
    via `rmarkdown::render("README.Rmd")`. Commit both.
-   I presume you are hooked up to GitHub remote repo, covered in
    [Existing project, GitHub
    last](https://happygitwithr.com/existing-github-last.html). Summary:
    -   Consider the convenience function `usethis::use_github()`. Or to
        do by hand:
    -   Create a similarly-named repo on GitHub.
    -   Add it to the local repo as the `origin` remote:
        `git remote add origin https://github.com/YOU/REPO.git`.
    -   Push and cement the branch tracking relationship:
        `git push --set-upstream origin master`.
-   Push! Now your README is an excellent welcome mat and summary of
    your project.
-   On GitHub, in *Settings*, turn on GitHub Pages. Visit the given URL
    for an even more polished report of your project. It may take a few
    minutes to show up / update. Record that as the URL for your repo.

## Overview

The goal of packages-report is to FINISH THIS SENTENCE.

I have `FILL THIS IN!!!` add-on packages installed.

Here’s how they break down in terms of which version of R they were
built under, which is related to how recently they were updated on CRAN.

### Flow of the analysis

*If you have time, document the analysis works, using internal links.*

*If you created some sort of controller script, describe that here.*

<details>
<summary>
Session info
</summary>

``` r
devtools::session_info()
#> ─ Session info ───────────────────────────────────────────────────────────────
#>  setting  value
#>  version  R version 4.2.0 (2022-04-22 ucrt)
#>  os       Windows 10 x64 (build 19042)
#>  system   x86_64, mingw32
#>  ui       RTerm
#>  language (EN)
#>  collate  English_United States.utf8
#>  ctype    English_United States.utf8
#>  tz       America/New_York
#>  date     2022-06-23
#>  pandoc   2.17.1.1 @ C:/Program Files/RStudio/bin/quarto/bin/ (via rmarkdown)
#> 
#> ─ Packages ───────────────────────────────────────────────────────────────────
#>  package     * version date (UTC) lib source
#>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 4.1.1)
#>  backports     1.4.1   2021-12-13 [1] CRAN (R 4.2.0)
#>  brio          1.1.3   2021-11-30 [1] CRAN (R 4.2.0)
#>  broom         0.8.0   2022-04-13 [1] CRAN (R 4.1.3)
#>  cachem        1.0.6   2021-08-19 [1] CRAN (R 4.1.1)
#>  callr         3.7.0   2021-04-20 [1] CRAN (R 4.1.1)
#>  cellranger    1.1.0   2016-07-27 [1] CRAN (R 4.1.1)
#>  cli           3.3.0   2022-04-25 [1] CRAN (R 4.2.0)
#>  colorspace    2.0-3   2022-02-21 [1] CRAN (R 4.2.0)
#>  crayon        1.5.1   2022-03-26 [1] CRAN (R 4.2.0)
#>  DBI           1.1.2   2021-12-20 [1] CRAN (R 4.2.0)
#>  dbplyr        2.2.0   2022-06-05 [1] CRAN (R 4.2.0)
#>  desc          1.4.1   2022-03-06 [1] CRAN (R 4.2.0)
#>  devtools      2.4.3   2021-11-30 [1] CRAN (R 4.1.3)
#>  digest        0.6.29  2021-12-01 [1] CRAN (R 4.2.0)
#>  dplyr       * 1.0.9   2022-04-28 [1] CRAN (R 4.2.0)
#>  ellipsis      0.3.2   2021-04-29 [1] CRAN (R 4.1.1)
#>  evaluate      0.15    2022-02-18 [1] CRAN (R 4.1.3)
#>  fansi         1.0.3   2022-03-24 [1] CRAN (R 4.2.0)
#>  fastmap       1.1.0   2021-01-25 [1] CRAN (R 4.1.1)
#>  forcats     * 0.5.1   2021-01-27 [1] CRAN (R 4.1.1)
#>  fs            1.5.2   2021-12-08 [1] CRAN (R 4.1.2)
#>  generics      0.1.2   2022-01-31 [1] CRAN (R 4.2.0)
#>  ggplot2     * 3.3.6   2022-05-03 [1] CRAN (R 4.2.0)
#>  glue          1.6.2   2022-02-24 [1] CRAN (R 4.1.3)
#>  gtable        0.3.0   2019-03-25 [1] CRAN (R 4.1.1)
#>  haven         2.5.0   2022-04-15 [1] CRAN (R 4.2.0)
#>  hms           1.1.1   2021-09-26 [1] CRAN (R 4.1.1)
#>  htmltools     0.5.2   2021-08-25 [1] CRAN (R 4.1.1)
#>  httr          1.4.3   2022-05-04 [1] CRAN (R 4.2.0)
#>  jsonlite      1.8.0   2022-02-22 [1] CRAN (R 4.2.0)
#>  knitr         1.39    2022-04-26 [1] CRAN (R 4.2.0)
#>  lifecycle     1.0.1   2021-09-24 [1] CRAN (R 4.1.1)
#>  lubridate     1.8.0   2021-10-07 [1] CRAN (R 4.2.0)
#>  magrittr      2.0.3   2022-03-30 [1] CRAN (R 4.2.0)
#>  memoise       2.0.1   2021-11-26 [1] CRAN (R 4.2.0)
#>  modelr        0.1.8   2020-05-19 [1] CRAN (R 4.1.1)
#>  munsell       0.5.0   2018-06-12 [1] CRAN (R 4.1.1)
#>  pillar        1.7.0   2022-02-01 [1] CRAN (R 4.2.0)
#>  pkgbuild      1.3.1   2021-12-20 [1] CRAN (R 4.2.0)
#>  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 4.1.1)
#>  pkgload       1.2.4   2021-11-30 [1] CRAN (R 4.2.0)
#>  prettyunits   1.1.1   2020-01-24 [1] CRAN (R 4.1.1)
#>  processx      3.5.3   2022-03-25 [1] CRAN (R 4.2.0)
#>  ps            1.7.0   2022-04-23 [1] CRAN (R 4.2.0)
#>  purrr       * 0.3.4   2020-04-17 [1] CRAN (R 4.1.1)
#>  R6            2.5.1   2021-08-19 [1] CRAN (R 4.1.1)
#>  readr       * 2.1.2   2022-01-30 [1] CRAN (R 4.2.0)
#>  readxl        1.4.0   2022-03-28 [1] CRAN (R 4.2.0)
#>  remotes       2.4.2   2021-11-30 [1] CRAN (R 4.2.0)
#>  reprex        2.0.1   2021-08-05 [1] CRAN (R 4.1.1)
#>  rlang         1.0.2   2022-03-04 [1] CRAN (R 4.1.3)
#>  rmarkdown     2.14    2022-04-25 [1] CRAN (R 4.2.0)
#>  rprojroot     2.0.3   2022-04-02 [1] CRAN (R 4.2.0)
#>  rstudioapi    0.13    2020-11-12 [1] CRAN (R 4.1.1)
#>  rvest         1.0.2   2021-10-16 [1] CRAN (R 4.1.1)
#>  scales        1.2.0   2022-04-13 [1] CRAN (R 4.2.0)
#>  sessioninfo   1.2.2   2021-12-06 [1] CRAN (R 4.2.0)
#>  stringi       1.7.6   2021-11-29 [1] CRAN (R 4.2.0)
#>  stringr     * 1.4.0   2019-02-10 [1] CRAN (R 4.1.1)
#>  testthat      3.1.4   2022-04-26 [1] CRAN (R 4.2.0)
#>  tibble      * 3.1.7   2022-05-03 [1] CRAN (R 4.2.0)
#>  tidyr       * 1.2.0   2022-02-01 [1] CRAN (R 4.1.3)
#>  tidyselect    1.1.2   2022-02-21 [1] CRAN (R 4.2.0)
#>  tidyverse   * 1.3.1   2021-04-15 [1] CRAN (R 4.2.0)
#>  tzdb          0.3.0   2022-03-28 [1] CRAN (R 4.2.0)
#>  usethis       2.1.6   2022-05-25 [1] CRAN (R 4.2.0)
#>  utf8          1.2.2   2021-07-24 [1] CRAN (R 4.1.1)
#>  vctrs         0.4.1   2022-04-13 [1] CRAN (R 4.2.0)
#>  withr         2.5.0   2022-03-03 [1] CRAN (R 4.2.0)
#>  xfun          0.31    2022-05-10 [1] CRAN (R 4.2.0)
#>  xml2          1.3.3   2021-11-30 [1] CRAN (R 4.2.0)
#>  yaml          2.3.5   2022-02-21 [1] CRAN (R 4.2.0)
#> 
#>  [1] C:/Program Files/R/R-4.2.0/library
#> 
#> ──────────────────────────────────────────────────────────────────────────────
```

</details>

*See <https://github.com/jennybc/wtf-packages-report-EXAMPLE> for a
fully realized example.*
