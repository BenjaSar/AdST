![header](doc/imgs/LogoHeader.png)
## Time Series Analysis - US Population Analysis

#### Overview
This project analyzes the US population time series data from 2011-2018 using various statistical methods and models. The analysis includes data preprocessing, stationarity tests, seasonal decomposition, and SARIMA modeling.

```
├── README.md
├── requirements.txt
├── uspopulation.csv          # Main dataset
├── tp_final.ipynb           # Main analysis notebook
└── doc/
    └── imgs/                # Documentation images
```

#### Dataset
The analysis uses monthly US population estimates from 2011 to 2018. The data includes:

* Time period: 96 months (2011-01 to 2018-12)
* Values range: 311,037 to 328,393 thousand people
* Monthly frequency

### Analysis Components
1. Data Preprocessing
* Loading and initial exploration of the time series data
* Handling missing values and duplicates
* Outlier detection using z-scores
* Log transformation
2. Time Series Analysis
* Stationarity testing using Augmented Dickey-Fuller (ADF) test
* Seasonal decomposition
ACF and PACF analysis
* First and seasonal differencing
3. SARIMA Modeling
* Model selection using ACF/PACF plots
* Implementation of SARIMA(0,1,0)(0,1,0,12) model
* Model evaluation using:
    * AIC: -1240.496
    * BIC: -1238.262
    * Log Likelihood: 621.248

4. Auto ARIMA
* Automated model selection using $\textit{pmdarima}$
Parameter ranges:
* $max_p=3, max_q=3$ (non-seasonal)
* $max_P=2, max_Q=2$ (seasonal)
* $m=12$ (seasonal period)

#### Requirements
The analysis requires the following Python packages:

* pandas
* numpy
* matplotlib
* seaborn
* statsmodels
* pmdarima
* scikit-learn

##### Authors:
- FS

##### License
MIT License ©
![footer](doc/imgs/LogoFooter.png)
