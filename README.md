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

```
MEDTOD: GET
ENDPOINT: https://<base_address>/API/SalesTableAr/GetOrdersReadyForDelivery
```

This will return an json array of the orders 
```
[
  {
    "DATASET": "string",
    "ROWNUMBER": 0,
    "LASTCHANGED": "2018-10-28T10:07:50.230Z",
    "NUMBER_": "string",
    "SEARCHNAME": "string",
    "CREATED": "2018-10-28T10:07:50.230Z",
    "NEXTDELIVERYDATE": "2018-10-28T10:07:50.230Z",
    "ACCOUNT": "string",
    "NAME": "string",
    "ADDRESS1": "string",
    "ADDRESS2": "string",
    "ZIPCITY": "string",
    "COUNTRY": "string",
    "ATTENTION": "string",
    "PHONE": "string",
    "GROUP_": "string",
    "FIXEDDISCPCT": 0,
    "CURRENCY": "string",
    "LANGUAGE_": 0,
    "VAT": "string",
    "DLVADDRESS1": "string",
    "DLVADDRESS2": "string",
    "DLVZIPCITY": "string",
    "DLVCOUNTRY": "string",
    "YOURREF": "string",
    "OURREF": "string",
    "REFFERENCENUMBER": "string",
    "DISCOUNT": 0,
    "FEETAXABLE": 0,
    "VATAMOUNT": 0,
    "INVOICEAMOUNT": 0,
    "LINEVAT": 0,
    "ORDERBALANCE": 0,
    "VATBASE": 0,
    "EMAIL": "string",
    "DLVEMAIL": "string",
    "CANCELLED": "2018-10-28T10:07:50.230Z",
    "ITEMNUMBER": "string",
    "QTY": 0,
    "PRICE": 0,
    "ITEMTXT": "string",
    "UNITCODE": "string",
    "COSTPRICE": 0,
    "PRICEUNIT": "string",
    "VOUCHER": "string",
    "INVOICENUMBER": "string",
    "INVOICEDATE": "2018-10-28T10:07:50.230Z",
    "STATUS": "string",
    "CARDTRANSID": 0,
    "DELIVERYDESCRIPTION": "string"
  }
]
```
