# Regularization and Feature Selection

Two questions decide how well a model generalises: **how much complexity to allow it**, and **which features to give it in the first place**. This repository answers both. You will:

- see, through the bias-variance trade-off, how a model goes wrong with too little or too much complexity
- control complexity with Ridge, Lasso and ElasticNet regularization
- choose features with filter, wrapper and embedded methods, and work out what to do when a feature is a category rather than a number
- decide how to handle outliers

Linear regression is the example model throughout, but the ideas apply to any supervised learning task.

## Learning Objectives

By the end of this repository, you should be able to:

- Split data into training and test sets, and calculate the root mean squared error (RMSE) on each.
- Compare the training and test RMSE of polynomial models to identify underfitting (high bias) and overfitting (high variance).
- Standardize the features and train Ridge, Lasso and ElasticNet models, choosing `alpha` on a validation set.
- Rank and select features with correlation, mutual information, `SelectKBest`, variance inflation factor, p-values, recursive feature elimination, sequential selection and Lasso, and classify each method as filter, wrapper or embedded by whether and how it uses the target.
- Choose the right association measure when a feature is categorical rather than numeric.
- Detect outliers visually and with z-scores, and compare models trained with and without them.

## Learning Path

Work through the notebooks in this order:

| File / Folder | Description |
|---|---|
| [**01 - Bias-Variance Trade-Off**](01_bias_variance_tradeoff.ipynb) | Train/test splits, polynomial features, and the bias-variance trade-off. Includes an exercise. |
| [**02 - Regularization**](02_regularization.ipynb) | Scaling, Ridge, Lasso and ElasticNet, with `alpha` chosen on a validation set. |
| [**03 - Feature Selection**](03_feature_selection.ipynb) | Filter, wrapper and embedded methods, and what to do when a feature is categorical. Includes an exercise. |
| [**04 - Detecting Outliers**](04_detecting_outliers.ipynb) | Spotting outliers and measuring how removing them affects model performance. Includes an exercise. |

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Data**](data/) | The white wine quality dataset, the California housing dataset used for feature selection, and the `tips` data carried over from week 2. |
| [**Assets**](assets/) | Images used in the notebooks. The Mermaid sources of the diagrams are in `assets/diagrams/`. |
| [**Solutions**](solutions/) | Reference solutions for the exercises. |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies. |
| [**uv.lock**](uv.lock) | Dependency lock file. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it, including the `< >` brackets, with your own value. For example, `cd <repo-name>` becomes `cd amle-regularization-feature-selection`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

## References & Further Reading

- [**Train Test Split (scikit-learn)**](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html): How to split data into train and test sets.
- [**Underfitting vs. Overfitting (scikit-learn)**](https://scikit-learn.org/stable/auto_examples/model_selection/plot_underfitting_overfitting.html): A worked polynomial example of the bias-variance trade-off.
- [**Linear Models: Ridge, Lasso, and ElasticNet (scikit-learn)**](https://scikit-learn.org/stable/modules/linear_model.html): The reference for the regularised regression models used in notebook 02.
- [**Outliers: To Drop or Not to Drop**](https://www.theanalysisfactor.com/outliers-to-drop-or-not-to-drop/): Practical guidance on when removing outliers is justified.
