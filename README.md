Check out my personal blog for study notes: https://harryqu1229.github.io/



# Project Introduction

__This project was made to help my learning with backend and frontend technologies.__

Easy-Shopping is an easy to use online shopping microservices system that includes an shopping subsystem for buyers and an administrative subsystem for shop owner. The shopping subsystem for buyers is yet to be completed.

Easy-Shopping’s backend provides RESTFUL API for front end to retrieve data for rendering.

Modules include product, order, warehouse, member, coupon, etc...

- Most of the third party services were deployed in docker installed on a Ubunutu virtual machine 
	![image-20210405175658877](https://raw.githubusercontent.com/HarryQu1229/image-host/main/notes-img/image-20210405175658877.png)
- Both shopping subsystem and administrative subsystem’s web pages are made with Vue2 framework and Element-ui.
- Both shopping subsystem and administrative subsystem’s uses SpringBoot2 for development of each module and SpringCloud Hoxton, SpringCloud Alibaba2 to procided additional services such as:
	- SpringCloud Alibaba Nacos -> as service discovery
	- SpringCloud Alibaba Nacos -> as configuration management
	- SpringCloud Ribbon -> for loab balance
	- SpringCloud Feign -> for HTTP clients
	- SpringCloud Alibaba Sentinel -> for flow control and concurrency limiting
	- SpringCloud Gateway -> for API gateway
	- SpringCloud Sleuth -> for monitor and backtracking
	- SpringCloud Alibaba Seata -> for Distrubuted transaction management


| Software names | Version | Description                         |
| -------------- | ------- | ----------------------------------- |
| nginx          | 1.10    | reverse proxy server                |
| elasticsearch  | 7.4.2   | searching                           |
| kibana         | 7.4.2   |                                     |
| nacos          | 1.2.1   | service discovery and configuration |
| redis          | ^       | cache                               |
| mysql          | 5.7     | database                            |

# Module Description

| Module name      | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| mall-auth-server | Login service、Oauth2.0                                      |
| mall-common      | Store constants, utility classes, exceptions, common entities, dependencies, etc... |
| mall-coupon      | Coupon services                                              |
| mall-gateway     | All requests are sent to gateway first to apply routes and filters |
| mall-member      | Member services                                              |
| mall-order       | Order services                                               |
| mall-product     | Product services                                             |
| mall-search      | Elasticsearch operatiun services                             |
| mall-third-party | Third party services、Alibaba Cloud OSS、etc...              |
| mall-ware        | Storage services                                             |
| renren-fast      | [人人开源](https://gitee.com/renrenio) Backend fast development platform |
| renren-fast-vue  | [人人开源](https://gitee.com/renrenio) Frontend fast development platform |

![image](https://user-images.githubusercontent.com/95863581/156907235-e589dfbe-350d-4243-9454-fdaff3e86863.png)
![image](https://user-images.githubusercontent.com/95863581/156907243-67088272-4481-45d6-8aef-a5c2e86c53e4.png)
![image](https://user-images.githubusercontent.com/95863581/156907248-675037a8-6519-4671-adb5-274e88abd82e.png)

