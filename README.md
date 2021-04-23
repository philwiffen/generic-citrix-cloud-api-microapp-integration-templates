# generic-citrix-cloud-api-microapp-integration-templates
Generic, importable, templates to help you get up and running more quickly with Citrix Cloud APIs, API Proxy, and Citrix Microapps integrations

## Uh, why?
I made these for myself. I needed an importable template I could use to quickly get a fresh Microapp Integration going that could use the Citrix Cloud API Proxy and Citrix Cloud APIs to develop/hack on microapps.

## How do I use them?
First, determine if you need the "CWSauth bearer=" edition, or the "Bearer" edition. Currently, Citrix Cloud APIs vary in what they'll accept as a Bearer token format. You can change this yourself in the auth header prefix field in the microapp integration configuration, but I'm lazy, so made two importable templates :)

If Header needs "Authorization: CwsAuth Bearer=" then use generic_citrix_api_template_for_cwsauth_method.mapp
If Header needs "Authorization: Bearer " then use generic_citrix_api_template_for_bearer_auth_method.mapp

Next, import the .mapp into the Microapps service

Then configure the Integration and change:

Base URL - to whatever API endpoint you need to hit :)

Token URL - to whatever API Proxy you wish to use (I provide a default US one)

Token URL Customer ID - replace {CUSTOMER_ID} with your own customerID, for example, I might put https://api-us.cloud.com/cctrustoauth2/acme_corp/tokens/clients

Client Secret and Client Password to be what you setup in Citrix Cloud > Identity and Access Management > Secure Clients (see https://developer.cloud.com/getting-started/docs/overview for better instructions)

Then uh, get playing :)
