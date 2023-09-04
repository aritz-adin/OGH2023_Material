# OpenGeoHub Summer School 2023

# [“Processing and visualizing large geospatial data using R, Python and Julia”](https://opengeohub.org/summer-school/opengeohub-summer-school-poznan-2023/)

![](img/logo.png)

## Tidy geographic data with sf, dplyr, ggplot2, geos and friends ([Robin Lovelace](https://www.robinlovelace.net/))

This lecture will provide an introduction to working with geographic
data using R in a ‘tidy’ way. It will focus on using the sf package to
read, write, manipulate, and plot geographic data in combination with
the tidyverse metapackage. Why use the sf package with the tidyverse?
The lecture will outline some of the ideas underlying the tidyverse and
how they can speed-up data analysis pipelines, while making data
analysis code easier to read and write. We will see how the following
lines

``` r
library(sf)
library(tidyverse)
```

can provide a foundation on which the many geographic data analysis
problems can be solved. The lecture will also cover on more recently
developed packages that integrate with the tidyverse to a greater and
lesser extent. We will look at how the geos package, which provides a
simple and high-performance interface to the GEOS library for performing
geometric operations on geographic data, integrates with the tidyverse.
The tidyverse is not the right tool for every data analysis task and we
touch on alternatives for working with raster data, with reference to
the terra package, and alternative frameworks such as data.table.
Finally, we will also look at how the ‘tidy’ philosophy could be
implemented in other programming languages, such as Python.

The focus throughout will be on practical skills and using packages
effectively within the wider context of project management tools,
integrated development environments (we recommend VS Code with
appropriate extensions or RStudio), and version control systems.

**Material del curso: <https://ogh23.robinlovelace.net/>**

**GitHub repository: <https://github.com/robinlovelace/opengeohub2023>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=CwL_luh2tWs), [parte
2](https://www.youtube.com/watch?v=1sQN6r-u15o)**

## Raster and vector data cubes in R ([Edzer Pebesma](https://www.uni-muenster.de/Geoinformatics/en/institute/staff/index.php/119/edzer_pebesma))

A common challenge with raster datasets is not only that they come in
large files (single Sentinel-2 tiles are around 1 GB), but that many of
these files, potentially thousands or millions, are needed to address
the area and time period of interest. In 2022, Copernicus, the program
that runs all Sentinel satellites, published 160 TB of images per day.
This means that a classic pattern in using R consisting of downloading
data to local disc, loading the data in memory, and analysing it is not
going to work. This lectures describes how large spatial and
spatiotemporal datasets can be handled with R, with a focus on packages
**sf** and **stars**.

For practical use, we classify large datasets as too large:

- to fit in working memory,
- to fit on the local hard drive, or
- to download to locally managed infrastructure (such as network
  attached storage)

These three categories may (today) correspond very roughly to Gigabyte-,
Terabyte- and Petabyte-sized datasets. Besides size considerations,
access and processing speed also play a role, in particular for larger
datasets or interactive applications. Cloud native geospatial formats
are formats optimised with processing on cloud infrastructure in mind,
where costs of computing and storage need to be considered and
optimised.

**Material del curso: <https://edzer.github.io/OGH23/dc.html> / [R
book](https://r-spatial.org/book/)**

**GitHub repository: <https://github.com/edzer/OGH23>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=c8omo1tEB-8), [parte
2](https://www.youtube.com/watch?v=hvST0r9F59Y)**
