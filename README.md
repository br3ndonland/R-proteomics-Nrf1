# README

Reproducible proteomic mass spectrometry data analysis in R

Brendon Smith

br3ndonland

[![license](https://img.shields.io/badge/license-CC--BY--4.0%20-blue.svg)](https://choosealicense.com/)

Provided on [GitHub](https://github.com/br3ndonland/R-proteomics-Nrf1) with a CC-BY-4.0 license.

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Reproducibility](#reproducibility)
  - [Comments](#comments)
  - [Resources](#resources)
- [Scientific background](#scientific-background)
- [Experimental methods](#experimental-methods)
- [Data analysis](#data-analysis)
  - [R Markdown](#r-markdown)
  - [Jupyter Notebook](#jupyter-notebook)
  - [Binder](#binder)
- [Instructions](#instructions)
  - [Run locally](#run-locally)
  - [Run online with binder](#run-online-with-binder)
- [Results](#results)

## Reproducibility

### Comments

What gets me out of bed in the morning is the **power of science to teach us about the world**. It's the most evidence-based thing we have. We use theory and experiment to generate new knowledge.

In science, reproducibility occurs when different scientists do the same experiment and get results that agree. **Our current scientific practices do not promote or reward reproducibility**. As a result, the scientific community is experiencing a **reproducibility crisis**, in which the discoveries that we publish can't be reproduced by multiple labs, or even repeated within the same lab by the same person, in some instances. This is not authentic knowledge.

The reproducibility crisis is troubling to me. During my postdoc in a large molecular biology lab, I saw the reproducibility crisis unfold, both in the scientific literature and among my colleagues. Even more striking than the crisis itself was the lack of an insightful solution. Rather than transition into an academic position and complain about this for the next forty years, I decided to do something about it. I started building my computational skills, focusing on web development, and I plan to build tools to alleviate some aspects of the reproducibility crisis.

**Documentation is the *sine qua non* of reproducibility.** How can we hope to reproduce experiments if we don't know how they were done? Documentation must start at the beginning, with reproducible data analysis being preceded by reproducible experimental practices. No statistical adjustment can make up for lack of detailed metadata collected at the time the experiment is performed. Clear, annotated raw data should be provided, and data analyses should clearly describe each action taken from raw data to final analysis.

This repository is a practical example of reproducible scientific data analysis. I have attempted to provide, to the greatest extent possible on GitHub, a complete documentation of the methods that led to the results presented. It's not perfect. There's definitely more I could do, but it's important practice for me and for science.

It might seem strange to my scientific colleagues, who are mostly focused on career advancement and personal aggrandizement, that I would take so much time to analyze preliminary data from a pilot study like this. **It's not just about the end result. If we want to address the reproducibility crisis, we need to focus on the process.**

### Resources

- These papers provide general discussions of reproducibility:
  - Barba LA. The hard road to reproducibility. *Science* 354:142 (2016). [https://doi.org/10.1126/science.354.6308.142](https://doi.org/10.1126/science.354.6308.142)
  - Loscalzo J. Irreproducible experimental results: Causes, (mis)interpretations, and consequences. *Circulation* 125:1211–1214 (2012). [https://doi.org/10.1161/circulationaha.112.098244](https://doi.org/10.1161/circulationaha.112.098244)
  - Morrison SJ. Time to do something about reproducibility. *eLife* 3:1–4 (2014). [https://doi.org/10.7554/eLife.03981](https://doi.org/10.7554/eLife.03981)
  - Sarewitz D. The pressure to publish pushes down quality. *Nature* 533:147 (2016). [https://doi.org/10.1038/533147a](https://doi.org/10.1038/533147a)
- The surgeon and writer Atul Gawande wrote a book about his research, in which he found that distributing a checklist (protocol) to surgical team members reduced patient deaths by half. If world-class surgeons can benefit from improved protocols, scientists certainly can also.
  - [The Checklist Manifesto, by Atul Gawande](http://a.co/0SjWYmN)
  - Haynes, AB et al. A surgical safety checklist to reduce morbidity and mortality in a global population. *NEJM* 360:491–499 (2009). [https://doi.org/10.1056/NEJMsa0810119](https://doi.org/10.1056/NEJMsa0810119)
- This *Cell Reports* commentary is a valuable example of the importance of documentation for experimental reproducibility.
  - Hines WC, Su Y, Kuhn I, Polyak K, Bissell MJ. Sorting out the FACS: A devil in the details. *Cell Rep.* 6:779–781 (2014). [https://doi.org/10.1016/j.celrep.2014.02.021](https://doi.org/10.1016/j.celrep.2014.02.021)
- Research reagents and materials, including antibodies, cell lines, and mice, appear to contribute substantially to lack of reproducibility.
  - Baker M. Reproducibility crisis: Blame it on the antibodies. *Nature* 521:274–276 (2015). [https://doi.org/10.1038/521274a](https://doi.org/10.1038/521274a)
  - Couzin-Frankel J. When mice mislead. *Science* 342:922–925 (2013). [https://doi.org/10.1126/science.342.6161.922](https://doi.org/10.1126/science.342.6161.922)
  - Ioannidis JPA. Extrapolating from animals to humans. *Sci. Transl. Med.* 4:151ps15 (2012). [https://doi.org/10.1126/scitranslmed.3004631](https://doi.org/10.1126/scitranslmed.3004631)
  - Lorsch JR, Collins FS, Lippincott-Schwartz J. Fixing problems with cell lines: Technologies and policies can improve authentication. *Science* 346:1452–1453 (2014). [https://doi.org/10.1126/science.1259110](https://doi.org/10.1126/science.1259110)
  - Martin B, Ji S, Maudsley S, Mattson MP. ‘Control’ laboratory rodents are metabolically morbid: why it matters. *PNAS* 107:6127–6133 (2010). [https://doi.org/10.1073/pnas.0912955107](https://doi.org/10.1073/pnas.0912955107)
- *Nature* ironically reports on the reproducibility crisis, while continuing to publishing trendy irreproducible articles weekly.
  - Baker M. 1,500 scientists lift the lid on reproducibility. *Nature* 533:452–454 (2016). [https://doi.org/10.1038/533452a](https://doi.org/10.1038/533452a)
  - Shen H. Interactive notebooks: Sharing the code. *Nature* 515:151–2 (2014). [https://doi.org/10.1038/515151a](https://doi.org/10.1038/515151a)
- The scientific journal *eLife* is a leader in reproducible data analysis and publishing. I particularly enjoy the [eLife Labs blog](https://elifesciences.org/labs).
- [Data Carpentry](http://www.datacarpentry.org/), which is sponsored by [NumFOCUS](https://www.numfocus.org/), has a [Reproducible Science Curriculum](https://github.com/Reproducible-Science-Curriculum) and holds workshops on reproducible data analysis in Python and R.
- The Harvard [Institute for Applied Computational Science (IACS)](https://iacs.seas.harvard.edu/) provides free resources to the scientific computing community, such as the annual [Computefest](https://computefest.seas.harvard.edu/). See *EDA.ipynb* and *grammarofdata.ipynb* from [Computefest 2018](https://github.com/Harvard-IACS/computefest2018-pandas) for info on reproducible Exploratory Data Analysis (EDA) workflows.
- Vincent Carey (Harvard Medical School, Brigham & Women's Hospital) provided helpful [resources](https://github.com/vjcitn/Repro2017) for reproducible data analyses associated with his Repro2017 Harvard Catalyst talk.

[(Back to TOC)](#table-of-contents)

## Scientific background

This is a summary report of an experiment I performed during my postdoc. The goal of this experiment was to identify a [molecular](https://www.khanacademy.org/science/biology/macromolecules) complex associated with Nrf1, a protein we were studying.

We began studying Nrf1 because it resides in a [cellular organelle](https://youtu.be/URUJD5NEXC8) called the Endoplasmic Reticulum (ER). We study the ER and its roles in [metabolism](http://learn.genetics.utah.edu/content/metabolism/). We found that Nrf1 mediates the cellular response to cholesterol, and that it seemed to do this separately from its known function as a genetic transcription factor in the nucleus. Cholesterol metabolism occurs at the ER, and is very important in the liver, where cholesterol is metabolized and prepared for excretion.

We hypothesize that a group of other proteins interacts with Nrf1 to mediate its response to cholesterol at the ER. We used proteomics to test our hypothesis, which identifies all possible proteins in a sample with a technique called mass spectrometry.

[(Back to TOC)](#table-of-contents)

## Experimental methods

The experimental methods are summarized in the computational analyses. Supplementary data, including the electronic lab notebook, raw data, other data analyses, and PowerPoint slides, are available in the [data-supplementary](data-supplementary) sub-directory of this repository.

## Data analysis

Data analyses were performed with the R computing language, and are provided in [R Markdown](http://rmarkdown.rstudio.com/) and [Jupyter Notebook](http://jupyter.org/documentation) formats.

These formats both allow a **combination of prose and code,** and promote construction of **reproducible computational narratives** that precisely describe each step in the data analysis. When code from a reproducible computational narrative is run on another computer, there is a high probability that the same result will be obtained. Reproducibility.

### R Markdown

- [R Markdown](http://rmarkdown.rstudio.com/) is a document creation package based on [Markdown](https://www.markdownguide.org/) (syntax for easy generation of formatted HTML documentation), [knitr](http://yihui.name/knitr/) (report generation package) and [pandoc](http://johnmacfarlane.net/pandoc/) (universal document converter).
- An RMarkdown file contains three types of data: YAML front matter header at the top of the file to specify output methods, Markdown-formatted text, and functional code chunks.
- I use [RStudio](https://www.rstudio.com/), installed via [Anaconda](https://www.anaconda.com/), to work with R Markdown.
- I created an [RStudio project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects), which is required for version control and package management.
- As you would guess by the fact that this is on GitHub, the repository is under version control with [Git](https://git-scm.com/doc).
- The R Markdown file outputs in the [GitHub document format](https://rmarkdown.rstudio.com/github_document_format.html) to output standard Markdown, in addition to HTML, for compatibility with GitHub.
- [Packrat](https://rstudio.github.io/packrat/) was used to manage R packages for the project. [Packrat works with RStudio](https://rstudio.github.io/packrat/rstudio.html) and gives each project its own private package library. R is heavily dependent on its package ecosystem, and Packrat helps avoid problems caused by different package versions and installations.

### Jupyter Notebook

- Jupyter Notebook files are run in JupyterLab, which is installed by default with Anaconda. JupyterLab was previously Jupyter Notebook.
- [JupyterLab](http://jupyterlab.readthedocs.io/en/latest/) is a development environment produced by [Project Jupyter](http://jupyter.org/). It is most widely used for scientific computing with Python, but supports many programming languages, including R.
- Jupyter Notebook files enable creation of reproducible computational narratives containing Markdown text interspersed with functional code chunks that will run and display output.

### Binder

- [Binder](https://mybinder.org/) turns GitHub repositories into reproducible computing environments. It uses code and dependency files to create [Docker](https://www.docker.com/) images that run in web browsers.
- Binder supports using R + RStudio, and provides a [GitHub demo repo](https://github.com/binder-examples/r) as an example of how to run RStudio from Binder. Running R requires [runtime.txt](binder/runtime.txt) to identify a specific snapshot of the CRAN package repository from [MRAN](https://mran.microsoft.com/documents/rro/reproducibility), and [install.R](binder/install.R) to specify R packages to install when the Binder is built. The two files runtime.txt and install.R can be in a [binder](binder) sub-directory.
- **Binder is a potentially great feature, but my experience so far is that it's extremely slow, and not properly loading additional R packages.**

[(Back to TOC)](#table-of-contents)

## Instructions

### Run locally

- The files in this repository can also be run with RStudio and JupyterLab locally.
- Install [Anaconda](https://www.anaconda.com/) (includes Python and JupyterLab by default). I install Anaconda by [direct download](https://www.anaconda.com/download/), instead of from a [Homebrew Cask](https://caskroom.github.io/), for proper configuration of the command prompt.
- Install R and R essentials from the command line:

  ```bash
  $ conda install -c r r-essentials
  ```

- Install RStudio from the command line:

  ```bash
  $ conda install rstudio
  ```

- [Fork](https://help.github.com/articles/fork-a-repo/) and [clone](https://help.github.com/articles/cloning-a-repository/) [this repository](https://github.com/br3ndonland/R-proteomics-Nrf1).
- Open [R-proteomics-Nrf1.Rproj](R-proteomics-Nrf1.Rproj), or open RStudio and select "Open project."
- Click "Knit." RStudio will run the code, installing packages locally with Packrat, and will then present R Markdown output. Installation of packages may take some time, and requires an internet connection.

### Run online with binder

- Again, **Binder is a potentially great feature, but my experience so far is that it's extremely slow, and not properly loading additional R packages.** It seems to have trouble loading the `calibrate` package.
- JupyterLab
  - [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/br3ndonland/R-proteomics-Nrf1/master?urlpath=lab) JupyterLab+R
  - Open [R-proteomics-Nrf1-R.ipynb](R-proteomics-Nrf1-R.ipynb) from within Jupyter Lab.
  - Run all cells.
- RStudio
  - [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/br3ndonland/R-proteomics-Nrf1/master?urlpath=rstudio) RStudio
  - Open [R-proteomics-Nrf1.Rmd](R-proteomics-Nrf1.Rmd) from within RStudio.
  - Click knit (at the top of the source code viewer).
  - The RStudio project file [R-proteomics-Nrf1.Rproj](R-proteomics-Nrf1.Rproj) can also be opened from within Binder RStudio, though I would discourage this. *Beware:* RStudio in Binder will recognize the Packrat library associated with the project, and will attempt to install all required packages. It could take up to an hour, in which time you could have already installed Anaconda, R, and RStudio on your computer.

## Results

![Volcano plot from R analysis comparing proteins in cholesterol-fed vs chow-fed liver](img/volcano-plot-chol.png)

Complement C1q proteins A, B, C (green dots in the plot above) were identified as potentially interacting with Nrf1 in the setting of liver cholesterol accumulation. The experiment did have notable limitations, which prompted us to refine our methods and continue with further experiments.

[(Back to TOC)](#table-of-contents)