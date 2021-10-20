# .Rprofile module for blogdown projects

.Rprofile options for running an R session in `path/to/my_blogdown_project`.

## Why its own repository?

These blogdown options make sense outside of the context of any _specific_ blogdown site.
Multiple sites may use the same configs, but neither site should "own" these options.
Thus, they have their own module for website projects to import.

## Setup

From `path/to/site`:

```sh
mkdir submodules
cd submodules
git submodule add git@github.com:mikedecr/dots_blogdown.git
git submodule update --init --recursive
```

Linking images to project locations:

```sh
# s = symlink, f = force
cd ~/path/to/site
ln -s -f ./submodules/dots_blogdown/.Rprofile ./.Rprofile
```
