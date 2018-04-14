# README

Reproducible mass spectrometry data analysis in R

Brendon Smith

br3ndonland

[![license](https://img.shields.io/badge/license-CC--BY--4.0%20-blue.svg)](https://choosealicense.com/)

[GitHub](https://github.com/br3ndonland/R-proteomics-Nrf1)

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Scientific background](#scientific-background)
- [Data analysis](#data-analysis)
  - [R Markdown](#r-markdown)
  - [Jupyter Notebook](#jupyter-notebook)
  - [Binder](#binder)
- [Instructions](#instructions)
  - [Run online with binder](#run-online-with-binder)
  - [Run locally](#run-locally)
- [Results](#results)

## Scientific background

This is a summary report of an experiment I performed during my postdoc. The goal of this experiment was to identify a [molecular](https://www.khanacademy.org/science/biology/macromolecules) complex associated with Nrf1, a protein we were studying.

We began studying Nrf1 because it resides in a [cellular organelle](https://youtu.be/URUJD5NEXC8) called the Endoplasmic Reticulum (ER). We study the ER and its roles in [metabolism](http://learn.genetics.utah.edu/content/metabolism/). We found that Nrf1 mediates the cellular response to cholesterol, and that it seemed to do this separately from its known function as a genetic transcription factor in the nucleus. Cholesterol metabolism occurs at the ER, and is very important in the liver, where cholesterol is metabolized and prepared for excretion.

We hypothesize that a group of other proteins interacts with Nrf1 to mediate its response to cholesterol at the ER. We used proteomics to test our hypothesis, which identifies all possible proteins in a sample with a technique called mass spectrometry.

[(Back to TOC)](#table-of-contents)

## Data analysis

Data analyses were performed with the R computing language, and are provided in [R Markdown](http://rmarkdown.rstudio.com/) and [Jupyter Notebook](http://jupyter.org/documentation) formats.

### R Markdown

- [R Markdown](http://rmarkdown.rstudio.com/) is a document creation package based on [Markdown](https://www.markdownguide.org/) (syntax for easy generation of formatted HTML documentation), [knitr](http://yihui.name/knitr/) (report generation package) and [pandoc](http://johnmacfarlane.net/pandoc/) (universal document converter).
- An RMarkdown file contains three types of data: YAML front matter header at the top of the file to specify output methods, Markdown-formatted text, and functional code chunks.
- I use [RStudio](https://www.rstudio.com/), installed via [Anaconda](https://www.anaconda.com/), to work with R Markdown.
- I created an [RStudio project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects), which is required for version control and package management.
- The R Markdown file outputs in the [GitHub document format](https://rmarkdown.rstudio.com/github_document_format.html) to output standard Markdown, in addition to HTML, for compatibility with GitHub.
- [Packrat](https://rstudio.github.io/packrat/) was used to manage R packages for the project. [Packrat works with RStudio](https://rstudio.github.io/packrat/rstudio.html) and gives each project its own private package library. R is heavily dependent on its package ecosystem, and Packrat helps avoid problems caused by different package versions and installations.

### Jupyter Notebook

- Jupyter Notebook files are run in JupyterLab, which is installed by default with Anaconda. JupyterLab was previously Jupyter Notebook.
- [JupyterLab](http://jupyterlab.readthedocs.io/en/latest/) is produced by [Project Jupyter](http://jupyter.org/). It is most widely used for scientific computing with Python, but supports many programming languages, including R.
- Jupyter Notebook files enable creation of "reproducible computational narratives" containing Markdown text interspersed with functional code chunks that will run and display output.

### Binder

- [Binder](https://mybinder.org/) turns GitHub repositories into reproducible computing environments. It uses code and dependency files to create Docker images that run in web browsers.
- Binder supports using R + RStudio, and provides a [GitHub demo repo](https://github.com/binder-examples/r) as an example of how to run RStudio from Binder. It requires [runtime.txt](binder/runtime.txt) to identify a specific snapshot of the CRAN package repository from [MRAN](https://mran.microsoft.com/documents/rro/reproducibility), and [install.R](binder/install.R) to specify R packages to install when the Binder is built. The two files runtime.txt and install.R can be in a [binder](binder) sub-directory.
- **Binder is a potentially great feature, but my experience so far is that it's extremely slow, and not properly loading additional R packages.**

[(Back to TOC)](#table-of-contents)

## Instructions

### Run online with binder

- JupyterLab
  - [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/br3ndonland/R-proteomics-Nrf1/master?urlpath=lab) JupyterLab+R
  - Open [R-proteomics-Nrf1-R.ipynb](R-proteomics-Nrf1-R.ipynb) from within Jupyter Lab.
  - Run all cells.
- RStudio
  - [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/br3ndonland/R-proteomics-Nrf1/master?urlpath=rstudio) RStudio
  - Open [R-proteomics-Nrf1.Rmd](R-proteomics-Nrf1.Rmd) from within RStudio.
  - Click knit (at the top of the source code viewer).
  - The RStudio project file [R-proteomics-Nrf1.Rproj](R-proteomics-Nrf1.Rproj) can also be opened from within RStudio. Beware, however, that RStudio will recognize the Packrat library and install all required packages. It could take up to an hour, in which time you could have already installed Anaconda, R, and RStudio on your computer.

### Run locally

- The files in this repository can also be run with RStudio and JupyterLab locally.
- Install [Anaconda](https://www.anaconda.com/) (including Python and JupyterLab by default). I install Anaconda by direct download, instead of from a Homebrew Cask, for proper configuration of the command prompt.
- Install R and R essentials from the command line:

  ```bash
  $ conda install -c r r-essentials
  ```

- Install RStudio from the command line:

  ```bash
  $ conda install rstudio
  ```

- [Fork](https://help.github.com/articles/fork-a-repo/) and [clone](https://help.github.com/articles/cloning-a-repository/) [this repository]().
- Open [R-proteomics-Nrf1.Rproj](R-proteomics-Nrf1.Rproj), or open RStudio and select "Open project."
- Click "Knit." RStudio will run the code, installing packages locally with Packrat, and will then present R Markdown output.

## Results

![Volcano plot from R analysis comparing proteins in cholesterol-fed vs chow-fed liver](img/volcano-plot-chol.png)

Complement C1q proteins A, B, C (green dots in the plot above) were identified as potentially interacting with Nrf1 in the setting of liver cholesterol accumulation. The experiment did have notable limitations, which prompted us to refine our methods and continue with further experiments.

[(Back to TOC)](#table-of-contents)