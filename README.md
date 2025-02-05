# Topsis-Minal102203788
 # TOPSIS Package

## Overview
The **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** package is designed to help you rank and evaluate multiple alternatives based on a set of criteria. It simplifies the decision-making process by identifying the option closest to the ideal solution and farthest from the negative ideal solution.

## Features
- Easy-to-use implementation of the TOPSIS algorithm.
- Supports data preprocessing and normalization.
- Handles multiple criteria with different weights.
- Outputs rankings and performance scores for each alternative.

## Installation
Install the package using pip:

```bash
pip install topsispackage
```

## Usage
### Input Format
The input to the TOPSIS package should be a CSV file with the following structure:

| Alternative | Criterion 1 | Criterion 2 | ... | Criterion N |
|-------------|-------------|-------------|-----|-------------|
| A1          | 10          | 20          | ... | 30          |
| A2          | 15          | 25          | ... | 35          |

- The first column should contain the names or labels of the alternatives.
- The subsequent columns should contain numerical values representing the criteria for each alternative.

### Code Example
```python
from topsispackage import topsis

# Provide the file path, weights, and impacts
data_file = "data.csv"
weights = [0.3, 0.4, 0.3]  # Sum of weights should be 1
impacts = ['+', '+', '-']  # '+' for benefit, '-' for cost

# Perform TOPSIS analysis
topsis(data_file, weights, impacts, "output.csv")
```

### Output
The output will be saved as a CSV file (e.g., `output.csv`) containing the rankings and performance scores:

| Alternative | Score  | Rank |
|-------------|--------|------|
| A1          | 0.75   | 1    |
| A2          | 0.65   | 2    |

## Parameters
- **data_file**: Path to the input CSV file.
- **weights**: List of weights for each criterion. The weights should sum up to 1.
- **impacts**: List of impacts for each criterion ('+' for benefit and '-' for cost).
- **output_file**: Path to save the output CSV file.

## Example Dataset
An example dataset (`data.csv`) might look like this:

```csv
Alternative,Price,Quality,Durability
A1,25000,4,7
A2,20000,3,9
A3,30000,5,6
```

## How it Works
1. **Normalization**: The dataset is normalized to make all criteria comparable.
2. **Weighting**: Each criterion is weighted according to its importance.
3. **Ideal Solutions**: The ideal (best) and negative ideal (worst) solutions are calculated.
4. **Ranking**: Alternatives are ranked based on their similarity to the ideal solution.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for enhancements or bug fixes.

## Contact
For questions or support, please contact:
**Minal Jain**  
[GitHub](https://github.com/minal2577)  
[LinkedIn](https://linkedin.com/in/minal-631400259)
