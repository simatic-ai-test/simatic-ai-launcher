<!--- Copyright 2020 Siemens AG -->
<!--- SPDX-License-Identifier: MIT -->

# Using a docker container

With the next command you can run a docker container with the necessary packages to run the related ipython notebook. We assume you already have a docker client installed on your system. If you haven't, please refer to the official [docker](https://www.docker.com/get-started) installation guide.

Once you have cloned the repository, please navigate into the environments/dockerized folder. Then you can start the docker container with the next command.  

```commandline
docker-compose -f image-classification.yml up
```

This command corresponds to the image classification sample. If you want to work with another example, choose the relevant docker compose .yaml file. For changing specific settings, you can edit this file. You can find more information about docker compose on the official [docker](https://docs.docker.com/compose/gettingstarted/) website.

Running the compose will download the chosen docker image, install the python dependencies, and start JupyterLab. In the background, the compose file also maps the Jupyter and TensorBoard related ports, as well as the previously cloned folder structure. Depending on your docker client version, you might need to enable folder sharing in its settings.

Once the JupterLab has started you will see the log on your terminal with the url to access it.
```commandline
image-classification    |     To access the notebook, open this file in a browser:
[..]
image-classification    |      or http://127.0.0.1:8888/?token=5075feec682d7b12e3195e76ffb9e93481c0b0abd4f371f2
```

