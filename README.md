# Day-079--t-Tests-and-Distributions--The-Tragic-Discovery-of-handwashing
T-test with Scipy, Distributions with Numpy, Pandas, Matplotlib, Plotly, Seaborn

- How to use histograms to visualise distributions
- How to superimpose histograms on top of each other even when the data series have different lengths
- How to use a to smooth out kinks in a histogram and visualise a distribution with a Kernel Density Estimate (KDE)
- How to improve a KDE by specifying boundaries on the estimates
- How to use scipy and test for statistical significance by looking at p-values
- How to highlight different parts of a time series chart in Matplotib
- How to add and configure a Legend in Matplotlib
- Use NumPy's .where() function to process elements depending on a condition


Scipy (scipy.stats):
- stats.ttest_ind() --> calculate the 't-statistic' and 'p-value' (tuple)
  - if p-value is small (under 1 %) --> difference is statistically significant !!!
  --> this means it is not coincidence the difference is high

Numpy (np):
- .where('condition', 'a', 'b') --> function that does 'a' if condition is True and does 'b' if condition is False

Pandas (pd):
- .loc['condition'] --> get only the Data that correspond to condition
- .rolling() --> to smooth out the time-series Data (no spikes in a chart, shows the trend)

Matplotlib (plt):
- .plot
- .twinx() --> two independent y-axis
- .xaxis.set_minor_locator() --> set tick locators on a x-axis (Matplotlib.Axes)
- .legend() --> create a legend

Plotly (px):
- .line() --> create line chart
- .box() --> create box chart
- .histogram() --> create histogram
  - .histogram(histnorm='percent') --> to make the time periods comparable (if one category has much more Data than the other one)
  - .histogram(barmode='overlay') --> overlay tho histograms (for example: two different categories)
  - .histogram(marginal='box') --> shows the box chart above the histogram
  
Seaborn (sns):
- .kdeplot() --> two kernel density (similar to histogram, but this shows continuous trend (not discrete bins))
  - .kdeplot(shade=True) --> shades the area under the graph
  - .kdeplot(clip(low, high)) --> sets limits (low, high) to clip (out) the "weird" Data


