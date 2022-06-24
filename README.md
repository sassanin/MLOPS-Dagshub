[![Python application test with Github Actions](https://github.com/sassanin/MLOps/actions/workflows/main.yml/badge.svg)](https://github.com/sassanin/MLOps/actions/workflows/main.yml)

# MLOps DagsHub Demo
Step 1:
    Create Git repo
    create DagsHub repo: https://dagshub.com

Step 2:
    install DVC
    configure dvc:
        dvc remote add origin https://dagshub.com/sashicds/MLOPS-Dagshub.dvc
        dvc remote modify origin --local auth basic
        dvc remote modify origin --local user sashicds
        dvc remote modify origin --local password $DAGSHUB_TOKEN

        dvc pull -r origin

        dvc push -r origin

Step 2:
    install mlflow

    # add the following in the python code!
    mlflow.set_tracking_uri("https://dagshub.com/sashicds/MLOPS-Dagshub.mlflow")
    tracking_uri = mlflow.get_tracking_uri()
    print("Current tracking uri: {}".format(tracking_uri))

    export MLFLOW_TRACKING_USERNAME=sashicds
    export MLFLOW_TRACKING_PASSWORD=$DAGSHUB_TOKEN

