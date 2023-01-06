# SecureX Alerting through MS Teams
## Preparation
1. Once logged into your SecureX tenant, create a Threat Response API client with all scopes. For this, go the Administration then Select API Clients in the left panel and click on the Generate API Client button. Click on the Select All link in the Scopes Section and click on the Add New Client button. Copy Threat Response client ID and Client Password and save them somewhere.

2. Now go to the your SecureX tenant Web GUI, and go to Orchestration. Then Create a SecureX Token named CTR_SecureX_Token See Instructions here . Or you can use the one you may have already created into your SecureX Tenant. In a few words, for creating it, open the Orchestration table then on the left panel go to Account Keys . Click on the New Account Key button and create a new account key named CTR_SecureX_Token with the SecureX_Token Account key type. OR check that a SecureX token already exist and use this one in the next steps.

## Setup
### 1 - Create Feeds
> First clean up:
--> Go to Threat Response => Feeds and check that SecureX_Firewall_Private_xxx feeds. If they exist delete all of them.
--> Then you have to do the same with indicators. Go to Indicators go to Source:Private and Delete all Secure_Firewall_SecureX_xxx indicators.

> Run "0015A-SecureFirewall-BlockObservable-Setup" (Get it from Cisoc GitHub Repo through import in SecX)

### 2 - Import other Workflows
Import: 
- Add IP to Feed through Webhook.json
- Secure Firewall - Block Observable.json
- SecureX Incidents - Send Alerts.json
- Send MS Teams Message.json
