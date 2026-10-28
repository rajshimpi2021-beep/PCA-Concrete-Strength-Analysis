# Dimensionality Reduction of Engineering Dataset using PCA

**Student project:** Principal Component Analysis (PCA) on the Concrete Compressive Strength dataset.

## Aim
Study how PCA reduces the dimensionality of engineering data and evaluate the effect of retaining different numbers of principal components on a regression task.

## Dataset
- **Dataset:** Concrete Compressive Strength
- **Rows:** 1,030
- **Columns:** 8 input features and 1 target (concrete compressive strength)
- **Missing values:** 0 in the version used for this project
- **Source:** UCI Machine Learning Repository — https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength

The dataset file is not included in this repository. Download it from the source above and use the `Concrete_Data.xls` file when running the Colab notebook.

## Method
1. Load and inspect the dataset.
2. Separate the eight input features from the compressive-strength target.
3. Standardize the input features.
4. Fit PCA and calculate explained and cumulative explained variance.
5. Visualize the scree curve, PCA projection, loadings, biplot, and feature correlations.
6. Compare a regression baseline using all eight original features with models using selected numbers of principal components.

## Reported results
These are the results recorded in the project report; re-run the notebook to reproduce them in your environment.

| Features/components | Explained variance retained | Test R² | Test RMSE |
|---|---:|---:|---:|
| Original 8 features | — | 0.628 | 9.797 |
| PCA, 2 components | 45.926% | -0.001 | 16.062 |
| PCA, 3 components | 62.757% | 0.265 | 13.765 |
| PCA, 4 components | 75.560% | 0.260 | 13.806 |
| PCA, 5 components | 87.372% | 0.479 | 11.582 |
| PCA, 6 components | 97.310% | 0.568 | 10.552 |
| PCA, 7 components | 99.612% | 0.617 | 9.941 |

**Interpretation:** Six components retain about 97% of the feature variance while reducing the feature count from eight to six. In this experiment, the full eight-feature baseline performs better than PCA with six components, so dimensionality reduction involves a trade-off between compression and predictive performance.

## Run in Google Colab
1. Open `PCA_Mini_Project_Colab.ipynb` in Google Colab.
2. Run the cells in order.
3. Upload `Concrete_Data.xls` when prompted.
4. Review the printed metrics and generated plots.

## Files
- `PCA_Mini_Project_Colab.ipynb` — notebook workflow.
- `README.md` — project summary, data source, and reported results.
- `requirements.txt` — Python dependencies.

## Reproducibility note
Model metrics can vary slightly with library versions and train/test split details. The values above reflect the results recorded in the report; use the actual notebook output as the primary evidence for your run.
