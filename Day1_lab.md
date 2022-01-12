Package Development Lab Day 1
================
Joyce Robbins

# Create a package

1.  Create the package file structure by typing the following in the
    Console. Choose the path carefully so that you don’t create a
    package inside another project.

``` r
library(devtools)
create_package("~/covidtime")  # you can change the path
```

Your RStudio session will now switch to the new `covidtime` package
project.

2.  Create a new R script, type in the following function, and save it
    as `day.R` in the R folder:

``` r
whatdayisit <- function() {
  format(Sys.Date(), "%A, %B %d, %Y")
}
```

3.  Run the following in the Console:

``` r
library(devtools)
load_all()
```

4.  Test the function in the Console:

``` r
whatdayisit()
```

5.  Make some changes and repeat 3. and 4. Some ideas:

-   Change `whatdayisit()` so the output begins with `Today is`

Add functions either in the same file or new R files:

-   `tomorrow()` returns tomorrow’s date

-   `yesterday()` returns yesterday’s date

-   `daysto(date)` returns the number of days until `date`, for example:

`> daysto("2022-02-01")`

`Time difference of 20 days`

Note: do not use any other packages (yet)!

# Document and install

1.  Open the `DESCRIPTION` file and do the following:

<!-- -->

1.  Change the `Title:` line to:

`Title: Helps reduce pandemic induced temporal disintegration`

2.  Change the `Authors@R:` line so it includes your name and email
    address. *Don’t remove what looks like an extra comma.* Delete the
    `comment` part.

3.  Change the `Description:` line to:

`Description: Tools for regaining temporal orientation.`

When you’re done it should look like this (with your name and email):

    Package: covidtime
    Title: Helps reduce pandemic induced temporal disintegration
    Version: 0.0.0.9000
    Authors@R: 
        person("first", "last", , "first.last@example.com", role = c("aut", "cre"))
    Description: Tools for regaining temporal orientation.
    License: `use_mit_license()`, `use_gpl3_license()` or friends to pick a
        license
    Encoding: UTF-8
    Roxygen: list(markdown = TRUE)
    RoxygenNote: 7.1.2

2.  Open `day.R`. Put the cursor inside the function and click “Code…
    Insert Roxygen Skeleton”. This will create the function
    documentation structure but you need to fill in the contents.

<!-- -->

1.  Change the first line to
    `Returns the current day and date nicely formatted`

2.  Change the `@return` line to
    `@return character string with day and date`

3.  After the `@examples` line add `whatdayisit()`

When you’re done, the documentation part of the file should look like
this:

    #' Returns the current day and date nicely formatted
    #'
    #' @return character string with day and date
    #' 
    #' @export
    #'
    #' @examples
    #' whatdayisit()
    #' 

3.  Run the following in the Console:

``` r
document()
```

4.  Run the following in the Console:

``` r
install()
```

Check that it appears in your list of packages.

5.  Close the project and try using your package!

``` r
library(covidtime)
whatdayisit()
```

# (Optional) Store your package on GitHub

This will only work if you have set up git to work with RStudio.

Open the `covidtime` project and run the following in the Console:

``` r
usethis::use_git()
usethis::use_github()
```

Now anyone can install your package with `devtools::install_github()`.

To set default branch from master to main, execute the following in the
terminal:

`git config --global init.defaultBranch main`
`git config --global init.defaultBranch main`
