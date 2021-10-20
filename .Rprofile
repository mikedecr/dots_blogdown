# global variables that control blogdown behavior
# https://bookdown.org/yihui/blogdown/global-options.html

# ---- global rprofile -----------------------

if (file.exists("~/.Rprofile")) {
  base::sys.source("~/.Rprofile", envir = environment())
}

# ---- hugo version -----------------------

# Read hugo_version from blogdown to ensure the env variable matches.
# Putting this in local() contains a blogdown error (why?)
local({
    pkgs <- rownames(utils::installed.packages())
    if ('blogdown' %in% pkgs) {
        hugo_vn <<- blogdown::hugo_version()
    }
})
options(blogdown.hugo.version = hugo_vn)


# ---- blog workflow -----------------------

# new post directory and extension
options(blogdown.subdir = "post")
options(blogdown.ext = ".Rmarkdown")

# knit to markdown, theme handles the HTML
options(blogdown.method = "markdown")

# MATH: knit to markdown, theme handles mathjax implementation
# https://github.com/rstudio/blogdown/issues/466
options(blogdown.protect.math = TRUE)

# knitting Rmd files on save
options(blogdown.knit.on_save = FALSE)


# ---- other site/page configs -----------------------

options(blogdown.author = "Michael DeCrescenzo")
# affects Rstudio only
options(blogdown.serve_site.startup = TRUE) 





