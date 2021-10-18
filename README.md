# .Rprofile module for blogdown projects

.Rprofile options for running an R session in `path/to/my_blogdown_project`.

## Why its own repository?

These blogdown options make sense outside of the context of any _specific_ blogdown site.
Multiple sites may use the same configs, but neither site should "own" these options.
Thus, they have their own module for website projects to import.

## Setup

For some other `site` folder...

```sh
cd path/to/site
```

Adding the module to project:

```sh
mkdir submodules
cd submodules
git submodule add <remote url>
```

Ensuring updated content:

```sh
git submodule update --init --recursive
```

Linking images to project locations:

```sh
# s = symlink, r = relative paths, f = force
cd ~/path/to/site
ln -s -f ./submodules/dots_blogdown/.Rprofile ./.Rprofile
```
