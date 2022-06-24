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
        dvc remote modify origin --local user DAGSHUB-USERNAME
        dvc remote modify origin --local password DAGSHUB-PASSWORD
