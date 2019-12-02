# Smartphone apps for the treatment of mental disorders: Data, analysis and computational environment

R Markdown notebook for the paper "Smartphone apps for the treatment of mental disorders: a systematic review"

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2682244.svg)](https://doi.org/10.5281/zenodo.2682244)

## Reproduce Online

Click the "Binder" button below to open the notebook on [binder.org](https://mybinder.org/).

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/cgranell/apps-treatment-mental-disorders/master?urlpath=rstudio)

In the RStudio page, open the file `analysis.Rmd`, the _main analysis file_. Then select "Knit > Knit to HTML" to render the document, which includes the complete analysis workflow, and display it in your browser. 

Alternatively, click on the file  `analysis.html`, the results of the analysis, and select `View in Web Browser` to display it. 

## Reproduce locally

Open the main analysis file `analysis.Rmd` with RStudio. Then select "Knit > Knit to HTML" to render the document. If you have errors rendering it, try running each chunk to locate the problem.

The Markdown document does not include code to install required packages. Run the code in the file `install.R` to install all dependencies.

## Reproduce locally with Docker (more on this soon)

Install [Docker CE](https://www.docker.com/community-edition) or a compatible tool for building an image based on a `Dockerfile` and running a container based on the image. Download the project files, open a command line in the root directory (where this file is), and run the following commands:

```bash
# build the image
docker build --tag apps-treatment-md .
# run the image
docker run -it -p 8888:8888 apps-treatment-md
```

Open a browser at http://localhost:8888 or click on the login link shown in the console. It will show the Jupyter start page as in the instructions in [Reproduce online](#reproduce-online).

## Files in this repository

- `all_data.rda`: Data items extracted from the surveyed papers.
- `all_data.csv`: Data items extracted from the surveyed papers.
- `analysis.Rmd`: R Markdown document with the code to conduct the analysis and create the figures and tables of the paper.
- `analysis.html`: HTML rendering of the analysis document.
- `Dockerfile`: A recipe for the computational environment using [Docker](https://en.wikipedia.org/wiki/Docker_(software)).
- `install.R`: R script file executed during creation of the Docker image to install required dependencies.

## Deposition on Zenodo

This repository is archived on Zenodo with DOI: [10.5281/zenodo.2682244](https://doi.org/10.5281/zenodo.2682244)


## License

The documents in this repository are licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

All contained code is licensed under the [Apache License 2.0](https://choosealicense.com/licenses/apache-2.0/).

The data used is licensed under a [Open Data Commons Attribution License](https://opendatacommons.org/licenses/by/).
