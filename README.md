Hi, this repo contains a simple script that finds the peaks in a one-dimensional data sequence.

# Algorithm

The algorithm involves two major steps. 

1. We first smooth the entire data by taking an average of sliding windows. Specifically, we use a sliding window across the entire time series and take an average over a given window size. 
(this step is optional as we can simply find the peaks in the raw data, feel free to try both to see which one fits your needs better)

2. Then, we use a sliding window that compares the center data point to all data points in the left and right halves of the window. We consider a point to be a peak if it is at least `min_diff` greater than the minimum value on the left and minimum value on the right.

You can also play around with the parameters `min_diff` and `window_width` in this step.

# Getting started

First, you need to have [python](https://www.python.org/downloads/) (at least version 3.8) downloaded.

It is also recommended to have an environment/package manager such as [conda](https://conda.io/projects/conda/en/stable/user-guide/install/index.html#regular-installation) installed.

Create a new environment
```
conda create --name peaks python=3.8
conda activate peaks
```

Install packages
```
pip install -r requirements.txt
```

Now you can get started by opening and running the notebook
```
jupyter notebook
```

# Citation

You should see a button on the right side of the repo page labeled "Cite this repository".
