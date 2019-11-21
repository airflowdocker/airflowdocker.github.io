## Welcome to Airflow Docker!

### What is it?

Airflow Docker is an extension to the open source project [Airflow](https://airflow.apache.org/).  Specifically it provides a base operator, forked from the existing docker operator, and a number of operators, and sensors on top of it, all that are fundamentally a wrapped `docker run` command.

### Ok. Its docker. We get it. But why?!?

By standardizing around a single execution pattern, namely _everything_ is a docker operator, a number of benefits fall into place:

1. All of the normal benefits of docker. Shared layers, immutable artifacts, artifact versioning, etc.
2. Because everything, from a sensor, to a short circuit operation, to a sql query type operation, to a standard python type operation, we were able to begin to build useful building blocks that augmented this standard run time behavior.
3. Isolation with respect to the airflow deployment itself - we can feel a lot more confident upgrading airflow or one of its dependencies if that has almost no chance of breaking somene's tasks.

### So what is included?

1. [airflow-docker](https://github.com/airflowdocker/airflow-docker): This is the core library. It is inteded to be installed in the same environment as airflow.  We publish python packages to the python package index and a couple of purpose build docker images to dockerhub.
2. [airflow-docker-helper](https://github.com/airflowdocker/airflow-docker-helper): This is a lightweight, pure python library intended to be installed in your docker images that provides useful primitives for interacting with airflow from within the context of a running docker container.

... And more

### List of Repos

Github Repos: [see list](https://github.com/airflowdocker)
Slack: [slack](https://join.slack.com/t/airflow-docker/shared_invite/enQtODQ1MjUzNjc5NzAzLTNjOTkzNmQwNzQ4NGI4MmIzMzdlZTIzZGRjNWVhMTliNGRkOWZhMTJmZDcyNmY2ZTU4ODU3OTQ0NTJmNzdjMDQ)
