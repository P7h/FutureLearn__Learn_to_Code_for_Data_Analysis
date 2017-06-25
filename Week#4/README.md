# Week 4: Further Techniques
---

## Jupyter Notebooks

### Jupyter Exercises Notebook
[http://www.open.edu/openlearnworks/mod/resource/view.php?id=77739](http://www.open.edu/openlearnworks/mod/resource/view.php?id=77739)

### Jupyter Project Notebook
[http://www.open.edu/openlearnworks/mod/resource/view.php?id=77741](http://www.open.edu/openlearnworks/mod/resource/view.php?id=77741)

### Side project
Also tried a small project for understanding Gross Domestic Product [GDP] per capita based on Purchasing-Power-Parity [PPP]. [GDP_PPP_Project.ipynb](GDP_PPP_Project.ipynb) is the Jupyter Notebook for this project.


## Data
* [`comtrade_milk_uk_monthly_14.csv`](comtrade_milk_uk_monthly_14.csv). Or is available [here](http://www.open.edu/openlearnworks/mod/resource/view.php?id=81700) and also (`comtrade_pivot.html`)[http://www.open.edu/openlearnworks/mod/resource/view.php?id=77740].
* [`comtrade_milk_in_monthly_16.csv`]("comtrade_milk_in_monthly_16.csv"). Or is available [here](https://comtrade.un.org/api/get?max=50000&type=C&freq=M&px=HS&ps=2016&r=699&p=all&rg=all&cc=0401&fmt=csv).
* [`comtrade_milk_uk_jan_jul_15.csv`]("comtrade_milk_in_monthly_16.csv"). Or is available [here](http://www.open.edu/openlearnworks/mod/resource/view.php?id=81699).


## Sections

### What is grouping?
* Explore why one might want to group data, by looking at international trade data.

### Split, apply, combine
* Learn how to systematically transform data with the split-apply-combine pattern and how to use the pattern with pandas.

### Pivot tables
* Learn how to reorganise tabular data.


## Glossary

### Concepts
* An API, or application programming interface provides a way for computer programmes to make function or resource requests from a software application. Many online applications provide a web API that allows requests to be made over the internet using web addresses or URLs (uniform resource locator). A URL may include several parameters that act as arguments used to pass information into a function provided by the API. To prevent ambiguity, simple punctuation is avoided in URLs. Instead, ‘websafe’ encodings using the ASCII encoding scheme are typically used to describe punctuation characters.
* The notion of *grouping* refers to the collecting together of sets of rows based on some defining characteristic. Grouping on one or more key columns splits the dataset into separate groups, one group for each unique combination of values that appears in the dataset across the key columns. Note that not all possible combinations of cross-column key values will necessarily exist in a dataset.
* The *split-apply-combine* pattern describes a process in which a dataset is _split_ into separate groups, some function is _applied_ to the members of each separate group, and the results then _combined_ to form an output dataset.

### Functions and methods
* `df.to_csv(filename,index=False)` writes the contents of the dataframe `df` to a CSV file with the specified filename in the current folder. The `index` parameter controls whether the dataframe index is included in the output file.
* `read_csv(URL,dtype={})` can be used to read a CSV file in from a web location given the web address or URL of the file. We also made use of an additional parameter, `dtype` to specify the data type of specified columns in a dataframe created from a CSV file.
* `df.groupby(columnName)` or `df.groupby(listOfColumnNames)` is used to split a dataframe into separate groups indexed by the unique values of `columnName` or unique combinations of the column values specified in the `listOfColumnNames`.
* `grouped.get_group(groupName)` is used to retrieve a particular group of rows by group name from a set of grouped items.
* `grouped.groups.keys()` is used to retrieve the names of groups that exist within a set of grouped items.
* `grouped.aggregate(operation)` applies a specified operation to a group (such as `sum`) and then combines the results into a single dataframe indexed by group.
* `grouped.apply(myFunction)` will apply a user defined function to the rows associated with each group in a set of grouped items and return a dataframe containing the combined rows returned from the user defined function.
* `grouped.filter(myFilterFunction)` will apply a user defined filtration function to each group in a set of grouped items that tests each group and returns a Boolean True or False value to say whether each group has passed the filter test. The `.filter()` function then returns a single dataframe that contains the combined rows from groups that the user defined filter function let through.
* `pivot_table(df, index=indexColumnNames, columns=columnsColumnNames, values=valueColumnName, aggfunc=aggregationFunction)` generates a pivot table from a dataframe using unique combinations of values from one or more columns specified by the `indexColumnNames` list to define the row `index` and unique combinations of values from one or more columns specified by the `columnsColumnNames` list to define the columns. The pivot table cells are calculated by applying the `aggfunc` function to the `valueColumnName` column in the group of rows associated with each cell.

### Notes on `merge`, `join`, `concat` and `append`
* [https://pandas.pydata.org/pandas-docs/stable/merging.html](https://pandas.pydata.org/pandas-docs/stable/merging.html)
* Main differences between `df.join()` and `df.merge()`:
	* Lookup on right table: `df1.join(df2)` always joins via the index of `df2`, but `df1.merge(df2)` can join to one or more columns of `df2` (default) or to the index of `df2` (with `right_index=True`).
	* lookup on left table: by default, `df1.join(df2)` uses the index of `df1` and `df1.merge(df2)` uses column(s) of `df1`. That can be overridden by specifying `df1.join(df2, on=key_or_keys)` or `df1.merge(df2, right_index=True)`.
	* left vs inner join: `df1.join(df2)` does a left join by default (keeps all rows of `df1`), but `df.merge` does an inner join by default (returns only matching rows of `df1` and `df2`).
