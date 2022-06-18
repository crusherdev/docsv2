---
title: 🐳 Docker deploy
sidebar_label: 🐳 Docker deploy
---

We've tried to make it super easy to install Crusher locally. It is the best option if you're looking to try Crusher locally.

:::tip
If you want to use Crusher regularly, either deploy crusher on server or use Crusher Cloud. With this your assests and service is always publicly available.
:::


#### Requirement

Make sure you've machine with 3 vCPU and 4GB RAM available (minimum).

Recommened -  4 vCPU and 4GB RAM available (minimum).


## Steps to deploy using docker


Before starting, make sure you have [docker](https://docs.docker.com/engine/install/) installed and git installed.

  
1.) Clone git repo.

``` shell
git clone https://github.com/crusherdev/crusher-docker-deploy.git
```
##### With Postgres/Redis

2.) Start the containers.

``` shell
docker-compose up
```
  
##### Withour Postgres/Redis


2.) Change `.env` file and the start the container using

``` shell
source .env && docker compose -f docker-compose-plain.yml up
```


  

3.) Wait for all container to spin up, check  status with ```docker ps```

  

  

4.) (Optional) Point crusher config for endpoint.


 
 ##### Reference

***Other helpful resources after docker deploy***

- Expose crusher publicly using tunnel

- Host crusher on VPS server such as AWS, etc.

- Import test from crusher system
- 
 P.S.- It's not recommended to deploy Crusher in CI as it's stateful application. 