# The Moving Epidemic Method Shiny Web Application

## Overview

*memapp* is a web application created to serve as a graphical user interface for the R mem package. It was created using Shiny, a web application framework for R.

## Installation

The stable package can be installed from the official R repositories (*CRAN*) using the built-in install function (or from the package manager in some GUIs for R):

```
# install the memapp CRAN version
install.packages("memapp")
```

To install the development version of *memapp* use the *devtools* package.

```
# install the devtools package
install.packages("devtools")
# install the memapp development version from GitHub
devtools::install_github("lozalojo/memapp")
```
When installing this version also you are intalling development versions of some sensitive packages that are used by *memapp* (including the *mem* package).

## Usage

To run the memapp application, just use the function:

```
# run the app:
memapp::runmemapp()
```

You can specify other parameters passed to `shiny::runApp`, such as `display = normal`, or  
`launch.browser = TRUE`.

## Notes

In order to use the Surveillance/Animation graph, *magick* package must be installed:

```
install.packages("magick")
```

Or alternatively, for low specs machines, the *animation* package:

```
install.packages("animation")
```

Along with one of the following programs: *GraphicsMagick* or *ImageMagick*:

www.imagemagick.org
www.graphicsmagick.org

The installers can be downloaded from their webpages or can be installed directly from R:

```
# check if installr is installed, and install it otherwise
if(!require("installr")) install.packages('installr')
library("installr")
# install GraphicsMagic
install.GraphicsMagick()
# install ImageMagick
install.ImageMagick()
```

## Localization

Starting with version 2.7, memapp enabled an option to localize the app. If your language is not listed in the Languages section and you want to see the app translated please, open the semicolon separated values file at github:

```
https://github.com/lozalojo/memapp/blob/master/inst/shinyapp/lang/en-GB.txt
```

With a text editor, translate the second column to your language and send it to the maintainer.

## References

Vega T, Lozano JE, Ortiz de Lejarazu R, Gutierrez Perez M. Modelling influenza epidemic—can we detect the beginning and predict the intensity and duration? Int Congr Ser. 2004 Jun;1263:281–3. 

Vega T, Lozano JE, Meerhoff T, Snacken R, Mott J, Ortiz de Lejarazu R, et al. Influenza surveillance in Europe: establishing epidemic thresholds by the moving epidemic method. Influenza Other Respir Viruses. 2013 Jul;7(4):546–58. DOI:10.1111/j.1750-2659.2012.00422.x.

Vega T, Lozano JE, Meerhoff T, Snacken R, Beaute J, Jorgensen P, et al. Influenza surveillance in Europe: comparing intensity levels calculated using the moving epidemic method. Influenza Other Respir Viruses. 2015 Sep;9(5):234–46. DOI:10.1111/irv.12330.

Lozano JE. lozalojo/mem: Second release of the MEM R library. Zenodo [Internet]. [cited 2017 Feb 1]; Available from: https://zenodo.org/record/165983. DOI:10.5281/zenodo.165983

