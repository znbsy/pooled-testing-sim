## Pooled testing simulation

Your goal is to implement a pooled testing strategy which minimizes the average number of tests for some specific prevalence _p_ and sample size _n_. Relevant slides can be found [here](https://docs.google.com/presentation/d/1ef4VCuorFMAF8eCewnktcQ7swXsg7pUmOdWHe1swtkQ/edit?usp=sharing).

### Instructions

1. Someone from the group should fork this repository.
2. Copy the `StudentProtocols/Baseline.py` file to `StudentProtocols/<YOUR_GROUP_NAME>.py`.
3. Implement the `isolate_positives` function in your protocol file. Essentially, the `isolate_positives` function is provided a `TestSample` object. Using the `query` method of the sample, you can query any set of numbers `0, 1, ..., n-1`, and the `query` method will return true of any of the queried numbers are "positive". In other words, you provide `query` a _pooled_ sample. Your task is to correctly return the IDs of the positive samples in the provided `TestSample` using as few tests as possible (on average). 
4. Run the simulation in the `CovidTester.ipynb` notebook. You should get a table that looks like this

```
+--------------+-------+----------+
|  Group Name  |  Mean | Variance |
+--------------+-------+----------+
| ProjectOwler | 7.129 |  30.643  |
|   Baseline   |  32.0 |   0.0    |
+--------------+-------+----------+
```

5. Once you are satisfied, create a pull request back to this repo. *Only add+commit your new file!*
```
git add `StudentProtocols/<YOUR_GROUP_NAME>.py`
git commit `StudentProtocols/<YOUR_GROUP_NAME>.py` -m "Updates"
```