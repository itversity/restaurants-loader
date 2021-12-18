# Restaurants Loader

## Pre-requisites

Here are the pre-requisites to use this repository.
* Make sure Docker Desktop is setup on Windows or Mac.
* Make sure to change the settings of Docker Desktop. Here are the instructions for Mac.
  * Go to **Preferences** of Docker Desktop
  * Change memory to 8 GB and CPUs to 4

## Setup Repository

Make sure to clone the repository by using following command.

```shell
git clone https://github.com/itversity/restaurants-loader.git
```

## Setup Data Set

Make sure to copy **train_full.csv** to **data** folder in this repository. 
* **data** folder is already in the **restaurants-folder** which will be created after running the `git clone` command to setup the repository.

## Start Docker Containers

Let us start the docker containers and also understand details of those. 

* Make sure to be in the **restaurants-folder** before running below commands.
* Make sure to create a Docker network by name **restlabnw**

```shell
docker network create restlabnw
```

* Start all the containers.

```shell
docker compose up -d --build
```

* It will start 3 containers (jupyter lab, postgres and mongodb). You can see the details by running below command.

```shell
docker compose ps
```

## Launching Jupyter Lab

Here are the instructions to launch jupyter lab.
* Make sure to be in the **restaurants-folder** before running below commands.
* Run `docker compose logs restlab` command.
* Make sure to copy the URL which is in the below format and then run using browser.

```text
http://127.0.0.1:8888/lab?token=951a079c387d80c9e6182bfcda00ddb8a95d0d2e2c7052a2
```

## Accessing Notebooks

Once you are in the Jupyter Lab environment, you should be able to see the notebooks
