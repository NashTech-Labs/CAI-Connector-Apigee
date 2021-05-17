# CAI-Connector-Apigee
Hi! This template demostrate how we can make 3rd party API call from Cloud Services Application Integration(CAI) to Apigee specfically but by doing some modifications you make call to any other Platform. 

## what is CAI ?
Informatica® Cloud Application Integration (CAI) service offers a single, trusted solution to support any integration pattern, data set, user-type or endpoint to automate business processes, expedite transactions and enable real-time analytics.

## What is Apigee ?
Apigee is a platform for developing and managing APIs. By fronting services with a proxy layer, Apigee provides an abstraction or facade for your backend service APIs and provides security, rate limiting, quotas, analytics, and more.

![High level overview
  of the Apigee architecture.](https://cloud.google.com/apigee/docs/api-platform/images/ng-saas/ng-saas-arch.png)
  
## How to use this template 

Create account on CAI platform and upload the Customer-1620303739972 zip file using import button. After successful import, you will observe nodes in the API flow where One of the node would be the service CAI connector so using this connecotr we would make a 3rd party call to Apigee platform.
Don't forget to publish the CAI flow, app connection and service connector on cloud server.
Ref for CAI connector - [Connector Doc ](https://docs.informatica.com/integration-cloud/cloud-application-integration/current-version/tutorial----calculator/create-a-service-connector-and-a-connection.html)

Create account on Apigee Management and upload the updateProfile11_rev5_2021_05_06.zip and pulish the API.

## CURL
### Request
>curl --location --request GET 'https://apse1-cai.dm-ap.informaticacloud.com/active-bpel/public/rt/lpnmZstyn6Ef7YjqBn8Tir/Customers?customerId=12&name=22' \
--header 'Cookie: JSESSIONID=9E71C3A97CA4D18B9BB83D734F200941.cai-prod-apse1-r36-app04.infacloudops.net'

### Response -
> {

"id": "1234_98_E_R",
"name": "Ram",
"bankAccount": "1234",
"status": "Delhi",
"address": "123 Rohini delhi",
"vehicle": "Yes"
}
