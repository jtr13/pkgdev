# Materials for package development workshop

_(Additional files to be added.)_

These materials are based on the [package development workshop modules](https://github.com/forwards/workshops/tree/master/package-dev-modules) developed by Emma Rand and Mine Çetinkaya-Rundel for [RForwards](https://forwards.github.io/about/).

## Pre-workshop setup

### Everyone

Install the **devtools** package:

`install.packages(devtools)`

If you already have **devtools** please reinstall to be sure you have the latest version (2.4.3) as [the package has frequent updates](https://github.com/r-lib/devtools/blob/main/NEWS.md).

(for Day 2) Install the **assertthat** package:

`install.packages(assertthat)`

### Windows users

(Verbatim from: https://r-pkgs.org/setup.html#windows)

On Windows the collection of tools needed for building packages from source is called Rtools.

Rtools is NOT an R package. It is NOT installed with `install.packages()`. Instead, download it from <https://cran.r-project.org/bin/windows/Rtools/> and run the installer.

During the Rtools installation you may see a window asking you to "Select
Additional Tasks".

- Do _not_ select the box for "Edit the system PATH". devtools and RStudio should put Rtools on the `PATH` automatically when it is needed.
- Do select the box for "Save version information to registry". It should be selected by default.


### Mac users

(Verbatim from: https://r-pkgs.org/setup.html#macos)

You need to install the Xcode command line tools, which requires that you [register as an Apple developer](https://developer.apple.com/programs/register/) (don't worry, it's free).

Then, in the shell, do:

```shell
xcode-select --install
```

Alternatively, you can install the current release of full [Xcode from the Mac App Store](https://itunes.apple.com/ca/app/xcode/id497799835?mt=12). This includes a very great deal that you do not need, but it offers the advantage of App Store convenience.

## Agenda (tentative)

### Day 1
* Where do R package come from?
* Why create R packages?
* Packages vs. scripts
* Creating initial package files
* Adding functions to the package
* Package states
* `devtools::load_all()`: testing and modifying functions
* `devtools::document()`: documenting your functions

### Day 2
* `devtools::check()`: checking a package
* Naming your package
* Licensing your package
* Adding dependencies
* Adding examples to documentation
* Creating vignettes
* Using git/GitHub
* Where next?


