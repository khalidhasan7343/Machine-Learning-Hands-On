# Machine Learning Hands-On

A growing collection of hands-on notebooks covering Python foundations, data analysis, machine learning, and deep learning.

This repository documents my learning through practical exercises and projects, from exploring datasets and preparing features to training models, comparing results, and understanding prediction errors. More notebooks, datasets, and experiments will be added as I continue learning.

## Topics Covered

- **Python fundamentals:** variables, user input, loops, strings, collections, and object-oriented programming.
- **Data analysis:** data inspection, filtering, missing values, exploratory analysis, and visualization.
- **Supervised learning:** regression, classification, preprocessing, and model evaluation.
- **Unsupervised learning:** clustering and dimensionality reduction.
- **Deep learning:** dense neural networks, convolutional neural networks, transfer learning, and fine-tuning.

## Notebook Collection

### Python Foundations

| Notebook | What it covers |
| --- | --- |
| [Python Basics](Python_Basics.ipynb) | Printing, variables, user input, type conversion, and a simple calculator. |
| [Python Basics 2](Python_Basics_2.ipynb) | Loops, conditions, string manipulation, and counting vowels. |
| [Python Basics 3](Python_Basics_3.ipynb) | `enumerate`, `zip`, tuples, and set operations. |
| [Online Shopping Cart System](Online_Shopping_Cart_System.ipynb) | Classes, cart operations, discounts, and combining objects with operator overloading. |

### Data Analysis and Exploration

| Notebook | What it covers |
| --- | --- |
| [Heart Disease Data Analysis](Pandas_Data_Analysis_Using_Heart_Disease_Dataset.ipynb) | Exploring a dataset with pandas, checking missing values, analyzing categories, and selecting and filtering rows. |
| [Titanic Exploratory Data Analysis](Exploratory_Data_Analysis_%28EDA%29_on_the_Titanic_Dataset.ipynb) | Missing-value handling, univariate analysis, relationships between features, and visual insights. |

### Machine Learning

| Notebook | Dataset | Models and techniques |
| --- | --- | --- |
| [Housing Regression](Regression_Models_on_Housing_Dataset.ipynb) | Boston Housing | Linear Regression, Ridge, and Lasso; comparison using MAE, MSE, and R-squared. |
| [Diabetes Prediction](Diabetes_Prediction_Model.ipynb) | Pima Indians Diabetes | Logistic Regression, Random Forest, and SVM; preprocessing, classification metrics, ROC curves, and model saving. |
| [Customer Churn Prediction](Telco_Customer_Churn_Dataset_%28Kaggle%29.ipynb) | Telco Customer Churn | Logistic Regression, KNN, Decision Tree, and Random Forest; encoding, scaling, evaluation, and feature importance. |
| [Clustering and Dimensionality Reduction](Clustering_%26_Dimensionality_Reduction_%28Dataset__Iris_Dataset%29.ipynb) | Iris | K-Means, the elbow method, PCA, hierarchical clustering, and DBSCAN. |

### Deep Learning and Computer Vision

| Notebook | Dataset | Models and techniques |
| --- | --- | --- |
| [Handwritten Digit Classifier](MNIST_Handwritten_Digit_Classifier.ipynb) | MNIST | Dense neural network, normalization, Batch Normalization, Dropout, and training curves. |
| [Dense Network vs. CNN](Fashion_MNIST_Dense_vs_CNN_Assignment.ipynb) | Fashion-MNIST | Comparing dense and convolutional networks, parameter counts, confusion matrices, and misclassified images. |
| [Dog vs. Cat Classifier](Dog_Cat_Image_Classifier.ipynb) | Dog and cat images | A custom CNN, MobileNetV2 feature extraction, ResNet50 fine-tuning, data augmentation, and error analysis. |

## Getting Started

### Run Locally

Download this repository or clone it using its GitHub URL, then open a terminal in the project folder.

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it using the command for your operating system:

```powershell
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
```

```bash
# macOS / Linux
source .venv/bin/activate
```

Install the tools used by the data analysis and traditional machine learning notebooks:

```bash
python -m pip install jupyterlab numpy pandas matplotlib seaborn scikit-learn scipy joblib
```

For the deep learning notebooks, also install TensorFlow:

```bash
python -m pip install tensorflow
```

Launch JupyterLab:

```bash
python -m jupyterlab
```

Open a notebook, check its data-loading cells, and run the cells in order. The Python foundations notebooks use the standard library; they only need a Python notebook environment.

Dependencies are not version-pinned, and a shared environment has not been validated across all notebooks.

### Run in Google Colab

You can also open these `.ipynb` files in Google Colab. Upload any required CSV files and adjust their paths before running the notebook. The Titanic notebook includes a Google Drive mounting cell; use it when accessing files from Drive. A GPU runtime can help with the image-classification notebooks, especially ResNet50 fine-tuning.

## Dataset Setup

Dataset files are not bundled with this repository. Check each notebook's loading cells before running it.

| Notebook / dataset | How the data is loaded |
| --- | --- |
| Heart disease | Expects `/heart.csv`. Supply the CSV and update the path for your environment. |
| Titanic | Expects `/titanic.csv`. Supply the CSV and update the path for your environment. |
| Telco customer churn | Expects `Telco-Customer-Churn.csv` in the notebook's working directory. |
| Housing regression | Reads the housing data from a remote URL defined in the notebook. Internet access is required. |
| Diabetes prediction | Reads the Pima Indians Diabetes data from a remote URL defined in the notebook. Internet access is required. |
| Iris | Loads the dataset through `scikit-learn`. |
| MNIST / Fashion-MNIST | Uses Keras dataset loaders, which download the datasets on first use. |
| Dog vs. cat | Clones an external dataset repository and uses `/content/dog-cat-full-dataset/data`. Run from `/content` in Colab, or adjust the clone location, existence check, and `DATA_ROOT` for local use. Git and internet access are required for the download. |

Pretrained image models also download ImageNet weights on first use. External datasets remain subject to their original terms and attribution requirements.

## Suggested Learning Path

1. Start with the Python basics and shopping cart exercises.
2. Explore pandas and visualization through the heart disease and Titanic notebooks.
3. Practice regression and classification with housing, diabetes, and customer churn.
4. Explore clustering and PCA with Iris.
5. Move to MNIST, Fashion-MNIST, and dog-vs-cat image classification.

## Future Additions

- [ ] More regression and classification projects with new datasets.
- [ ] Cross-validation, hyperparameter tuning, and reusable preprocessing pipelines.
- [ ] Feature engineering and model interpretation experiments.
- [ ] Further work in natural language processing, time series, and computer vision.
- [ ] Project-specific dependency files and reproducible setup instructions.

When adding a project, include its objective, dataset source, setup requirements, approach, evaluation, and key observations, then add it to the notebook collection above.
