# az CLI learnt

## List available built-in stacks which can be used for web apps.

`az webapp list-runtimes --linux`


## To find the outbound IP addresses currently used by your app in the Azure portal, 

``` Get outbound IP addresses currently used by your app
az webapp show \
    --resource-group <group_name> \
    --name <app_name> \ 
    --query outboundIpAddresses \
    --output tsv
```

``` Get all possible outbound IP addresses for your app, regardless of pricing tiers
az webapp show \
    --resource-group <group_name> \ 
    --name <app_name> \ 
    --query possibleOutboundIpAddresses \
    --output tsv
```


`az webapp list | jto |select name, resourceGroup, possibleOutboundIpAddresses, outboundIpAddresses`

`az webapp list | jto | select name, resourceGroup`

`az group list | jto | select name, location`

Note: jto is an alias 😉