# MongoDB Deployment on Kubernetes

This readme file outlines the steps to deploy MongoDB on a Kubernetes cluster using the following steps:

## Step 1: Create Storage Class

Begin by defining a StorageClass to provision storage for MongoDB within your Kubernetes cluster. Use the provided YAML file `createStorageClass.yaml` and apply it using `kubectl apply -f`.

## Step 2: Deploy Persistent Volume

Deploy a PersistentVolume (PV) on the cluster to allocate storage resources. The `createPersistentVolume.yaml` file contains the configurations needed for this step. Apply it using `kubectl apply -f`.

## Step 3: Deploy Persistent Volume Claim

Next, deploy a PersistentVolumeClaim (PVC) to request storage resources for MongoDB. The `createPersistentVolumeClaim.yaml` file specifies the storage requirements. Apply it using `kubectl apply -f`.

## Step 4: Install MongoDB

Deploy MongoDB onto the Kubernetes cluster using the `createDeployment.yaml` file. Customize the configurations based on your requirements, whether as a standalone instance or a replica set. Apply the YAML file using `kubectl apply -f`.

## Step 5: Deploy Service

Expose MongoDB to other parts of your application by deploying a Service. Use the `createService.yaml` file to define the service configuration and apply it using `kubectl apply -f`.
## Step 6: Check the Database

Verify the functionality of MongoDB after deployment. Access the MongoDB instance using tools like MongoDB Compass, utilizing the login credentials and designated port specified in the deployment and service files. Confirm the operational status of the database.

## Step 7: Deploy Configuration and Secrets

Manage application settings and sensitive information by deploying a ConfigMap and a Secret. Apply the configurations using `kubectl apply -f` with the `createConfigMap.yaml` and `createMongoDbSecret.yaml` files.

## Step 8: Verification

Finally, verify the successful deployment of MongoDB by checking the status of pods using `kubectl get pods`. Ensure all replicas of MongoDB are running without any issues, indicating a successful deployment ready for use by your application.
