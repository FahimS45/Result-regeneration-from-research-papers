## Paper Reproduction:

**Title of the paper:** Evaluation and optimization of red pine needle-reinforced roller-compacted concrete by bioinspired algorithms

**Authors:** Sadik Alper Yildizel, Mehmet Uzun, Kemal Armagan, Togay Ozbakkaloglu

**Machine Learning algorithm used in this paper:**

* Artificial Neural Network (ANN) to predict Compressive Strength (CS) and Flexural Strength (FS).

**Optimization algorithms:**

* Genetic Algorithm (GA)
* Particle Swarm Optimization (PSO)
* Simulated Annealing (SA)

**Steps that were taken to rebuild the methodology and results:**

1.  Synthetic data generation: Since the paper does not include the dataset, a Gaussian distribution method was used to generate 100 mix designs.
2.  Multilinear Regression Models:  A multilinear regression model was also used to approximate real experimental data with the help of 5 data points from the CS and FS result sections in the paper.
3.  Trained an ANN model: Using synthetic data an ANN model was trained and saved.
4.  GA, PSO, and SA: 10 optimized mix designs were generated from each optimization algorithm.
5.  Prediction with ANN Model: The pre-trained ANN model predicted CS & FS for optimized mixes.
6.  Prediction with Multilinear Regression Models: The pre-trained regression model predicted CS & FS values for optimized mixes (considered as ground truth for performance comparison).
7.  Performance metrics:  RMSE, R², MAE, and MAPE were used to evaluate optimization algorithms by comparing ANN predictions and regression model outputs as reference values.

**Performance comparison of the applied algorithms:**

| Applied Algorithm | RMSE   | R²     | MAE    | MAPE   |
| ----------------- | ------ | ------ | ------ | ------ |
| ANN for CS        | 0.2281 | 0.9854 | 0.1830 | 0.61   |
| ANN for FS        | 0.2564 | 0.9866 | 0.2051 | 2.59   |
| GA for CS         | 0.7098 | 0.6345 | 0.3775 | 1.23   |
| GA for FS         | 0.2286 | 0.9581 | 0.1839 | 1.60   |
| POS for CS        | 0.1970 | 0.9484 | 0.1618 | 0.50   |
| PSO for FS        | 0.2266 | 0.9569 | 0.1662 | 1.62   |
| SA for CS         | 0,5620 | 0.7405 | 0.3738 | 1.17   |
| SA for FS         | 0.1770 | 0.9594 | 0.1527 | 1.31   |
