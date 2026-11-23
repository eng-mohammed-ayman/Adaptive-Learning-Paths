# Adaptive Learning Path Classification

An interpretable decision-tree coursework project that assigns student performance categories from the UCI Student Performance mathematics dataset.

## Team and scope

Coursework team, as credited in the supplied report: Mohamed Ayman, Hamed Ahmed and Mostafa El-Demiry. Mohamed wrote the report and presentation and studied the code to understand it. Implementation belongs to the team project; this repository makes no claim that Mohamed independently wrote the model or notebook. This is a GitHub coursework entry, not an addition to his CV.

The labels are constructed from final grade `G3`: below 10 is `remedial`, 10 to below 15 is `standard`, and 15 or above is `advanced`. `G3` is then removed from the predictors. These are project-defined grade bands, not validated teaching recommendations or demonstrated improvements in student learning.

## Reproduce locally

See `dataset/README.md` for the original UCI source and required local filename.

```bash
python -m venv .venv
# Activate .venv.
pip install -r requirements.txt
jupyter lab adaptive_learning_paths.ipynb
```

Run the notebook from this repository directory. It inspects the data, plots distributions, one-hot encodes categorical features, makes a stratified 80/20 split with random seed 42, and fits a depth-4 decision tree.

## Interpretation and limits

`G1` and `G2`, earlier-period grades, remain predictors. Results therefore describe prediction after those grades exist, not an early intervention before any grades are known. UCI explicitly notes the strong relationship between these grades and `G3`. The small dataset and one holdout split do not establish generalization across schools, fairness, or educational benefit. The notebook performs one-hot encoding before the split; production work should move preprocessing into a train-fitted pipeline.

Original notebook outputs and execution metadata are removed. Dataset, reports and slides are not included. Verification results and any rerun measurements are recorded separately in `VERIFICATION.md`. No software license is granted on behalf of the other team members.
