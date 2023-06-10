<h1> Prediction of Real Estate Prices in St. Petersburg </h1>

[Dataset](https://github.com/stepanvarygin/final_project/blob/main/rent_data_cleaned.csv)

<h3> Data preprocessing: </h3>

1. Outliers cleaning with IQR.
2. Feature engineering: price per square.
3. Using of scaling: `StandardScaler()`.

<h3> Features - target correlations: </h3>

![alt text](https://github.com/stepanvarygin/final_project/blob/main/Viz.png)

<h3> ML model </h3>

Parameteters of the model were tuned using `Pipeline()` classifier with `ParameterGrid()` loop.

**Optimal model was:** `RandomForestRegressor()`

**Checked parameters were:**
```
params_grid = dict(n_estimators = [50, 100, 150, 200, 300, 400], max_depth = [5, 6, 7, 8, 9])
```

**Optimal parameters were:**
```
{'max_depth': 9, 'n_estimators': 150}
```

<h3> Project </h3>

* The project was created using local path and Yandex remote machine with connection to the GitHub remote repository.

* The [Docker image](https://hub.docker.com/repository/docker/stepanvarygin/final_project/general) was created.

* The running was tested on the Postman app.