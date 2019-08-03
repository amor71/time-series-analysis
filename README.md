# time-series-analysis

### Overview

Most events may be viewed, or converted to time-series. The purpose of this project is to provide tools to analyze time-series for the purpose of estimating "Roughness", "Fractal Dimension" and help create some intuition of the predictability and exposure to extremities.  

### Project Structure & Setup

```
- datasets/
    (folder holding datasets)
- generators/ 
    (Jupyter Notebooks for generating datasets)
- viewers/
    (folder holding various dataset viewers)
- analyzers/
    (folder holding various dataset analysis tools)
```

Install requirements by:
 
`pip install -r requirements.txt`


### Generators

* `generator_randomwalk` : Notebook for generating a random walk dataset. Data is written into the `datasets` folder, as CSV file. Filename include `rw` prefix and timestamp. The notebook includes basic visualization and analysis of the generated walk.

* `generator_whitenoise` : Notebook for generating a "white noise" dataset. Data is written into the `datasets` folder, as CSV file. Filename include `wn` prefix and timestamp. The notebook includes basic visualization and analysis of the generated series.

* `generator_basic_fractal`: Notebook for generating a basic "fractal" dataset. The Fractal is generated around a random trend-line to simulate financial data. Data is written into the `datasets` folder, as CSV file. Filename include `bf` prefix and timestamp. The notebook includes basic visualization and analysis of the generated series.

### Viewers

* `basic`: Notebook w/ basic visualization for a dataset.

* `powers`: Notebook for comparison between the dataset and various functions, viewing on various scales to provide intuition on the dataset power and behavior.

### Analysers 

* `Hurst Exponent`: Notebook for calculating H (Hurst Exponent) 

* `DFA`: Notebook that calculates Detrended fluctuation analysis (DFA) - an extension to H exponent. Helpful for understanding auto-correlation, fracal dimension. 

## ToDo

* Add analysis for ACF
* add generators for step, sin and similar processes
* add FT
* Add multi fractal generator
* Add Mandelbrot Financial analysis
* Calc H and DFA over time/scale calc parameters
* integrate w/ external APIs for market data

