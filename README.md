P1 A EXPLANATION
Here’s the notebook explained step-by-step, super concise:

1. Objective
   Design, train, and test a simple **Linear Regression** model on synthetic data.

2. Create synthetic dataset

* Import `randint`; set `TRAIN_SET_LIMIT = 1000`, `TRAIN_SET_COUNT = 100`.
* For 100 rows, sample integers `a, b, c ∈ [0, 1000]`.
* Compute target with a known linear rule: **y = a + 2b + 3c**.
* Build `TRAIN_INPUT = [[a,b,c], …]` and `TRAIN_OUTPUT = [y, …]`.

3. Train the model

* `from sklearn.linear_model import LinearRegression`
* `predictor = LinearRegression(n_jobs=-1)`
* `predictor.fit(TRAIN_INPUT, TRAIN_OUTPUT)` to learn the mapping.

4. Test the model (manual check)

* Define `X_TEST = [[10, 20, 30]]` → expected **y = 10 + 2×20 + 3×30 = 140**.
* `outcome = predictor.predict(X_TEST)` → **\[140.]**.
* `coefficients = predictor.coef_` → **\[1., 2., 3.]** (exact recovery of the true weights).


* Perfect, noiseless linear data → Linear Regression recovers exact coefficients and predictions.
* Demonstrates the ML workflow: **generate data → fit model → predict → verify**.
