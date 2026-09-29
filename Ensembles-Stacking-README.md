# Heart Failure Prediction with Stacking Ensembles

A machine learning project that predicts heart failure outcomes using **stacking**, an ensemble method that combines the predictions of several different models into one stronger model.

> **Disclaimer:** This project is for learning and research only. It is not a medical device and must not be used to diagnose, treat, or make decisions about any patient.

---

## What is stacking?

Instead of trusting a single model, stacking trains several **base models** and then trains a **meta-model** that learns how best to combine their predictions.

```
                 ┌──────────────┐
                 │ Base model 1 │──┐
                 └──────────────┘  │
   Patient data  ┌──────────────┐  │   ┌────────────┐    ┌────────────┐
  ─────────────► │ Base model 2 │──┼──►│ Meta-model │───►│ Prediction │
                 └──────────────┘  │   └────────────┘    └────────────┘
                 ┌──────────────┐  │
                 │ Base model N │──┘
                 └──────────────┘
```

Because the base models make different kinds of mistakes, the combined model can often perform better than any of them alone.

## Repository contents

| File | Description |
| --- | --- |
| `Ensembles_Stacking_Heart_Failure_Prediction_(1).ipynb` | The main notebook: data loading, preparation, model training, stacking, and evaluation. |
| `index.html` | Placeholder page (currently empty). |
| `README.md` | This file. |

## Getting started

### Prerequisites

- Python 3.9 or newer
- [Jupyter Notebook or JupyterLab](https://jupyter.org/install), or upload the notebook to [Google Colab](https://colab.research.google.com/) to run it in your browser with no setup

### Installation

```bash
git clone https://github.com/TimBroAhm/Ensembles-Stacking-.git
cd Ensembles-Stacking-

python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

> The notebook's first cells show the exact libraries it imports. Install any that are missing.

### Run the notebook

Make sure your terminal is inside the `Ensembles-Stacking-` folder (run `ls` on Mac/Linux or `dir` on Windows to check that the `.ipynb` file is listed), then start Jupyter:

```bash
jupyter notebook
```

Your browser will open a file list. Click the notebook (`Ensembles_Stacking_Heart_Failure_Prediction_(1).ipynb`) and run the cells from top to bottom.

If you don't want to type the filename, this also works:

```bash
jupyter notebook *.ipynb
```

## Results

Add your final numbers here so visitors can see how well the model works, for example:

| Model | Accuracy | F1 | ROC-AUC |
| --- | --- | --- | --- |
| Base model 1 | | | |
| Base model 2 | | | |
| **Stacked ensemble** | | | |

## Ideas for future work

- Tune the hyperparameters of the base models and the meta-model
- Compare stacking with bagging and boosting
- Add feature importance or SHAP plots to explain predictions
- Turn the notebook into a small web app (the empty `index.html` could be the start)

## Contributing

Suggestions and improvements are welcome:

1. Fork the repository
2. Create a branch (`git checkout -b feature/your-idea`)
3. Commit your changes
4. Open a pull request

## Author

**TimBroAhm** - [GitHub profile](https://github.com/TimBroAhm)
