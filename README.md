# Programming Languages Popularity Analysis

This project analyzes the popularity of various programming languages over time using data from StackOverflow. The data was sourced using an SQL query and visualized with the help of Python libraries such as Pandas and Matplotlib.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Getting Started](#getting-started)
- [Data Exploration](#data-exploration)
- [Data Cleaning](#data-cleaning)
- [Data Manipulation](#data-manipulation)
- [Data Visualization](#data-visualization)
- [Smoothing Time Series Data](#smoothing-time-series-data)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The purpose of this project is to analyze and visualize the popularity of different programming languages over time based on the number of posts tagged with each language on StackOverflow. By examining the trends in programming language usage, we can gain insights into the evolution of technology and developer preferences.

## Data Source

The data is retrieved from StackExchange using the following [SQL query](https://data.stackexchange.com/stackoverflow/query/675441/popular-programming-languages-per-over-time-eversql-com). The query selects data related to the number of posts tagged with specific programming languages and aggregates it monthly.

## Getting Started

To get started with the project, you will need to clone the repository and install the required dependencies.

### Prerequisites

- Python 3.x
- Pandas
- Matplotlib

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Prathamesh326/Data-Visualisation-with-Matplotlib.git
    cd Data-Visualisation-with-Matplotlib
    ```

2. Install the required Python packages:
    ```bash
    pip install pandas matplotlib
    ```

3. Obtain the data:
    - You can either use the provided `QueryResults.csv` file or generate your own CSV file by running the [SQL query](https://data.stackexchange.com/stackoverflow/query/675441/popular-programming-languages-per-over-time-eversql-com) on StackExchange.

4. Run the Jupyter notebook or Python script to perform the analysis.

## Data Exploration

The data is read into a Pandas DataFrame from the `QueryResults.csv` file. Here are some initial exploration steps performed:

- Display the first and last few rows of the data using `df.head()` and `df.tail()`.
- Check the dimensions of the DataFrame using `df.shape`.
- Count the number of entries in each column using `df.count()`.
- Calculate the total number of posts per language using `df.groupby('TAG').sum(numeric_only=True)`.

## Data Cleaning

The date format is cleaned to make it more readable, converting it from a string to a datetime object.

## Data Manipulation

The data is reshaped using the `pivot` function to create a new DataFrame with programming languages as columns and dates as rows.

## Data Visualization

### Single Language Plot

A single programming language, such as Java, is plotted on a chart to visualize its popularity over time.

### Comparison of Two Languages

A comparison between two languages, such as Java and Python, is plotted on the same chart.

### All Languages Plot

All programming languages in the dataset are plotted on the same chart to compare their popularity trends over time.

## Smoothing Time Series Data

To smooth out the time series data and better visualize trends, a rolling mean is calculated using different window sizes (e.g., 3, 6, 12 months) and plotted.

## Contributing

If you would like to contribute to this project, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
