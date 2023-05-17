# Programming Exercises for Python

## Data wrangling

1. Create a `DataFrame` named `df` with 6 nrows with the following columns:

    - `A`: random floating point value
    - `B`: randomly assigned categorical values from `["test", "train"]`
    - `C`: random integer values, constructed from an `numpy.array`
    - `D`: random integer values, constructed from a `Series`
    - `E`: monthly dates "2021-01-01", "2021-02-01", "2021-03-01" ...

2. Convert numeric columns into a `numpy.matrix` and compute the row sums.

3. Sort `df` by column `C`.

4. Filter `df` for entries for which `B` has value `train` and `C`
   has values greater than 0.

5. Change the value in the 4th column and 2nd row to 10.

6. Create a column `F` where half the values are `NaN`.

7. Deal with missing values in two different ways:
    
    - remove entries with missing data
    - fill missing values with 0

8. Convert column `A` into a cumulative sum.

9. Subtract column `A` from column `B`.

10. Plot the numeric columns as a line plot, ensuring that the plot
   has proper labels.

11. Compute the mean values of each column for groups `train` and `test`.

12. Convert the following `DataFrame` from `a` into `b` (long to wide).
    Additionally, convert from `b` into `a` (wide to long).

```
a = pd.DataFrame(
    {"value": [1, 2, 3, 4, 5, 6], "group": ["a", "a", "a", "b", "b", "b"]}
)

b = pd.DataFrame(
    {"a": [1, 2, 3], "b": [4, 5, 6]}
)
```


## Supervised learning

1. Load the `iris` dataset by
```
import sklearn as sk
import sklearn.datasets
iris = sk.datasets.load_iris()
```

2. Visualize the data matrix.

3. Train a random forest classifier to predict the target values and 
   report its performance using an appropriate evaluation metric.

4. Explain how key parameters of the random forest classifier would influence
   its peformance.


## Text mining

1. Using `Biopython`, collect medline abstracts on "medulloblastoma"
   published in 2012. Save the data to disk as a CSV table.

2. Import the CSV table and build a SQLite database.

3. Obtain the PMID and title of publications for authors with the surname
   "Shih" from the database.


## Neural network

1. Implement a full connected feedforward network from scratch using 
only the `numpy` library with the following layers:
one input, two hidden, and one output.
Neurons should use the sigmoid transfer function.
The network should be trained using
[backpropagation of errors](https://dustinstansbury.github.io/theclevermachine/derivation-backpropagation).
