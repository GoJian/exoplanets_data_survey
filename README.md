# Exoplanet Data Analysis Tools
This is a series of Plotly tools built to analyze the NASA Exoplanet Archive's Planetary Systems dataset.

(If you have any suggestinos, whether for this documentation or the programs themselves, please feel free to reach out to Dr. Jian Gong. If you're a programmer, feel free to copy this code and make your own improvments.)

## Installation
### Setup Python
 
1. Download and setup a conda environment using [miniforge](https://github.com/conda-forge/miniforge#miniforge3). Then, activate your conda environment at the command line terminal with:
 
```

conda activate

```
 
2. Using git to clone this github repository:
 
```

git clone git@github.com:GoJian/exoplanets_data_survey.git

```
 
For those unfamiliar with CLI, use a git GUI such as GitHub Desktop or the git interface in VS Code to clone the repo to your desired location.
 
3. Navigate to the 'exoplanets_data_survey' directory (`cd` in or open the directory in your IDE of choice) and issue the following command to create a new virtual environment called "exo" (You can change this name in the yml file. This is the name of your conda environment that we will activate later). It will pull all necessary libraries and dependencies together. We recommend [VS Code](https://code.visualstudio.com/download) as a good modern IDE.
 
4. Pull in all libraries described in the environment.yml file.
```

conda env create -f environment.yml

```
### Download data

5. Open setup.ipynb and run the file to download the necessary data. You will be asked for input.


## Tools
Principal Component Analysis (PCA.ipynb): A quick way to frontload the most important parts of a dataset with many variables into a few new ones. This program can create 3D and 2D PCA scatterplots, as well as a graph of the Explained and Cumulative Variance Ratios and the Feature Loadings for each PC.

Uniform Manifold Approximation Projection (UMAP.ipynb): While PCA isn't great at capturing non-linear relations, UMAP moves similar data points into clusters that can be easily identified, even without linear relations. The tradeoff is that it is slower than PCA, which is why it’s a separate program.

Histogram (histogram.ipynb): While the NASA Exoplanet Archive already has a histogram function, I’ve added additional features to this version, including grouping by factors other than discovery method, faceting the histograms by those groups, and comparing the percentage contributions.

Scatterplot (scatterplot.ipynb): A scatterplot function was also present on the NASA Exoplanet Archive, but I’ve added a 3d version and the same additional groups as the histogram function.

Starmap (starmap.ipynb): This program creates 2d and 3d spatial vizualizations of exoplanets in the dataset relative to Earth.

Compare Groups (grouptable.ipynb): a table used to compare the intersections of variables used to group exoplanets. 

## Usage
All of the tools are stored in the programs folder as .ipynb files. To run a program, select the fule and run the cell using Ctrl+Alt+Enter. Alongside a window popping up, you can enter the designated localhost to run it in a web browser.

Data filters: these can be used to filter out exoplanets that don't meet certain criteria.

Features: this is different between programs and not present in starmap or compare groups. For an exhausive list, see [this file](terms.md).

How to handle NaN values: Used in situations where the lack of values could impact the final graph.

Group by: Aside from colors, the mean and median are calculated separately for each group.

Extra options: Some additional changes to the graphs. Settings marked with "compare planets only" cannot be used with the "compare stars" setting.
