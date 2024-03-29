# bigau_probability

## Gaussian and Binomial Distributions
<p> This package contains code for some basic Gaussian and Binomial distribitions. For Gaussian distribution, you can calculate the mean and standard deviation from a sample input file. You can plot histograms from data and probability density functions (PDF). You can calculate PDF for a point,  add two gaussian instances and print a description for a gaussian instance.

# Installation
```python
pip install bigau-probability
```

### Gaussian Distribution Methods
#### Import
Before using the gaussian methods defined in this package, you have to import the Gaussian class 

```python
from bigau_probability import Gaussian
```


#### Instantiating Gaussian

A Gaussian object can be instantiated by passing in the mean and standard deviation parameters.Alternatively, it can be instantiated without parameters for example in the case that data is in another file. See examples below

```python
gaussian1 = Gaussian(5, 10)  # creates a gaussian distribution with mean of 5 and stdev of 10
gaussian2 = Gaussian() # creates a gaussian distribution with no parameters
```

#### Reading Data File
The ```read_data_file``` method is used for reading data from a file. This becomes very handy when you have quite a number of data to process. The expected data content are usually numbers, one per line. A sample data file is shown below <br>
1\
3\
99\
100\
120\
32\
330\
23\
76\
44\
31

The ```read_data_file``` method takes in a parameter, the name of the file containing data. Be sure to put the file in the same directory you are running your code from. Suppose the data above is stored in a <i>.txt</i> file called <i>gaussian.txt</i>, you would call the read_data_file method as shown below:<br>
```python
gaussian2.read_data_file('gaussian.txt')
```

#### Calculating mean
The ```calculate_mean``` method is used to calculate the mean of a gaussian distribution. It returns the mean of the distribution.<br>
```python
gaussian2.calculate_mean()
```

#### Calculating standard deviation
The calculate_stdev() method is used to calculate the standard deviation of a gaussian distribution. It returns the standard deviation of the distribution.<br>
```python
gaussian2.calculate_stdev()
```

#### Calculating probability density function
The ```pdf``` method is used for calculate the probability density function of a given value x. It takes a parameter x which is a number as input. It returns the probability density function of x.<br>
```python
gaussian2.pdf(50)
``` 

#### Plotting histogram
The ```plot_histogram``` method is used to display a histogram of the gaussian distribution. It uses mathplotlib for the plot.<br>
```python
gaussian2.plot_histogram()
```

#### Plotting histogram for probability distribution function
The ```plot_histogram_pdf``` is used  plot the normalized histogram of the data and a plot of the 
probability density function along the same range. It optional takes an integer that specifies the number of data points. If no parameter is passed, it uses a default value of 50. This method returns the x and y axis of the histogram besides showing the plot. <br>
```python
gaussian2.plot_histogram_pdf()
```



#### Adding two gaussian distributions
You can add two gaussian distributions by using the addition symbol (+). This will show the mean and standard deviation of the resultant gaussian distribution. <br>
```python
gaussian1 + gaussian2
``` 

#### Printing a gaussian object
The print method displays the mean and the standard deviation of a given gaussian distribution
```python
print(gaussian1)
```

### Binomial Distribution Methods
#### Import
Before using the binomial methods defined in this package, you have to import the Binomial class 

```python
from bigau_probability import Binomial
```


#### Instantiating Binomial

A Binomial object can be instantiated without parameters for example in the case that data is in another file. See examples below

```python
binomial = Binomial()  # creates a binomial distribution with no parameters
```

#### Reading Data File
The ```read_data_file``` method is used for reading data from a file. The expected data content are usually trial outcomes, one per line. For example, the tossing of a coin 13 times may have outcomes like the sample data shown below with 1 representing a head and 0 representing a tail.<br>

0\
1\
1\
1\
1\
1\
0\
1\
0\
1\
0\
1\
0

The ```read_data_file``` method takes in a parameter, the name of the file containing data. Be sure to put the file in the same directory you are running your code from. Suppose the data above is stored in a <i>.txt</i> file called <i>binomial.txt</i>, you would call the read_data_file method as shown below:<br>
```python
binomial.read_data_file('binomial.txt')
```

#### Generating stats from data
The ```replace_stats_with_data``` method is used to generate the probability and sample size from a given binomial data. It is recommended to call this method immediately a data file is read.
```python
binomial.replace_stats_with_data()
```


#### Calculating mean
The ```calculate_mean``` method is used to calculate the mean of a binomial distribution. It returns the mean of the distribution.<br>
```python
binomial.calculate_mean()
```

#### Calculating standard deviation
The calculate_stdev() method is used to calculate the standard deviation of a binomial distribution. It returns the standard deviation of the distribution.<br>
```python
binomial.calculate_stdev()
```

#### Plotting Barchart
The ```plot_bar``` method is used to display a barchar of the binomial distribution. It uses mathplotlib for the plot.<br>
```python
binomial.plot_bar()
```

#### Plotting Barchart for probability distribution function
The ```plot_bar_pdf```  method is used to plot a bar chart for the probability density function from  k = 0 to k = n This method returns the x and y axis of the barchart besides showing the plot. <br>
```python
binomial.plot_bar_pdf()
```


#### Adding two binomial distributions
You can add two binomial distributions by using the addition symbol (+). This will show the mean, standard deviation, probability and sample size of the resultant gaussian distribution. <br>
```python
binomial + binomial
``` 

#### Printing a gaussian object
The print method displays the mean, standard deviation, probability and sample size of a given binomial distribution
```python
print(binomial)
```

### Source Code
https://github.com/grace-omotoso/Bigau_Probability
