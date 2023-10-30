Welcome to my B-DOP-500 Advanced DevOps project! In this project, I've orchestrated a containerized application using Kubernetes, becoming the "Leonard Bernstein of Containers." Below is a brief overview of the project.

Project Overview
Application Components
This project involved deploying a web poll application with the following components:

Poll: A Flask Python web application that collects votes and pushes them into a Redis queue.
Redis: A queue for holding votes sent by the Poll application.
Worker: A Java application that consumes votes from the Redis queue and stores them in a PostgreSQL database.
PostgreSQL: A database for persistently storing votes.
Result: A Node.js web application for displaying the results.
Specifications
I defined various resources in my Kubernetes cluster, including databases, services, a load balancer, and a monitoring tool. The project required detailed configuration, as outlined in the project description.

Deployment
I followed the deployment process provided in the project description, creating necessary resources and services in Kubernetes. Additionally, I manually set up the PostgreSQL database.

Environment Requirements
I ensured that my Kubernetes cluster had at least one master and two worker nodes. To make the project more manageable, I ran it on a "Kubernetes as a Service" platform, which provided the required infrastructure.

Project Structure
The repository contains the following configuration files:

cadvisor.daemonset.yaml
poll.deployment.yaml
poll.ingress.yaml
poll.service.yaml
postgres.configmap.yaml
postgres.deployment.yaml
postgres.secret.yaml
postgres.service.yaml
postgres.volume.yaml
redis.configmap.yaml
redis.deployment.yaml
redis.service.yaml
result.deployment.yaml
result.ingress.yaml
result.service.yaml
traefik.deployment.yaml
traefik.rbac.yaml
traefik.service.yaml
worker.deployment.yaml
Accessing the Application
I configured the necessary DNS entries and provided access details in the project description to access the web poll application.