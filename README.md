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

* `generator_randomwalk` : generating a random walk datas-et. Data is written into the `datasets` folder, as CSV file. Filename include `rw` prefix and timestamp. The notebook includes basic visualization and analysis of the generated walk.

* `generator_whitenoise` : generating a "white noise" data-set. Data is written into the `datasets` folder, as CSV file. Filename include `wn` prefix and timestamp. The notebook includes basic visualization and analysis of the generated series.

* `generator_basic_fractal`: generating a basic "fractal" data-set. The Fractal is generated around a random trend-line to simulate financial data. Data is written into the `datasets` folder, as CSV file. Filename include `bf` prefix and timestamp. The notebook includes basic visualization and analysis of the generated series.

* `generator_pink_noise`: generating a "pink noise" data-set. Data is written into the `datasets` folder, as CSV file. Filename include `pn` prefix and timestamp. The notebook includes basic visualization and analysis of the generated series.

### Viewers

* `basic`: Notebook w/ basic visualization for a data-set.

* `powers`: Notebook for comparison between the data-set and various functions, viewing on various scales to provide intuition on the dataset power and behavior.

* `stationary-vs-non-stationary`: calculates and presents the mean and variance of the timeseries over time. Identify weak-stationary-process using auto-covariance. The presentation should help forming an intuition of the timeseries is a result of a stationary or non-stationary process. 

* `lag view (iid analysis)`: presents lag plot of the time-series, with lag 1, 2, 4, 8, 16 (1 & 2 lags also showed w log scale). The view is helpful to get some basic intuition on the independeance assumption of the time series, and the autocorrelation

* `deltas`: present visualizations of the time-series deltas, as well as visualized the probability for a streak of upwards and downwards trends. For financial time-series, helps to form intuition on volatility and decision making processes.

### Analysers 

* `Hurst Exponent`: Notebook for calculating H (Hurst Exponent) 

* `DFA`: Notebook that calculates Detrended fluctuation analysis (DFA) - an extension to H exponent. Helpful for understanding auto-correlation, fracal dimension. 

* `auto-correlation`: Calculates the auto-covariance of the time-series, and uses the calculations to calculate and presents the auto-correlation frequency.



