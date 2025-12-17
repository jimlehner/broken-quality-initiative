![Broken quality logo vertical - no subtitle test](https://github.com/user-attachments/assets/d00b7ed8-5ad1-4d87-951c-e2d8e5432393)

Welcome to the official GitHub repository of The Broken Quality Initiative [www.brokenquality.com](https://www.brokenquality.com/). Here, you'll find the datasets and Python code associated with the essays found on the [Broken Quality Bookshelf](https://www.brokenquality.com/bookshelf). 

The datasets found in the [data folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/data) use the following naming convetion:

**essay_name-dataset_name**

As an example, the dataset associated with the essay **Network Analysis: Advancing the utility of SPC** has the name **network_analysis_advancing_spc-manufacturing_process_data**.

The code used to generate the figures found in each essay are named in accordance with the the essay. These files can be found in the [Python code folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/code).

## Table of Contents

1. [Essays](#essays)
2. [How to use this repository](#how-to-use-this-repository)
3. [Bias correction and scaling factor tables](#bias-correction-and-scaling-factor-tables)
4. [Filing bugs](#filing-bugs)
5. [Contributing](#contributing)
6. [About The Broken Quality Initiative](#about-the-broken-quality-initiative)
7. [Contact](#contact)

## Essays
The essays on The Broken Quality Initiative Bookshelf include:
- **The definition of quality**: Quality has become an overused term of little substance. This essay is about how the current state of quality came to be and what we can do to fix it. There is no dataset associated with this essay. [The definition of quality](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a11f3deb559c2a30f66348/1738612541895/The+definition+of+quality.pdf)
- **Understanding the process capability indices**: The process capability indices have become a standard method by which processes are graded. This essay explains the process capability indices and the context that is required to put them to use. [Understanding the process capability indices](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a113ff741c0305cbcaf1db/1738609665034/Understanding+the+process+capability+indices.pdf)
- **On writing, reports, & process behavior charts**: An essay outlining the advantages of written reports over PowerPoint. [On writing, reports, & process behavior charts](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/678682b0985aa0078fb3b983/1736868529394/On-writing-reports-and-process-behavior-charts.pdf)
- **Network Analysis: Advancing the utility of SPC**: Network analysis updates the tried and true methods of Statistcal Process Control (SPC) and process behavior charts (control charts) such that they reflect the modern business and industrial ecosystems. [Network Analysis: Advancing the utility of SPC](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/679910513be40134de9b54f7/1738084433790/Network+analysis.pdf)
- **What the spec?**: An essay explaining the practical differences of process limits and specification limits. [What the spec?](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a12bc5d98a6f4c49d1a4a4/1738615750105/What+the+spec.pdf)
- **The importance of context: How process behavior charts imbue meaning**: Without context, data is random and miscellaneous. This essay articulates how process behavior charts establish context and imbue meaning better than any other method or tool. [The importance of context](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a61713095e3d696e01d614/1738938132289/The+importance+of+context.pdf)
- **Poverty & Improvement**: Process behavior charts (control charts) are not limited to industrial applications. This essay serves as an example of the process behavior charts utility to social problems. [Poverty & Improvement](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a61be65845e420dcc8c0b3/1738939366795/Poverty+and+improvement.pdf)
- **Network analysis of supplier On-Time Delivery (OTD)**: On-Time Delivery (OTD) is a common supplier quality metric. This essay expands on the utility of OTD using a network analysis. [Network analysis of supplier on-time delivery](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a635232700da46098b6d60/1738945828468/Network+analysis+of+supplier+on+time+delivery.pdf)
- **Supplier Quality Ratios**: Manufacturing in modern industry is often executed across global networks of suppliers and customers. This essay outlines an alternative method for understanding supplier quality. [Supplier Quality Ratios](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/6789790261af002ec3b0edd6/1737062659434/Supplier-quality-ratios.pdf) 
- **Same parts, new supplier**: This essay serves as an example of how to evaluate legacy parts produced by a new supplier. [Same parts, new supplier](https://static1.squarespace.com/static/5b722db6f2e6b1ad5053391b/t/67a64c21fe4e8d2763b7aa06/1738951714572/Same+parts+new+supplier.pdf)

## How to use this repository
Inside this repository you'll find the datasets and code associated with the essays found on [](https://www.brokenquality.com/bookshelf). As outlined above, the datasets associated with each essay can be found in the [data folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/data) and are labeled in accordance with the naming convention `essay_name-dataset_name`. The code for each essay, found in the [code folder](https://github.com/jimlehner/broken-quality-initiative/tree/main/code), is labeled in accordance with the naming convetion **essay_name_code**.

## Bias correction and scaling factor tables
The **bias correction factor table** contains the values for the factors that convert the average ranges and median ranges into the appropriate measures of dispersion, namely, either *Sigma(X)*, *Sigma($\overline{X}$)*, or *Sigma(R)*. For details on how these values are calculated see [Monte Carlo simulation for determining bias correction factors](https://github.com/jimlehner/understanding-variation/projects).

The two scaling factors tables (*average-range-chart-scaling-factors-using-average-range.csv* and *average-range-chart-scaling-factors-using-median-range.csv*), should be used to determine the value of the respective scaling factors based on subgroup size when building an Average and Range chart.

### Scaling factors for Average and Range chart using the average range, $ \overline{R} $
Given *k* subgroups each with *n* observations with grand average, and average range, use the tabled constants in *average-range-chart-scaling-factors-using-average-range.csv*.

Limits for subgroup averages for an Average and Range chart using the **average range** are obtained from:

$$ \text{UAL}_{\overline{X}} = \overline{\overline{\text{X}}} + A_2 \cdot \overline{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{\overline{X}} $$
$$ \text{LAL}_{\overline{X}} = \overline{\overline{\text{X}}} - A_2 \cdot \overline{\text{R}} $$

Limits for subgroup ranges for an Average and Range chart using the **average range** are obtained using the formulas:

$$ \text{URL}_{R} = D_4 \cdot \overline{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{R} $$
$$ \text{LRL}_{R} = D_3 \cdot \overline{\text{R}} $$

Natural process limits for individual values may be obtained using the formulas:

$$ \text{UPL}_{X} = \overline{\overline{\text{X}}} + E_2 \cdot \overline{\text{R}} $$
$$ \text{CL}_{X} = \overline{\overline{X}} $$
$$ \text{LPL}_{X} = \overline{\overline{\text{X}}} - E_2 \cdot \overline{\text{R}} $$

The formulas for the scaling factors in *average-range-chart-scaling-factors-using-average-range.csv* are:

$$ \text{A}_{2} = \frac{3}{d_2 \sqrt{n}} $$
$$ \text{D}_{3} = 1 - (\frac{3\cdot\text{d}_3}{d_2}) $$
$$ \text{D}_{4} = 1 + (\frac{3\cdot\text{d}_3}{d_2}) $$
$$ \text{E}_{2} = \frac{3}{d_{2}} $$

### Scaling factors for Average and Range chart using the median range, $ \tilde{R} $
Given *k* subgroups each with *n* observations with grand average, and average range, use the tabled constants in *average-range-chart-scaling-factors-using-median-range.csv*.

Limits for subgroup averages for an Average and Range chart using the **median range** are obtained from:

$$ \text{UAL}_{\overline{X}} = \overline{\overline{\text{X}}} + A_4 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{\overline{X}} = \overline{\overline{X}} $$
$$ \text{LAL}_{\overline{X}} = \overline{\overline{\text{X}}} - A_4 \cdot \tilde{\text{R}} $$

Limits for subgroup ranges for an Average and Range chart using the **median range** are obtained using the formulas:

$$ \text{URL}_{R} = D_6 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{R} = \tilde{R} $$
$$ \text{LRL}_{R} = D_5 \cdot \tilde{\text{R}} $$

Natural process limits for individual values may be obtained using the formulas:

$$ \text{UPL}_{X} = \overline{\overline{\text{X}}} + E_5 \cdot \tilde{\text{R}} $$
$$ \text{CL}_{X} = \overline{\overline{X}} $$
$$ \text{LPL}_{X} = \overline{\overline{\text{X}}} - E_5 \cdot \tilde{\text{R}} $$

The formulas for the scaling factors in *average-range-chart-scaling-factors-using-median-range.csv* are:

$$ \text{A}_{4} = \frac{3}{d_2 \sqrt{n}} $$
$$ \text{D}_{5} = 1 - \frac{d_{2} - 3\text{d}_3}{d_4} $$
$$ \text{D}_{6} = \frac{d_{2} - 3\text{d}_3}{d_4} $$
$$ \text{E}_{5} = \frac{3}{d_{4}} $$

## Filing Bugs
Although we strive to realize it, we know perfection is difficult to attain. If you encounter any issues or errors in the book or code samples, please don't hesitate to file a bug in the [Issues](https://github.com/jimlehner/broken-quality-initiative/issues) section of this repository. When filing an issue please include as much detail as possible including the chapter, page, number, descirption of the issue, and, if relevant, a screenshot or code snippet.

## Contributing
Contributions from our readers are welcomed and appreciated. If you've discovered an error or a way to improve the code, feel free to create a pull request. For signficant changes, please open an issue first to discuss the proposed changes. 

## About The Broken Quality Initiative
**The Broken Quality Inititiave** aims to address industries pervasive lack of knowledge of variation of variation and the only tool capable of making sense of variation, the process behavior chart (control chart).

The lack of knowledge of variation is reflected in the often haphazard, disorganized, and chaotic way  individuals, teams, and organizations attempt to improve quality and reduce costs. Rather than work to understand and eliminate the sources of variation that make processes unpredictable, inordinate amounts of time and attention are dedicated to gut feelings and guess work. While this sentiment is often accompanied by best efforts and hard work, the lack of theory to guide actions reliably digs the hole deeper.  

Since the mid-1920s, with the seminal work of Dr. Walter Shewhart at Bell Labs, a method and tool capable of making sense of data has been at our fingertips. It is due time that industry put to work what Shewhart discovered more than 100 years ago. It is due time that individuals, teams, and organizations learn to turn data into insights and insights into actions that result in change using process behavior charts.

Visit [BrokenQuality.com](https://www.BrokenQuality.com/bookshelf) for resources and more details regarding the application and use of **process behavior charts**.

## Contact
If you have questions or would like to collaborate email **James.Lehner@gmail.com** or **thebrokenqualityinitiative@gmail.com**.
