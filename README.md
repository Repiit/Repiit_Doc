# Repiit Integration Documentation
Documentation of integration with Repiit Subscription service

## Base address
### Test
`portalmanagertest.repiit.com`

### Drift
`portalmanager.repiit.com`

## Dataset
When you make an agreement you will be giving information of your dataset, that should be sent with all request to Repiit service

## Purchase of subscription
A subscription in repiit consist of excactly one product.
To start the process of letting the customer buy a subscription, the customer should be referred to the following url. Our recomendation is to this in either a new browser window or in an IFrame

`https://<base_address>/#customerLogin?DATASET=<Dataset>&ITEMNUMBER=<Itemnumber>`
  
## Get all new orders
Every night We will make new orders for all subscription there should be renewed. The following API endpoint

```MEDTOD: GET
ENDPOINT: https://<base_address>/api/SalesController/GetOrders```
