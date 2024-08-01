Overview
========

Welcome to Astronomer! This project was generated after you ran 'astro dev init' using the Astronomer CLI. This readme describes the contents of the project, as well as how to run Apache Airflow on your local machine.

Project Contents
================

Your Astro project contains the following files and folders:

- dags: This folder contains the Python files for your Airflow DAGs. By default, this directory includes one example DAG:
    - `example_astronauts`: This DAG shows a simple ETL pipeline example that queries the list of astronauts currently in space from the Open Notify API and prints a statement for each astronaut. The DAG uses the TaskFlow API to define tasks in Python, and dynamic task mapping to dynamically print a statement for each astronaut. For more on how this DAG works, see our [Getting started tutorial](https://www.astronomer.io/docs/learn/get-started-with-airflow).
- Dockerfile: This file contains a versioned Astro Runtime Docker image that provides a differentiated Airflow experience. If you want to execute other commands or overrides at runtime, specify them here.
- include: This folder contains any additional files that you want to include as part of your project. It is empty by default.
- packages.txt: Install OS-level packages needed for your project by adding them to this file. It is empty by default.
- requirements.txt: Install Python packages needed for your project by adding them to this file. It is empty by default.
- plugins: Add custom or community plugins for your project to this file. It is empty by default.
- airflow_settings.yaml: Use this local-only file to specify Airflow Connections, Variables, and Pools instead of entering them in the Airflow UI as you develop DAGs in this project.

Deploy Your Project Locally
===========================

1. Start Airflow on your local machine by running 'astro dev start'.

This command will spin up 4 Docker containers on your machine, each for a different Airflow component:

- Postgres: Airflow's Metadata Database
- Webserver: The Airflow component responsible for rendering the Airflow UI
- Scheduler: The Airflow component responsible for monitoring and triggering tasks
- Triggerer: The Airflow component responsible for triggering deferred tasks

2. Verify that all 4 Docker containers were created by running 'docker ps'.

Note: Running 'astro dev start' will start your project with the Airflow Webserver exposed at port 8080 and Postgres exposed at port 5432. If you already have either of those ports allocated, you can either [stop your existing Docker containers or change the port](https://www.astronomer.io/docs/astro/cli/troubleshoot-locally#ports-are-not-available-for-my-local-airflow-webserver).

3. Access the Airflow UI for your local Airflow project. To do so, go to http://localhost:8080/ and log in with 'admin' for both your Username and Password.

You should also be able to access your Postgres Database at 'localhost:5432/postgres'.

Deploy Your Project to Astronomer
=================================

If you have an Astronomer account, pushing code to a Deployment on Astronomer is simple. For deploying instructions, refer to Astronomer documentation: https://www.astronomer.io/docs/astro/deploy-code/

Contact
=======

The Astronomer CLI is maintained with love by the Astronomer team. To report a bug or suggest a change, reach out to our support.
![airflow-1 1](https://github.com/user-attachments/assets/a8b5a9c9-2dbf-4ac4-bb23-48c39acf41e7)
![aiflow-1 2](https://github.com/user-attachments/assets/f5a093ea-91ab-411f-b84f-38c73aadfc6d)
![airflow-2](https://github.com/user-attachments/assets/70c39615-f1e4-4bb7-8765-6f9c5ac11c05)
![airflow-3](https://github.com/user-attachments/assets/51cd61a7-ba69-45c3-8e2a-f5aa54e4f823)
![airflow-dag](https://github.com/user-attachments/assets/475438d0-4d61-490e-b07c-533174550da5)
![airflow-tasks](https://github.com/user-attachments/assets/110d9e82-70b2-4538-bc4e-5393
![aiflow-requirements](https://github.com/user-attachments/assets/e69eb52f-9ba0-4ca2-9456-d578ec9b3efb)
8e563503)
![airflow-minio](https://github.com/user-attachments/assets/c0afb6d7-4ea9-4048-81c2-500332d02d13)
![airflow-spark master](https://github.com/user-attachments/assets/14cd31a6-d728-4b78-b45c-ad6ad9777deb)
![airflow-spark worker](https://github.com/user-attachments/assets/f0fc9afd-f136-43fa-a2ef-f6ceef6bce4a)
![airflow-Metabase](https://github.com/user-attachments/assets/b78bc287-570a-46ef-a9ef-88abf3d8bcb7)
![airflow-slack](https://github.com/user-attachments/assets/b1366660-c4f6-4965-a35b-22bff5f8fe0e)


