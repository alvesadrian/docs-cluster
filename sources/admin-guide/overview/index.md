# Overview

[TOC]

Gluu Cluster promises scalability, reliability and a fail-over mechanism through its innovative design implemented using [Docker](https://www.docker.com/). The cluster server can also call a DOS service, like [DOSarrest](http://www.dosarrest.com/), enabling protection from distributed denial of service attacks.
The cluster package deploys the Gluu Server access management suite, which is capable of authenticating and authorizing users with both the SAML and OpenID Connect protocols. We recommended trying a single Gluu Server deployment first for testing as the Cluster packages require a commercial license.

An overview of the Gluu Server is available [here](http://www.gluu.org/docs/admin-guide/getting-started/).

## Design

The Gluu Cluster has two principle compoents that are interdependent, the master and the consumer.
The master package must be installed for the cluster to be functional, and without the master package, the consumer will not work.
The installation instructions are available in the [Installation Docs](../installation/).

![image](../../img/gluu-cluster-overview.png)

The diagram above shows the design structure of Gluu Cluster. The components are held together in various docker containers, accessed using the `gluu-flask` which has a separate User Interface that can be used to manage the cluster. Prometheus is the monitoring system for the cluster prividing real-time reports on the containers.

## Functionalities

The core functionalities of the Gluu Server is available in the cluster design with a few additional features such as cluster monitoring, DDOS protection and a fail-safe system.
The Cluster monitoring system uses Prometheus for alerts and reports on the nodes in real-time.
The cluster administrator can use the dashboard to check on the health and activity, view logs and other Gluu Server administration tasks. The Gluu Server Administration Guide is available [here](http://www.gluu.org/docs/admin-guide/introduction/).

## Supported Operating Systems

The following __64-bit__ operating systems are supported by cluster:

* Ubuntu Trusty (14.04)

_Note_:

* 32-bit operating systems are __not__ supported.
* At least kernel 3.10 at minimum.

## Hardware Requirements

At minimum, the recommended resources for each server in cluster are:

* 4 CPU Units
* 8 GB of RAM
* 80 GB of disk space

## Components

The Gluu Cluster takes advantage of the latest free, open-source, components which work together to provide a hickup-free cluster environment.
The components are listed in the [components page](../components/#components).

## License
There are 3 available licenses for Gluu Cluster deployment:

1. E-Commerce: This license allows a cluster deployed in two separate locations or virtual machines from two different vendors. An example would be a cluster with its master package deployed in Amazon and the consumer deployed in Rackspace. For pricing information please [schedule a meeting](http://www.gluu.org/booking).

2. Premium: This package allows the cluster to be deployed to five (5) locations or virtual machines. The premium package also includes Premium Support. The details are given in the [Gluu Pricing](http://www.gluu.org/gluu-server/pricing/) page.

3. Enterprise: The Enterprise package includes a license for unlimited cluster deployment with an enterprise support. This package will allow any enterprise to create any number of clusters for development, QA and production.
