# PlatformAppK8S
Kubernetes deployment files for the platform app

## Table of contents
* [Introduction](#introduction)
* [Used technologies](#used-technologies)
* [Project status](#project-status)

## Introduction
In this project all the Kubernetes deployment files for the platform app are stored. The architecture consists of two services - the platforms service 
(https://github.com/Kprzyby/PlatformService) and the command service (command service here - https://github.com/Kprzyby/CommandService) each with their own database
hosted on the SQL Server instance along with a load balancer. I've added a node port to each service for testing purposes. The services communicate between each other
through Azure Service Bus and with their databases thorugh a clusterIP service. The services' endpoints are accessed through an API Gateway in the form of an NGINX Ingress
Controller.

## Used technologies
* Docker
* Kubernetes

## Project status
The project is still in development. In the future I plan on deploying the microservices architecture in the Azure Kubernetes Service.
