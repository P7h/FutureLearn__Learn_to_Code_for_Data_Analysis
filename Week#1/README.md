# Week 1: Having a go at it
---

## Jupyter Notebooks

### Jupyter Exercises Notebook
[http://www.open.edu/openlearnworks/mod/resource/view.php?id=77731](http://www.open.edu/openlearnworks/mod/resource/view.php?id=77731)


### Jupyter Project Notebook
[http://www.open.edu/openlearnworks/mod/resource/view.php?id=77733](http://www.open.edu/openlearnworks/mod/resource/view.php?id=77733)


## Data
This week's data file is [WHO POP TB some.xls](http://www.open.edu/openlearnworks/mod/resource/view.php?id=77732).


## Sections

### The basics of coding
Learn about the basic constituents that every program is made of, and how to use notebooks to code this week’s data analysis project using those constituents.

### Introducing tabular data
Learn how to represent and manipulate data more effectively as a table of rows and columns, how to compute simple statistics on individual columns and how to derive new columns from the existing data.

### Writing and sharing a data analysis
Learn how to write up a data analysis, how to extend the project, and how to share the results with others.


## Glossary
### Programming and data analysis concepts
* An *assignment* is a statement of the form `variable = expression`. It evaluates the expression and stores its value in the variable. The variable is created if it doesn’t exist. Each assignment is written on its own line.
* CamelCase is a naming style in which names made of various words have each word capitalized, except possibly the first.
* A comment is a note about the code. It starts with the hash sign (#) and goes until the end of the line.
* A dataframe is the pandas representation of a table.
* An expression is a fragment of code that can be evaluated, i.e. that has a value, like a variable name.
* A file not found error occurs if the computer can’t find the given file, e.g. because the name is misspelled or because it’s in another folder.
* A function takes zero or more arguments (values) and returns (produces) a value.
* A function call is an expression of the form `functionName(argument1, argument2, ...)`.
* An `import` statement of the form from module import * loads all the code from the given module.
* The `maximum` and `minimum` of a set of values is the largest and smallest value, respectively.
* The `mean` of a set of numbers is the sum of those numbers divided by how many there are.
* The `median` of a set of numbers is the number in the middle, i.e. half of the numbers are below the median and half are above.
* A method is a function that can only be called in a certain context, like a dataframe or a column.
* A method call is an expression of the form `context.methodName(argument1, argument2, ...)`.
* A module is a package of various pieces of code that can be used individually.
* A name is a case-sensitive sequence of letters, digits and underscores. Names cannot start with a digit. Function, variable and module names usually start with lowercase.
* A name error occurs if the computer doesn’t recognize a name, e.g. if it was misspelled.
* An operator is a symbol that represents some operation on one or two expressions, e.g. the four basic arithmetic operators.
* The range of a set of values is the difference between the maximum and the minimum.
* A reserved word cannot be used as a name. Jupyter shows reserved words in green boldface.
* A statement is a command for the computer to do something, e.g. to assign a value or to import some code.
* A string is a verbatim piece of text, surrounded by quotes. Jupyter shows strings in red.
* A syntax error occurs if the computer can’t understand the code because it is not in the expected form, e.g. if a reserved word is used instead of a name or some punctuation is missing.
* A variable is a named storage for values.

### Reserved words
* `from`
* `import`

### Functions and methods
* `max(value1, value2, ...)` returns the maximum of the given values.
* `column.max() returns the maximum value in the column.
* `min(value1, value2, ...)` returns the minimum of the given values.
* `column.min()` returns the minimum value in the column.
* `column.mean()` returns the mean of the values in the column.
* `column.median()` returns the median of the values in the column.
* `column.sum()` returns the total of the values in the column.
* `dataFrame.sort(columnName)` takes a string with a column’s name and returns a new dataframe, in which rows are sorted in ascending order according to the values in the given column.
* `read_excel(fileName)` takes a string with an Excel file name, reads the file, and returns a dataframe representing the table in the file.

