# Materials for package development workshop

## Pre-workshop setup

### Everyone
Install the **devtools** package:

`install.packages(devtools)`

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

## Agenda

### Day 1

* 

