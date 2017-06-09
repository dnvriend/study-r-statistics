# study-r-statistics
A small study project on [statistics](https://en.wikipedia.org/wiki/Statistics) with the [R-programming language](https://www.r-project.org/).

## What is statistics?
[Statistics](https://en.wikipedia.org/wiki/Statistics) is a branch of mathematics dealing with the collection, analysis, interpretation, presentation, and organization of data. In applying statistics to, e.g., a scientific, industrial, or social problem, it is conventional to begin with a statistical population or a statistical model process to be studied. Populations can be diverse topics such as "all people living in a country" or "every atom composing a crystal." Statistics deals with all aspects of data including the planning of data collection in terms of the design of surveys and experiments.

## What is the R-programming language?
R is an open source programming language and software environment for statistical computing and graphics that is supported by the R Foundation for Statistical Computing. The R language is widely used among statisticians and data miners for developing statistical software and data analysis. Polls, surveys of data miners, and studies of scholarly literature databases show that R's popularity has increased substantially in recent years.

R is a GNU package.[10] The source code for the R software environment is written primarily in C, Fortran, and R.[11] R is freely available under the GNU General Public License, and pre-compiled binary versions are provided for various operating systems. While R has a command line interface, there are several graphical front-ends available.[12]

## What is RStudio?
[RStudio](https://www.rstudio.com/products/rstudio/) is an integrated development environment (IDE) for R. It includes a console, syntax-highlighting editor that supports direct code execution, as well as tools for plotting, history, debugging and workspace management. RStudio makes it easy to work with R and I will use it for my studies.

## What is the Scientific Method?
The [scientific method](https://en.wikipedia.org/wiki/Scientific_method) is a body of techniques for investigating phenomena, acquiring new knowledge, or correcting and integrating previous knowledge. To be termed scientific, a method of inquiry is commonly based on empirical or measurable evidence subject to specific principles of reasoning. The Oxford Dictionaries Online define the scientific method as "a method or procedure that has characterized natural science since the 17th century, consisting in systematic observation, measurement, and experiment, and the formulation, testing, and modification of hypotheses". Experiments need to be designed to test hypotheses. The most important part of the scientific method is the experiment.

The scientific method is a continuous process, which usually begins with observations about the natural world. Human beings are naturally inquisitive, so they often come up with questions about things they see or hear and often develop ideas (hypotheses) about why things are the way they are. The best hypotheses lead to predictions that can be tested in various ways, including making further observations about nature. In general, the strongest tests of hypotheses come from carefully controlled and replicated experiments that gather empirical data. Depending on how well the tests match the predictions, the original hypothesis may require refinement, alteration, expansion or even rejection. If a particular hypothesis becomes very well supported a general theory may be developed.

## The Scientific Method and Statistics
The scientific method has been extremely successful in bringing the world out of medieval thinking, especially once it was combined with industrial processes. However, when the scientific method employs statistics as part of its arsenal, there are mathematical and practical issues that can have a deleterious effect on the reliability of the output of scientific methods. This is described in a popular 2005 scientific paper ['Why Most Published Research Findings Are False' by John Ioannidis](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1182327/).

The particular points raised are statistical ("The smaller the studies conducted in a scientific field, the less likely the research findings are to be true" and "The greater the flexibility in designs, definitions, outcomes, and analytical modes in a scientific field, the less likely the research findings are to be true.") and economical ("The greater the financial and other interests and prejudices in a scientific field, the less likely the research findings are to be true" and "The hotter a scientific field (with more scientific teams involved), the less likely the research findings are to be true.") Hence: "Most research findings are false for most research designs and for most fields" and "As shown, the majority of modern biomedical research is operating in areas with very low pre- and poststudy probability for true findings." However: "Nevertheless, most new discoveries will continue to stem from hypothesis-generating research with low or very low pre-study odds," which means that *new* discoveries will come from research that, when that research started, had low or very low odds (a low or very low chance) of succeeding. Hence, if the scientific method is used to expand the frontiers of knowledge, research into areas that are outside the mainstream will yield most new discoveries.

## What is the Mean?
In mathematics, [mean](https://en.wikipedia.org/wiki/Mean) has several different definitions depending on the context.

In probability and statistics, 'population mean' and 'expected value' are used synonymously to refer to 'one measure of the central tendency either of a probability distribution or of the random variable characterized by that distribution'. In the case of a discrete probability distribution of a random variable X, the mean is equal to the sum over every possible value weighted by the probability of that value; that is, it is computed by taking the product of each possible value x of X and its probability P(x), and then adding all these products together. An analogous formula applies to the case of a continuous probability distribution. Not every probability distribution has a defined mean; see the Cauchy distribution for an example. Moreover, for some distributions the mean is infinite denoted by "mu".

For a data set, the terms 'arithmetic mean', 'mathematical expectation', and sometimes 'average' are used synonymously to refer to a 'central value of a discrete set of numbers': specifically, the sum of the values divided by the number of values. The arithmetic mean of a set of numbers x1, x2, ..., xn is typically denoted by "x bar". If the data set were based on a series of observations obtained by sampling from a statistical population, the arithmetic mean is termed the sample mean denoted by "x bar" to distinguish it from the population mean denoted by "mu".

For a finite population, the population mean of a property is equal to the arithmetic mean of the given property while considering every member of the population. For example, the population mean height is equal to the sum of the heights of every individual divided by the total number of individuals. The sample mean may differ from the population mean, especially for small samples. The law of large numbers dictates that the larger the size of the sample, the more likely it is that the sample mean will be close to the population mean.

### Example:
To calculate the [mean](http://www.r-tutor.com/elementary-statistics/numerical-measures/mean):

```
> x = c(2, 3, 4, 7, 9)
> mean(x)
[1] 5
```

## What is Standard Deviation (SD)?
In statistics, the [standard deviation](https://en.wikipedia.org/wiki/Standard_deviation) (SD, also represented by the Greek letter sigma σ or the Latin letter s) is a measure that is used to quantify the amount of variation or dispersion of a set of data values. A low standard deviation indicates that the data points tend to be close to the mean (also called the expected value) of the set, while a high standard deviation indicates that the data points are spread out over a wider range of values.

### Example:
To calculate the [standard deviation](http://www.r-tutor.com/elementary-statistics/numerical-measures/standard-deviation):

```
> x = c(2, 3, 4, 7, 9)
> sd(x)
[1] 2.915476
```

## Statistical Functions
Useful statistical functions are provided in the following table. Each has the option na.rm to strip missing values before calculations. Otherwise the presence of missing values will lead to a missing result. Object can be a numeric vector or data frame.

| Function | Description |
| -------- | ----------- |
| mean(x, trim=0, na.rm=FALSE) | mean of object x |
| sd(x) | standard deviation of object(x). also look at var(x) for variance and mad(x) for median absolute deviation. |
| median(x)	| median |
| quantile(x, probs) | quantiles where x is the numeric vector whose quantiles are desired and probs is a numeric vector with probabilities in [0,1] |
| range(x) | range |
| sum(x) | sum |
| diff(x, lag=1) | lagged differences, with lag indicating which lag to use |
| min(x) | minimum |
| max(x) | maximum |
| scale(x, center=TRUE, scale=TRUE)	| column center or standardize a matrix. |

Example:

```
mx <- mean(x,trim=.05,na.rm=TRUE)
# trimmed mean, removing any missing values and 
# 5 percent of highest and lowest scores 

# 30th and 84th percentiles of x
y <- quantile(x, c(.3,.84))
```

## Courses
- [Coursera - Basic Statistics](https://www.coursera.org/learn/basic-statistics)
- [Coursera - Statistics with R](https://www.coursera.org/specializations/statistics)

## Videos
- [Getting Started With R - Mike Marin](https://www.youtube.com/watch?v=riONFzJdXcs&list=PLqzoL9-eJTNARFXxgwbqGo56NtbJnB37A)
- [Calculate Statistical Mean with R - Edward Kench](https://www.youtube.com/watch?v=SYh6vHPjBBs)
- [Find Median Value with R - Edward Kench](https://www.youtube.com/watch?v=kl3BifSwXo4)
- [Standard Deviation with R - Edward Kench](https://www.youtube.com/watch?v=nkmfHREo8iY)
- [Five number summary, quartiles, and boxplots with R - Edward Kench](https://www.youtube.com/watch?v=fLndTRunNdw)

## Resources
- [Producing Simple Graphs with R](http://www.harding.edu/fmccown/r/)
- [Quick R - Built-in Functions](http://www.statmethods.net/management/functions.html)