# STATS615-Final-Project
This is the final project of Stats 615 in Rice Univerisity
# Project Title: Regression Analysis and Model Diagnostics

## Overview
This project uses **Multiple Linear Regression (MLR)** and **Lasso Regression** to perform statistical analysis and model diagnostics. The analysis is implemented in the R Markdown file `final2.0.Rmd`. The goal of the project is to:
- Identify significant predictors in the dataset.
- Compare the performance of MLR and Lasso Regression.
- Provide model diagnostics and visualizations for interpretability.

---

## File Information
- **Primary File**: `final2.0.Rmd`
- **Purpose**: Perform statistical modeling, visualize results, and generate model summaries.
- **Output**: The R Markdown file can produce:
   - **HTML reports** (default)
   - **PDF reports** (requires LaTeX installation)
   - **Word documents**

---

## Requirements
To replicate the project, you need the following:

### Software
- **R** (version 4.0.0 or higher)
- **RStudio** (recommended for running R Markdown)

### R Libraries
The required libraries can be installed using the following command in R:

```r
install.packages(c("rmarkdown", "ggplot2", "glmnet", "caret", "dplyr"))
Follow these steps to run the project:

Clone this repository to your local machine:

bash

git clone https://github.com/yourusername/yourproject.git
cd yourproject
Open the final2.0.Rmd file in RStudio or any compatible editor.

Install the required libraries listed above.

Render the R Markdown file to generate the report:

In RStudio, click the Knit button.
Or run the following command in R:
r
rmarkdown::render("final2.0.Rmd")


The output report (HTML, PDF, or Word) will be saved in the project directory.

Features
The project includes the following features:

Data Preprocessing: Clean and prepare the dataset for analysis.
Multiple Linear Regression (MLR):
Build and evaluate the MLR model.
Check model assumptions using diagnostic plots.
Lasso Regression:
Perform cross-validation to select the optimal regularization parameter (𝜆).
Visualize coefficient paths for variable selection.
Visualizations:
Residual plots, Lasso coefficient paths, and comparison of model performance.
Example Code
Here’s an example of the analysis process:


# Load necessary libraries
library(ggplot2)
library(glmnet)

# Example: Fitting Lasso Regression
x <- model.matrix(mpg ~ ., mtcars)[, -1]
y <- mtcars$mpg

# Perform Lasso regression with cross-validation
cv_lasso <- cv.glmnet(x, y, alpha = 1)
plot(cv_lasso)

# Optimal lambda
best_lambda <- cv_lasso$lambda.min
Outputs
The analysis produces the following:

Model Summaries: Comparison of MLR and Lasso Regression results.
Visual Diagnostics:
Residual vs. Fitted plots for MLR.
Coefficient paths for Lasso Regression.
Performance Metrics:
Adjusted 
𝑅^2
 
Residual Standard Error
Cross-validated error for Lasso Regression.
Contributing
Contributions are welcome! If you find any issues or have suggestions, please open an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any questions or feedback, feel free to reach out:

Author: Zenan Ji
Email: zenanji1024@gmail.com
GitHub: https://github.com/ZenanJi1024


