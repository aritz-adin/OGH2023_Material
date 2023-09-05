# OpenGeoHub Summer School 2023

![](img/logo.png)<https://opengeohub.org/summer-school/opengeohub-summer-school-poznan-2023/>

## Tidy geographic data with sf, dplyr, ggplot2, geos and friends ([Robin Lovelace](https://www.robinlovelace.net/))

This lecture will provide an introduction to working with geographic
data using R in a ‘tidy’ way. It will focus on using the sf package to
read, write, manipulate, and plot geographic data in combination with
the tidyverse metapackage. Why use the **`sf`** package with the
tidyverse? The lecture will outline some of the ideas underlying the
tidyverse and how they can speed-up data analysis pipelines, while
making data analysis code easier to read and write. We will see how the
following lines

``` r
library(sf)
library(tidyverse)
```

can provide a foundation on which the many geographic data analysis
problems can be solved. The lecture will also cover on more recently
developed packages that integrate with the tidyverse to a greater and
lesser extent. We will look at how the **`geos`** package, which
provides a simple and high-performance interface to the GEOS library for
performing geometric operations on geographic data, integrates with the
tidyverse. The tidyverse is not the right tool for every data analysis
task and we touch on alternatives for working with raster data, with
reference to the **`terra`** package, and alternative frameworks such as
data.table. Finally, we will also look at how the ‘tidy’ philosophy
could be implemented in other programming languages, such as Python.

The focus throughout will be on practical skills and using packages
effectively within the wider context of project management tools,
integrated development environments (we recommend VS Code with
appropriate extensions or RStudio), and version control systems.

**Material del curso: <a href="https://ogh23.robinlovelace.net/"
class="uri">https://ogh23.robinlovelace.net/tidy</a>**

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
**`sf`** and **`stars`**.

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

## Unsupervised classification (clustering) of satellite images with R ([Krzysztof Dyba](https://researchportal.amu.edu.pl/info/author/UAM223562/Person%2Bprofile%2B%25E2%2580%2593%2BKrzysztof%2BDyba%2B%25E2%2580%2593%2BAdam%2BMickiewicz%2BUniversity?affil=&tab=main&conversationPropagation=begin&sort=&lang=en&pn=1))

Unsupervised classification of satellite images is the process of
grouping similar pixels on an image into homogeneous clusters based
primarily on their spectral characteristics. This approach does not
require reference (labeled) data, unlike supervised classification,
therefore it can be used as a method of first choice. Satellite image
classification is commonly used in a variety of fields, including
environmental monitoring, land cover mapping, and disaster management.
The generated thematic maps can be used to identify and monitor changes
in land use, and assess the impact of natural disasters.

During this workshop, participants will gain practical knowledge and
skills to perform unsupervised classification of Landsat data using the
R language. It will be demonstrated step by step how to use and prepare
raster data for analysis, popular grouping methods will be discussed and
finally we will prepare a land cover map with interpretation of the
results. The workshop will also cover the challenges and limitations of
unsupervised classification, such as subjective interpretation of
results difficulty of selecting the optimal number of clusters, and
validation methods for ensuring the accuracy and reliability of results.

The workshop is aimed at beginners, but basic knowledge of GIS and
satellite remote sensing is required.

**Material del curso: <https://kadyb.github.io/OGH2023/>**

**GitHub repository: <https://github.com/kadyb/OGH2023>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=YJlnxyEpDu4), [parte
2](https://www.youtube.com/watch?v=i06fwdLyZmg)**

## Cloud-based analysis of Earth Observation data using openEO Platform, R and Python ([Edzer Pebesma](https://www.uni-muenster.de/Geoinformatics/en/institute/staff/index.php/119/edzer_pebesma))

[**openEO**](https://openeo.org/) Platform holds a large amount of free
and open as well as commercial Earth Observation (EO) data which can be
accessed and analysed with openEO, an open API that enables cloud
computing and EO data access in a unified and reproducible way.
Additionally, client libraries are available in R, Python and
Javascript. A JupterLab environment and the Web Editor, a graphical
interface, allow a direct and interactive development of processing
workflows. The platform is developed with a strong user focus and
various use cases have been implemented to illustrate the platform
capabilities. Currently, three federated backends support the analysis
of EO data from pixel to continental scale.  

The future evolution of openEO Platform in terms of data availability
and processing capabilities closely linked to community requirements,
facilitated by feature requests from users who design their workflows
for environmental monitoring and reproducible research purposes. This
presentation provides an overview of the completed use cases, the newly
added functionalities such as user code sharing, and user interface
updates based on the new use cases and user requests. openEO Platform
exemplifies how the processing and analysing large amounts of EO data to
meaningful information products is becoming easier and largely compliant
with FAIR data principles supporting the EO community at large.

**openEO documentation: <https://docs.openeo.cloud/>**

**GitHub repository: <https://github.com/edzer/OGH23>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=NurpU0V6JG8), [parte
2](https://www.youtube.com/watch?v=mrY8VKOoz3c)**

## Environmental analysis using satellite image time series (Ewa Grabska-Szwagrzyk)

Satellite imagery time series offer a powerful means to detect and
analyze both short- and long-term changes in the environment. In
particular, the availability of open-access data from missions like
Landsat (since 1972) and Sentinel (since 2015) has significantly
enhanced our ability to study these changes. This workshop aims to
explore the use of time series of indices derived from satellite imagery
for analyzing various types of land cover changes using the programming
language R. The workshop will cover essential preprocessing steps,
including outlier removal and handling missing observations, to ensure
the quality of the data. Participants will learn how to effectively
model time series using different methods. Additionally, the workshop
will provide insights into detecting trends and breaks within the time
series data. The analysis will focus on a range of objects and encompass
both abrupt and gradual changes. Examples of the types of changes that
will be explored include urban growth or vegetation succession.

**Material del curso: <https://egrabska.github.io/OGH2023/>**

**GitHub repository: <https://github.com/egrabska/OGH2023>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=v_tQDJtCnsQ), [parte
2](https://www.youtube.com/watch?v=glR5hruA4-w)**

## Spatial ML model assessment and interpretation ([Alexander Brenning](https://geods.netlify.app/))

While significant progress has been made towards explaining black-box
machine-learning (ML) models, there is still a distinct lack of
diagnostic tools that elucidate the spatial behaviour of ML models in
terms of predictive skill and variable importance. This contribution
proposes spatial prediction error profiles (SPEPs) and spatial variable
importance profiles (SVIPs) as novel model-agnostic assessment and
interpretation tools for spatial prediction models with a focus on
prediction distance. Their suitability is demonstrated in two case
studies representing a regionalization task in an environmental-science
context, and a classification task from remotely-sensed land cover
classification. In these case studies, the SPEPs and SVIPs of
geostatistical methods, linear models, random forest, and hybrid
algorithms show striking differences but also relevant similarities.
Limitations of related cross-validation techniques are outlined, and the
case is made that modelers should focus their model assessment and
interpretation on the intended spatial prediction horizon. The range of
autocorrelation, in contrast, is not a suitable criterion for defining
spatial cross-validation test sets. The novel diagnostic tools enrich
the toolkit of spatial data science, and may improve ML model
interpretation, selection, and design.

**GitHub repository: <https://github.com/alexanderbrenning/ogh23_ml>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=EYJ7xsjrQ4o), [parte
2](https://www.youtube.com/watch?v=qElU6VzV0Jc)**

## Tools and packages to query and process Sentinel-1 and Sentinel-2 data with R and Python ([Lorena Abad](https://loreabad6.github.io/))

This session focuses on the products from the ESA Copernicus program
Sentinel-1 and Sentinel-2. These products can be freely accessed in
several manners and through different portals. We will take a look at
packages to query the data you need for your analyses using Python and
R, switching between platforms when relevant. An introduction on how to
process Sentinel data with both platforms will also be covered focusing
on the particularities of the sensors.

For Sentinel-1 data access, we will use the [ASF Data
Service](https://search.asf.alaska.edu/) to query data. There is no need
for credentials for querying the data but if you want to try the
downloading steps, you will need [Earthdata
Login](https://urs.earthdata.nasa.gov/) credentials.

**Material del curso: <https://loreabad6.github.io/ogh23/>**

**GitHub repository: <https://github.com/loreabad6/ogh23>**

**Enlace a la grabación en Youtube: [parte
1](https://www.youtube.com/watch?v=WRxmAhDEQFE), [parte
2](https://www.youtube.com/watch?v=a8X_jFN63Wc)**

## Processing large OpenStreetMap datasets for geocomputational research ([Robin Lovelace](https://www.robinlovelace.net/))

OpenStreetMap (OSM) is a free and openly editable map of the world. Like
Wikipedia and unlike government or corperation maintained datasets, OSM
is created and maintained by a community of volunteers, making it the
premier decentralized and fastest evolving source of geographic vector  
data focussed on features relevant to human activity (e.g. roads,
buildings, cafes) on planet Earth. Unlike Wikipedia, every data point in
OSM has a geographic location and attributes must be structured as
key-value pairs. OSM is a rich source of data for geocomputational
research, but the decentralized nature of the project and the sheer
volume of data. 'Planet.osm' now has more nodes than there are people on
Earth, with more than 8 billion
[nodes](https://wiki.openstreetmap.org/wiki/Node), and the rate of data
creation is increasing as the community grows, to [10 million
users](https://wiki.openstreetmap.org/wiki/Stats) in early 2023. The
size and rapid evolution of OSM are great strengths, democratising
geographic knowledge and ensuring resilience. However, these features
can make it difficult to work with OSM data. This lecture will provide
an introduction to working with OSM and will cover the following:

- How and where to download OSM data.

- How to process small amounts of OSM data using the **`osmdata`** R
  package.

- How to process large OSM 'extracts' data with the **`osmextract`** R
  package ([documentation](https://docs.ropensci.org/osmextract/)).

- Other command line tools for working with OSM data, including the
  mature and widely used `osmium` tool, the `pyrosm` Python package and
  the [`osm2streets`](https://github.com/a-b-street/osm2streets) web
  application and Rust codebase.

Finally, the lecture will outline ideas for using OSM data. It will
conclude with a call to action, inspiring the use of this rich resource
to support policy objectives such as the fast and fair decarbonisation
of the global economy as societies transition away from inefficient,
polluting and costly fossil fuels.

**Material del curso: <https://ogh23.robinlovelace.net/osm>**

**GitHub repository: <https://github.com/robinlovelace/opengeohub2023>**

## Progress in modernizing and replacing infrastructure packages in R-spatial workflows (Roger Bivand)

Until June 2023, maintainers of legacy packages using **`rgdal`**,
**`rgeos`** and/or **`maptools`** were encouraged to migrate to
**`sf`**/**`stars`** or **`terra`**, as described in
<https://github.com/r-spatial/evolution> and blogs listed there:
<https://r-spatial.org/r/2022/04/12/evolution.html>,
<https://r-spatial.org/r/2022/12/14/evolution2.html>,
<https://r-spatial.org/r/2023/04/10/evolution3.html>.

In June 2023, **`sp`** switches from using **`rgdal`** by default for
`sp::CRS` and `sp::spTransform` to using **`sf`** functionality by
default.

From October 2023, retiring packages **`rgdal`**, **`rgeos`** and
**`maptools`** will be archived on CRAN. This means that residual
installations of retiring packages will continue for R 4.2 and R 4.3,
but will not be updated after October 2023, nor will they be available
for R 4.4.

The workshop will present current status, and may assist participants
with affected workflows to adapt; the same applies to key affected
packages needed in participants’ workflows. Participants are invited to
contact the presenter with practical ideas to packages to adapt, and
time may also be used to prepare non-maintainer update candidates for
non-responsive packages. The count of affected packages was over 800,
but the severity of the impact of the withdrawal of the retiring
packages varies by the dependency category, strong dependence as Depends
or Imports, weak dependence as Suggests.

**Material del curso:
<https://r-spatial.github.io/evolution/ogh23_bivand.html>**

**GitHub repository: <https://github.com/r-spatial/evolution>**

## Introduction to working with spatial data in Python (Michael Dorman)

Python is an extremely popular general-purpose programming language. It
is used in a wide range of settings and for various purposes, including
for spatial data processing and analysis.

The aim of this tutorial is to give an introduction to methods of
working with spatial data using Python. The tutorial will be split into
two parts, introducing two central Python packages:

- `geopandas`---For working with vector layers

- `rasterio`---For working with rasters

The tutorial will demonstrate typical basic workflows of processing
spatial data: data input, processing, geo-computation, and exporting of
the results. We will use realistic datasets, such as GTFS public
transport data and remote sensing products.

By the end of the tutorial, the participants will be able to:

- Import spatial data from files

- Subset and process the data

- Graphically display the data

- Perform spatial calculations (such as calculating distances, or
  applying raster algebra operators)

- Export the results

To follow along and reproduce the results on your own computer, the
prerequisite is to be able to run Python code in a Jupyter Notebook
interface, linked to a Python environment with the two above-mentioned
packages installed. Instructions will be sent in advance.

**Material del curso: <https://geobgu.xyz/presentations/p_2023_ogh/>**

## Processing geospatial data using JuliaGeo framework ([Marteen Pronk](https://www.evetion.nl/))

Julia is a programming language that is simple to write and scriptable
like Python and R, but fast like C or C++. At 10 years, it’s a young
language, so the ecosystem isn’t as large and mature as you want it to
be. Maarten Pronk was an early adopter of the language in his research
at Deltares, a Dutch research institute. In this lecture(s) he will
introduce Julia, his motivation to use it and his OSS journey. Half of
the lecture will be non-spatial, while the latter half will focus on the
`JuliaGeo` ecosystem and showcased some of the possibilities of the
Julia language.

The [JuliaGeo GitHub](https://github.com/JuliaGeo) organization is
intended primarily for the collaborative development of packages that
are generally applicable across the geospatial and geosciences domains.
For dealing with geospatial data, packages from the JuliaGeometry and
JuliaImages organizations may also be of interest, and we will aim for
good integration with those. Since the JuliaGeo organization aims to
provide mostly general tools, more domain specific packages may be
better suited for development in domain specific organizations.
JuliaClimate is a nice example of such an organization that will be
especially interesting to climate, atmosphere and ocean scientists.
EcoJulia also provides some tools for generating and downloading spatial
data sets, with a focus on ecological applications.

**GitHub repository: <https://github.com/evetion/OGH2023>**

## Parallelization of geoprocessing workflows in GRASS GIS and Python ([Caitlin Haedrich](https://chaedri.github.io/))

High-resolution, continental-scale modeling enabled by modern, massive
datasets, requires development of scalable geoprocessing workflows. To
enable participants to effectively use available computational resources
(laptop, desktop, institutional HPC), we will introduce basic
parallelization concepts such as parallelization efficiency and scaling.
We will explain various approaches to parallelization in GRASS GIS, an
open source geoprocessing engine, that rely on OpenMP, Python and
Bash.  

In the hands-on part, participants will speed up an urban growth model
by parallelizing different parts of this complex geoprocessing workflow
using techniques that are easily applicable to a wide range of analyses
and computational resources. The workshop will be running in a Jupyter
Notebook environment using GRASS GIS Python API to run GRASS tools and
visualize results of the analysis in a reproducible way.

Participants will be able to either run the workshop on their laptops
(see instructions) or in a cloud environment (using WholeTale, no
installation required).

**GitHub repository:
<https://github.com/ncsu-geoforall-lab/opengeohub-2023>**

## xcube for spatiotemporal data analysis and visualization (Alicja Balfanz)

[xcube](https://xcube.readthedocs.io/en/latest/) is an open-source
xarray-based Python package and toolkit that has been developed to
provide Earth observation (EO) data in an analysis-ready form to users.
xcube achieves this by carefully converting EO data sources into
self-contained data cubes that can be published in the cloud.

In this session you will learn about the ecosystem around xcube, which
allows to access different data sources and turning the inputs into data
cubes. These data cubes can then be easily used for spatiotemporal data
analysis and visualization. After a brief introduction about the
software components, we will go step by step though some example Jupyter
notebooks and finally we will dive into a hands-on session with a little
challenge.

For the session you will need a laptop with an internet connection, some
basic knowledge about Python and already installed
[miniconda](https://docs.conda.io/en/latest/miniconda.html) which is
used to download the necessary Python packages for the session. Prior
experience with Jupyter notebooks will be helpful, but not mandatory.

## Data engineering for Mobility Data Science (with Python and DVC) ([Anita Graser](https://anitagraser.com/))

This session introduces [MovingPandas](https://movingpandas.org) and
[DVC](https://dvc.org) for Mobility Data Science.

MovingPandas is a Python library for the analysis and visualization of
movement data. It is built on top of GeoPandas and provides functions to
analyze, manipulate and plot trajectories. To get a better idea of the
type of analytics that MovingPandas supports, visit:
<https://movingpandas.org/examples>

DVC is a data version control (and machine learning experiment tracking)
library. It follows a similar logic to source code version control
systems (such as Git) and is typically used together with Git to keep
track of data and experiments while Git keeps track of the source code.
In this session, we will use DVC to keep track of our movement data
analytics workflow. Participants are expected to come prepared with a
working MovingPandas & DVC Python environment. Basic previous experience
with (Geo)Pandas and version control systems (i.e. how pull, commit,
push works in Git) is expected.

**GitHub repository:**
<https://github.com/movingpandas/movingpandas-examples/tree/opengeohub2023>

## Mapping explanation - Python toolchaing for spatial interpretative machine learning ([Jarosław Jasiewicz](http://jarekj.home.amu.edu.pl/))

The course will present applications of interpretive machine learning
methods to geospatial analysis. Interpretive machine learning is a new
branch of machine learning that allows the decomposition of black box
models. It allows complex, non-linear models to explain the criteria
that lead to a result. In the case of geospatial data, it can be used to
search for patterns of spatial explanatory factors. The course covers
the entire toolchain from data preparation, model training, and the data
transformation process, through data analysis and interpretation of the
results, to spatial visualization. The toolchain includes tools such as
the shap library, selected components of the scikit-learn, geopandas,
and matplotlib packages. The course includes a theoretical introduction
to interpretive machine learning and how it can be applied to geospatial
data. The practical part is built around analysing the U.S. presidential
election results Clinton vs. Trump. In the first step, explanatory
variables are collected and transformed into `shapely numbers`. The data
transformed in this way will determine the relevance of the explanatory
variables and their actual impact on the election outcome in each
county. The advantage of shapely numbers is that the variables are
automatically weighted, allowing for efficient clustering. The shapely
numbers and their clustering results reveal interesting spatial patterns
in the electoral process.

### Video: [Sharing your geospatial knowledge in the open](https://www.youtube.com/watch?v=AUt-GOZJQaY) ([Jakub Nowosad](https://jakubnowosad.com))
