# Matplotlib Cheat Sheet

This repository is a beginner-friendly Matplotlib cheat sheet. It focuses on the most common plotting tasks in Python, including line plots, scatter plots, bar charts, histograms, subplots, labels, legends, and saving figures.

Matplotlib is commonly used through the `pyplot` module, usually imported as `plt`.

## Repository

GitHub repository:

```text
https://github.com/arq7arq/Matplotlib
```

Clone the repository:

```bash
git clone https://github.com/arq7arq/Matplotlib.git
cd Matplotlib
```

## Requirements

Install Matplotlib, NumPy, Pandas, and Jupyter:

```bash
pip install matplotlib numpy pandas notebook
```

Start Jupyter:

```bash
jupyter notebook
```

Then open the notebook or Python file from the repository and run the examples.

## Import Libraries

```python
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
```

| Library | Purpose |
| --- | --- |
| `matplotlib.pyplot` | Creates and customizes plots |
| `numpy` | Creates numeric arrays and sample data |
| `pandas` | Loads and works with table-style data |

## Basic Line Plot

```python
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.show()
```

`plt.plot()` is used for line plots.

## Add Title and Axis Labels

```python
plt.plot(x, y)

plt.title("Simple Line Plot")
plt.xlabel("X values")
plt.ylabel("Y values")

plt.show()
```

| Function | Meaning |
| --- | --- |
| `plt.title()` | Adds a title to the plot |
| `plt.xlabel()` | Adds a label to the x-axis |
| `plt.ylabel()` | Adds a label to the y-axis |
| `plt.show()` | Displays the plot |

## Customize Line Style

```python
plt.plot(
    x,
    y,
    color="red",
    linestyle="--",
    marker="o",
    linewidth=2
)

plt.show()
```

Common customization options:

| Option | Example | Meaning |
| --- | --- | --- |
| `color` | `"red"` | Line color |
| `linestyle` | `"--"` | Dashed line |
| `marker` | `"o"` | Marker at each point |
| `linewidth` | `2` | Thickness of the line |

## Multiple Lines

```python
x = np.array([1, 2, 3, 4, 5])

y1 = x * 2
y2 = x ** 2

plt.plot(x, y1, label="x * 2")
plt.plot(x, y2, label="x squared")

plt.title("Multiple Lines")
plt.xlabel("x")
plt.ylabel("y")
plt.legend()

plt.show()
```

Use `label` with `plt.legend()` to explain each line.

## Scatter Plot

```python
x = [5, 7, 8, 7, 2, 17, 2, 9]
y = [99, 86, 87, 88, 100, 86, 103, 87]

plt.scatter(x, y)

plt.title("Scatter Plot")
plt.xlabel("x")
plt.ylabel("y")

plt.show()
```

`plt.scatter()` is useful for showing relationships between two numeric variables.

## Bar Chart

```python
names = ["A", "B", "C", "D"]
values = [10, 25, 15, 30]

plt.bar(names, values)

plt.title("Bar Chart")
plt.xlabel("Category")
plt.ylabel("Value")

plt.show()
```

`plt.bar()` is useful for comparing categories.

## Histogram

```python
data = np.random.randn(1000)

plt.hist(data, bins=30)

plt.title("Histogram")
plt.xlabel("Value")
plt.ylabel("Frequency")

plt.show()
```

`plt.hist()` is useful for showing the distribution of numeric data.

## Pie Chart

```python
labels = ["Python", "JavaScript", "C++", "Java"]
sizes = [45, 25, 15, 15]

plt.pie(sizes, labels=labels, autopct="%1.1f%%")
plt.title("Pie Chart")

plt.show()
```

Pie charts are useful for showing parts of a whole.

## Subplots

Use subplots when you want multiple charts in one figure:

```python
x = np.array([1, 2, 3, 4, 5])

fig, axes = plt.subplots(1, 2, figsize=(10, 4))

axes[0].plot(x, x * 2)
axes[0].set_title("Line Plot")

axes[1].bar(["A", "B", "C"], [5, 7, 3])
axes[1].set_title("Bar Chart")

plt.tight_layout()
plt.show()
```

| Code | Meaning |
| --- | --- |
| `plt.subplots(1, 2)` | Creates 1 row and 2 columns of plots |
| `figsize=(10, 4)` | Sets the figure size |
| `axes[0]` | First plot |
| `axes[1]` | Second plot |
| `plt.tight_layout()` | Reduces overlap between plots |

## Figure Size

```python
plt.figure(figsize=(8, 5))
plt.plot(x, y)
plt.show()
```

`figsize=(width, height)` controls the size of the figure in inches.

## Grid Lines

```python
plt.plot(x, y)
plt.grid(True)
plt.show()
```

Grid lines can make plots easier to read.

## Save a Figure

```python
plt.plot(x, y)
plt.title("Saved Plot")

plt.savefig("plot.png", dpi=300, bbox_inches="tight")
plt.show()
```

| Option | Meaning |
| --- | --- |
| `plot.png` | Output file name |
| `dpi=300` | Image quality/resolution |
| `bbox_inches="tight"` | Removes extra whitespace |

## Quick Reference

| Task | Code |
| --- | --- |
| Line plot | `plt.plot(x, y)` |
| Scatter plot | `plt.scatter(x, y)` |
| Bar chart | `plt.bar(categories, values)` |
| Histogram | `plt.hist(data, bins=30)` |
| Pie chart | `plt.pie(values, labels=labels)` |
| Add title | `plt.title("Title")` |
| Add x-axis label | `plt.xlabel("X label")` |
| Add y-axis label | `plt.ylabel("Y label")` |
| Add legend | `plt.legend()` |
| Add grid | `plt.grid(True)` |
| Create subplots | `fig, axes = plt.subplots()` |
| Save figure | `plt.savefig("plot.png")` |
| Show figure | `plt.show()` |

## Main Concepts Practiced

- Importing Matplotlib
- Creating line plots
- Adding titles and axis labels
- Customizing colors, markers, and line styles
- Plotting multiple lines
- Creating scatter plots
- Creating bar charts
- Creating histograms
- Creating pie charts
- Using legends
- Using grid lines
- Creating subplots
- Changing figure size
- Saving plots as image files

## Notes

- Always call `plt.show()` when you want to display a plot in a normal Python script.
- In Jupyter Notebook, plots often display automatically, but `plt.show()` is still a good habit.
- Use `plt.figure(figsize=(width, height))` before plotting to control the chart size.
- Use `label="..."` and `plt.legend()` when plotting multiple datasets.
- Use `plt.tight_layout()` when subplots overlap.
