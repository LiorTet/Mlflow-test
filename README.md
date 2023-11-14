# Starting with mlflow
MLFLOW_TRACKING_URI=https://dagshub.com/LiorTet/Mlflow-test.mlflow \
MLFLOW_TRACKING_USERNAME=LiorTet \
MLFLOW_TRACKING_PASSWORD=403b889fbd11e85790b79a1b69c6b87ae4e20c78 \
python script.py

```bash Dugshub
export MLFLOW_TRACKING_URI="https://dagshub.com/LiorTet/Mlflow-test.mlflow"
export MLFLOW_TRACKING_USERNAME=LiorTet
export MLFLOW_TRACKING_PASSWORD=403b889fbd11e85790b79a1b69c6b87ae4e20c78
´´´
sudo apt update
sudo apt install python3-pip
sudo pip3 install pipenv
sudo pip3 install virtualenv
mkdir mlflow
cd mlflow
pipenv install mlflow
pipenv install awscli
pipenv install boto3
pipenv shell
## Then set aws credentials
aws configure
#Finally configure it with an s3
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/

# To use it with Sagemaker it is actually fantastic. Automatically creates the ECR and pushes it and also
# deploys the model as well as very easy prediction. Actually wonderfull. 
# https://gitlab.com/juliensimon/sagemaker-automation/-/tree/master/mlflow/direct-marketing-xgboost

