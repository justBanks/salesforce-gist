# Developer Guide - Salesforce API Integration
All about the integration between DemocracyLab's web site and Salesforce instance

Based on [OAuth 2.0 JWT Bearer Flow for Server-to-Server Integration](https://help.salesforce.com/articleView?id=remoteaccess_oauth_jwt_flow.htm)

## Overview 
Access to Salesforce data is provided by the Lightning Platform REST API. Exposing this API from DemocracyLab's Salesforce instance		is achieved by configuring a Salesforce connected app, which in our case is named "DemocracyLab Integration." This connected app provides the API client key.

![App Manager](https://user-images.githubusercontent.com/277740/98370404-8352c900-2008-11eb-911d-9e4400471465.png)

*Note: When working with a sandbox org, refreshing the sandbox will change the client key and invalidate the previous security configuration*

## Security 
Some important securtiy settings:

![AppManager2](https://user-images.githubusercontent.com/277740/98378979-bdc26300-2014-11eb-8f41-4d2735c68fb1.png)

![image](https://user-images.githubusercontent.com/277740/98376388-65d62d00-2011-11eb-9d01-778382b021b2.png)

### Create the X509 Certificate
Use some cryptography framework (e.g. OpenSSL) to create a private key and a self-signed certificate

Create the JWT (JSON web token) from the certificate's private key. You could use are Node's built-in crypto module or the pyjwt library, to name just two available alternatives
 
## 

## Postman Collection of API Requests
See https://documenter.getpostman.com/view/150694/SzmY9MgZ 

Other developer resources

- https://github.com/scolladon/postman-salesforce-apis#readme
- https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/dome_upsert.htm
