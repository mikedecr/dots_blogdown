# global variables that control blogdown behavior
# https://bookdown.org/yihui/blogdown/global-options.html

# ---- global rprofile -----------------------

if (file.exists("~/.Rprofile")) {
  base::sys.source("~/.Rprofile", envir = environment())
}

# ---- hugo version -----------------------

# ensure that env variable matches blogdown
# by reading from blogdown directly
pkgs <- rownames(utils::installed.packages())
if ('blogdown' %in% pkgs) {
  hugo_vn <- blogdown::hugo_version()
  options(blogdown.hugo.version = hugo_vn)
}


# ---- blog workflow -----------------------

# post directory
options(blogdown.subdir = "post")

# knitting Rmd files on save
options(blogdown.knit.on_save = FALSE)

# knit to markdown, theme handles the HTML
options(blogdown.ext = ".Rmarkdown")
options(blogdown.method = "markdown")

# MATH: knit to markdown, theme handles mathjax implementation
# https://github.com/rstudio/blogdown/issues/466
options(blogdown.protect.math = TRUE)


# ---- other site/page configs -----------------------

options(blogdown.author = "Michael DeCrescenzo")
# affects Rstudio only
options(blogdown.serve_site.startup = TRUE) 





