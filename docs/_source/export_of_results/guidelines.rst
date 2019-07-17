Export Guidelines
==================
Disclosure review means that ADRF staff will manually look at all your data output/study results which may be time consuming. Please limit the volume of your output requests for two reasons. One is that each additional release adds disclosure risk and limits subsequent releases. The other is that although we will try to release tables as quickly as possible, large requests are very time consuming and slow to review. To allow a quicker turnaround we ask you to follow the ADRF Export Guidelines:

Documentation
^^^^^^^^^^^^^^^^^^
Please structure your input and output folders to enable ADRF Staff to find information quickly if needed. For example you can have one folder in which you store all the code, one folder for graphs, one folder for data, etc. If you have multiple files of code which depend on each other please name them in a way that is is visible which files runs first, second, etc. (1_DataPrep.py, 2_SummaryStats.py, 3_MultivarAnalyses.py).

Think about meaningful names to allow inference on the content of the file. This also applies to variables. For instance, if you are calculating outflows it is better to name the variable outflows instead of var1. Every file of code should have a header including a description of the content of the file, a timestamp, and what kind of data manipulation takes place. The more detailed your documentation the easier it is for ADRF staff to follow your study during disclosure control.

Code documentation is helpful for disclisure reviews. The better the documentation the faster the turnaround of export requests. In particular when you aggregate data files. In this case we require documentation on the level of aggregation and during which step in the program the aggregation took place (specify in code).

Required Information
^^^^^^^^^^^^^^^^^^
Please denote the unit of analysis clearly in your programs (individuals, regions, etc.). During disclosure review cell sizes represented with less than 10 individuals will be suppressed. Thus for each cell in the table (or the source data underlying any graph representation), provide the counts of each entity (n) and the percentage (p) of any value accounted for by the top 4 (k) entities. Some helpful hints are provided in the checklist below.

For each statistic you want to be released we need the count of entities who are underlying this statistic. In case you generate aggregates we need the number of entities in each aggregate. If the aggregate is a ratio, the number of valid cases has to be computed for each subgroup of the aggregate (e.g. number of men in state X and number of women in state X in addition to the ratio of women in state X). For descriptive statistics: always report mean, min, max, and total number of observations. Do not include unit record data in programming code and logs.


Checklist for Output 
^^^^^^^^^^^^^^^^^^

#. Tabular Output

	* General Rule: No cell should have fewer than 10 observations.

	* Aggregation: If a table contains sensitive cells, a method you can use to protect these cells is to aggregate (collapse) those categories (see the Jupyter Notebook for examples).

	* Suppression: When sensitive cells still occur and no further grouping is appropriate, the procedure is to suppress the cell (remove its value), then suppress other cells to stop the first cell from being determined. This later stage is called secondary suppression

	* Secondary Suppression: Secondary suppression is the suppression of other cells or marginal totals in the table so that the suppressed cell cannot be recalculated. There are no universal guidelines for applying secondary suppression, except that there has to be enough secondary suppression to ensure that primary suppressed values

	* Percentages: You may calculate percentages, proportions, and ratios using the unrounded counts. However, suppress percentages, proportions, or ratios where either, or both, of the counts used to calculate the percentage, proportion, or ratio have been suppressed. Round percentages calculated from unweighted counts to 1 decimal places. Do not report 0 or 100%.

	* Medians: Do not report medians. You can calculate a fuzzy median by averaging the 45 and 55 percentile.

	* Maxima and minima: Suppress maximum and minimum values in general. Where a maximum or minimum value is not identifying, it may be considered for release

#. Regression Output

	* Regression output does not usually have confidentiality issues. However, you need to check that pieces of output are not equivalent to, or based on, small counts. Only report the necessary coefficients and list the control variables.

#. Graphs

	* Type A: Graphs produced from aggregated data, or tables that have been confidentialised (eg frequency histograms, bar charts of magnitudes). Provide the underlying tables
	* Type B: Graphs produced directly from the unit record data, but aggregated in the process by the software (eg frequency histograms, kernel density plots). Provide the underlying tables
	* Type C: Graphs produced directly from the unit record data, and displaying unit record values (eg scatterplots, residual plots). For this type of graph to be released, you need to ensure that individuals cannot be recognised and that values can only be estimated with a high level of uncertainty- Further processing can include, but is not restricted to: cutting off the tails of a distribution, removing outliers, jittering the actual values, and removing or modifying axis values
	* Type D: Graphs produced from the results of modelling or derivation that use the unit record data (eg regression curves) – Release only if the values cannot be used to find original data values
