+++
title = "Getting Started"
weight = 20
+++

There are mutiple ways to run the app but **Docker Compose** is the easiest way to begin !

To see all the documentation about running the app, visit [Chapter 2](/running)


{{% notice info %}}
Docker Compose launches a full environnement with a pre-configured Prometheus and Grafana 
{{% /notice %}}

## 1. Install Requirements
* Docker (>19.03.0)
* Docker-Compose 

## 2. Modify config
Edit the `config.yaml` file located in `docker-compose` folder. Complete the file with the provided example or visit the [chapter 3](/config) of the documentation to know more about writing config file. 

*Example Config:* 
```yaml
---
shares:
- name: Apple
  symbol: AAPL
  purchase:
    quantity: 1
    fee: 2
    cost_price: 119.98
  estate:
    quantity: 2
    received_dividend: 2.85
```


## 3. Run the stack
Run the following command in the `docker-compose` folder :

```bash
docker-compose up -d
```


## 4. Visit Grafana
Connect to Grafana (`http://localhost:3000`) with the following credentials:
* login:  `admin`
* password: `admin`
    
and go to dashboard **Stock share monitoring**

*NB:* please wait ~10m to see all the cells getting filled
