# Build a Heat Map Tile App with Alibaba Cloud ECS & PostgreSQL

>**Disclaimers：**This service is provided by a third party, and we make every effort to ensure its security, accuracy, and reliability, but we cannot guarantee that it is completely free from failures, interruptions, errors, or attacks. Therefore, our company hereby declares that we make no representations, warranties or commitments regarding the content, accuracy, completeness, reliability, applicability, and timeliness of this service, and we are not liable for any direct or indirect losses or damages arising from your use of this service; For the third-party websites, applications, products, and services accessed by you through this service, you are not responsible for their content, accuracy, completeness, reliability, applicability, and timeliness. You shall bear the risks and responsibilities arising from the consequences of use on your own; We are not responsible for any losses or damages arising from your use of this service, including but not limited to direct, indirect, profit, goodwill, data or other economic losses, even if our company has been informed in advance of the possibility of such losses or damages; We reserve the right to modify this statement from time to time, so please regularly check this statement before using this service. If you have any questions or concerns about this statement or this service, please contact us.

## Overview

A Heat Map Tile is a data visualization tool that represents the spatial distribution of data by overlaying colored tiles on a map. Each tile's color intensity reflects the magnitude or concentration of a particular metric within that area. Heat Map Tiles are often used to visualize geographic data, making it easier to identify patterns, trends, and outliers at a glance.

## Billing instructions

The expenses on Hmt mainly involve：

- Selected vCPU and memory specifications
- System disk type and capacity
- Public network bandwidth
- Cloud database PostGreSQL specifications and storage space

## Deployment Architecture

<img src="1.png" width="1500" height="700" align="bottom"/>

## Parameter Description

| Parameter Group            | Parameter item          | illustrate                                                                                                                                           |
|----------------------------|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Service Instance           | Service Instance Name   | The name can be up to 64 characters in length, and can contain digits, letters, hyphens (-), and underscores (_). The name must start with a letter. |
|                            | Region                  | The region where the service instance is deployed.                                                                                                   |
|                            | Instance Charge Type    | Charge type for the service instance.                                                                                                                |
| ECS instance configuration | Instance Type           | ECS instance type                                                                                                                                    |
|                            | Instance Password       | Server login password, Length 8-30, must contain three(Capital letters, lowercase letters, numbers, ()`~!@#$%^&*_-+={}[]:;'<>,.?/ Special symbol in) |
| network configuration      | Availability Zone       | The availability zone where the ECS instance is located                                                                                              |
|                            | VPC ID                  | VPC where resources are located                                                                                                                      |
|                            | VSwitch ID              | The availability zone of the VSwitch                                                                                                                 |
| PostGreSQL configuration   | Instance specifications | The specifications of PostGreSQL instances that can be used in the availability zone                                                                 |
|                            | DatabaseName            | Database Name(default hmt)                                                                                                                           |
|                            | AccountName             | Account Name(default hmt_user)                                                                                                                       |
|                            | EngineVersion           | Engine Version                                                                                                                                       |

## Permissions required

Deploying this service instance requires accessing and creating some Alibaba Cloud resources. Therefore, your account needs to include permissions for the following resources.
  **Note**：You only need to add this permission when your account is a RAM account.

| Permission policy name                 | Remarks                                                                |
|----------------------------------------|------------------------------------------------------------------------|
| AliyunECSFullAccess                    | Permission to manage cloud server service (ECS)                        |
| AliyunVPCFullAccess                    | Permission to manage private network (VPC)                             |
| AliyunROSFullAccess                    | Permission to manage Resource Orchestration Service (ROS)              |
| AliyunComputeNestUserFullAccess        | Manage user-side permissions for the ComputeNest service (ComputeNest) |
| AliyunPostGreSQLFullAccess             | Manage permissions for cloud database services (PostgreSQL)            |

## Deployment steps

1.Visit Deployment Link and fill in the deployment parameters as prompted:[Deployment link](https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceId=service-3fc795faef2148658afe)

![image.png](2.png)

2.After filling in the deployment link parameters, you can see the corresponding inquiry details. After confirming the parameters, click **Next step: Confirm the order**.

![image.png](3.png)

3.After confirming the completion of the order, agree to the service agreement and click **Create Now** to enter the deployment phase.

![image.png](4.png)

4.Wait for deployment to complete before entering service instance management.

5.Find Hmt links in the console and copy them to the browser to access them.

![image.png](5.png)
![image.png](6.png)

## Reference documents
https://aliyuque.antfin.com/xdc01323960/tyfivo/id1gp04h7kp3n66b?singleDoc=