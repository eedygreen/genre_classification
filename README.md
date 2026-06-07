Running the pipeline with MLflow

Running from local environment 

These command requires cloning this repository
```
mlflow run . -P hydra_options="main.execute_steps='random_forest'"
```
To select two or more pipeline steps, you can use a comma-separated list of steps. For example, to run the download and preprocess steps, you can use the following command:
```
mlflow run . -P hydra_options="main.execute_steps='download,preprocess'"
```

Inference 
```
mlflow run . -P hydra_options="main.project_name=classification_prod"
```

Running from remote environment

```
mlflow run -v {release_tag} repository_url -P hydra_options="main.project_name=classification_prod"
```

`mlflow run -v 1.0.0 https://github.com/eedygreen/genre_classification.git -P hydra_options="main.project_name=released_prod_version"`
