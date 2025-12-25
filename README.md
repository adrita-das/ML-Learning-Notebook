## Pandas Iris Dataset Notes

This repository contains practice notes and examples using Pandas with the Iris dataset.
The focus is on data aggregation, ranking, and basic statistical concepts commonly used in data analysis.

 **pandas.DataFrame.agg()**

The `pandas.DataFrame.agg()` method is used to apply one or more aggregation functions to a DataFrame, Series, or GroupBy object.

## Flexible Usage of agg()
**Single Function**

Apply a single aggregation function to the entire DataFrame.

```
df.agg('mean')
````

**Multiple Functions (List)**

Apply multiple aggregation functions to a specific column.

```

df['A'].agg(['sum', 'mean', 'std'])

```
**Different Functions per Column (Dictionary)**

```
df.agg({
    'Col_A': ['min', 'max'],
    'Col_B': ['mean', 'sum']
})


```

## Creating a New Column

To create a new column in a DataFrame, use square brackets `[]` with the new column name.

```
df['new_column'] = df['existing_column'] * 2

```
## pandas.DataFrame.nlargest()

**Method Signature**

```
DataFrame.nlargest(n, columns, keep='first')

```
Description

Returns the top `n` rows ordered by specified column(s) in descending order.

- Only the specified columns are used for ordering

- All other columns are returned unchanged

**Example**
```
df.nlargest(5, 'sepal_length')

```

## Interquartile Range (IQR)

The Interquartile Range (IQR) measures the spread of the middle 50% of a dataset.

`IQR = Q3 - Q1`

Where:

- Q1 (First Quartile): Median of the lower half of the data

- Q3 (Third Quartile): Median of the upper half of the data

The IQR is commonly used for:

- Detecting outliers

- Understanding data variability

- Robust statistical analysis

## Purpose of This Repository

- Practice Pandas operations

- Learn data aggregation techniques

- Understand basic statistical concepts

- Maintain personal study notes for data analysis

