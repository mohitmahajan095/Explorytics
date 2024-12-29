# Explorytics

Explorytics is a Python library designed to simplify the process of exploratory data analysis (EDA). With an intuitive interface and powerful visualization tools, it provides quick insights into datasets, helping you understand distributions, correlations, and outliers with ease.

## Features

- **Comprehensive Data Analysis**: Perform statistical and visual analysis in a few lines of code.
- **Interactive Visualizations**: Generate dynamic plots for distributions, correlations, and relationships.
- **Outlier Detection**: Identify and explore outliers across various features.
- **User-Friendly API**: Designed for simplicity and ease of use, even for beginners.

## Installation

Install Explorytics using pip:

```bash
pip install explorytics
```

## Getting Started

Here's a quick example of how to use Explorytics with the Wine dataset from scikit-learn:

```python
# Import required libraries
import pandas as pd
from sklearn.datasets import load_wine
from explorytics import DataAnalyzer

# Load the wine dataset
wine = load_wine()
df = pd.DataFrame(wine.data, columns=wine.feature_names)
df['wine_class'] = wine.target

# Initialize the analyzer
analyzer = DataAnalyzer(df)

# Perform analysis
results = analyzer.analyze()

# Generate a distribution plot
analyzer.visualizer.plot_distribution('alcohol', kde=True).show()

# Generate a correlation heatmap
analyzer.visualizer.plot_correlation_matrix().show()
```

## Documentation

The complete documentation is available [here](./DOCUMENTATION.md). It includes details on:

- Installation and setup
- Usage examples
- API references for key classes and methods
- Advanced configuration options

See it in action on [Google-Colab](https://colab.research.google.com/drive/1JH2ewdZeakqBptWbcuCf91L0sw9ZFB6Y?usp=sharing) <
## Examples

Explore the `examples` folder for Jupyter notebooks showcasing various use cases, including:

- Basic data exploration
- Advanced feature relationships
- Outlier detection and analysis

## Contributing

We welcome contributions! If you'd like to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Make your changes and commit: `git commit -m 'Add feature name'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

Please ensure your code adheres to the existing style and includes tests for any new functionality.
## Issue Resolution: Versions 0.1.0, 0.1.1, and 0.1.2

### ⚠️Warning: **Do not use versions 0.1.0, 0.1.1, or 0.1.2 (if using any **upgrade** to version 0.1.4)**
If you're using version 0.1.0, 0.1.1, or 0.1.2, **please upgrade** to **version 0.1.4** or later. These earlier versions had critical issues that resulted in incomplete installations and missing files. The package structure was not correctly bundled, leading to missing dependencies and modules that prevented users from fully utilizing the library.

### Problem Overview
In versions  0.1.0, 0.1.1, and 0.1.2, we faced multiple issues with the packaging process, resulting in missing files such as visualizations and helper modules, and incorrect package structure. Following were the issues and their resolutions:

#### Issues:

1. **Missing Visualizations and Helper Files (Version 0.1.0)**:
   The `visualizations` and `helpers` modules were not included in the package, causing errors like:
   ```python
   ModuleNotFoundError: No module named 'explorytics.visualizations'
2. **Incorrect Package Structure (Version 0.1.1)**:
   Despite efforts to fix the structure, important directories such as core, visualizations, and utils were still missing in the final distribution.

4. **Dependency Issues (Version 0.1.2)**:
   There were problems with dependencies not being correctly listed in setup.py, causing compatibility issues with different Python environments.

To resolve these issues, we took the following steps:
1. Updated MANIFEST.in to Include All Files
2. Manually Verified the Distribution
3. Fixed Dependencies in setup.py
4. Re-released as Version 0.1.3
 
## License

Explorytics is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## Acknowledgments

This library was inspired by a course I was pursuing on Coursera: [Exploratory Data Analysis for Machine Learning](https://www.coursera.org/learn/ibm-exploratory-data-analysis-for-machine-learning/). Special thanks to the open-source community for providing inspiration and support.

---

Start exploring your data today with Explorytics!
