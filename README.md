
### Tools for creating D3 JavaScript network graphs from R

This is a port of Christopher Gandrud's [d3Network](http://christophergandrud.github.io/d3Network/) package to the [htmlwidgets](https://github.com/ramnathv/htmlwidgets) framework. 

#### Installation

To install and use you'll need to install this package and two of it's dependencies from GitHub:

```S
library(devtools)
install_github("rstudio/htmltools")
install_github("ramnathv/htmlwidgets", ref = "sizing")
install_github("jjallaire/d3networks")
```

Note that the version of htmlwidgets installed is from a particular development branch in that repo.

#### Usage

There is currently only one of the d3Network package functions available (`d3SimpleNetwork`). Here's an example of it's use:

```S
library(d3networks)

src <- c("A", "A", "A", "A", "B", "B", "C", "C", "D")
target <- c("B", "C", "D", "J", "E", "F", "G", "H", "I")
networkData <- data.frame(src, target)

d3SimpleNetwork(networkData)
```


