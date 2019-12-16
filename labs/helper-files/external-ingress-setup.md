Use the doco here to setup a basic Ingress Controller deployed to the  **ingress-external** namespace: https://docs.microsoft.com/en-us/azure/aks/ingress-basic
Here are the instructions for implementing a basic external ingress using the Nginx Ingress controller already setup in the **ingress-external** namespace:

1. Delete the **web** and **api** services
2. Apply **web** and **api** service updates in ***heroes-web-api-clusterip.yaml***
3. Review & update ***heroes-web-api-ingress-svc.yaml*** with the Namespace used for the Heroes app, then Apply to create required **External Services**
4. Apply ***heroes-web-ingress-external.yaml*** to create ingress paths to the Web UI and API
5. ???? Update the Environment Variable **API** in the ***heroes-web-deploy*** deployment to: **http://EXTERNAL_INGRESS_IP/heroes/** (e.g. http://23.96.23.205/heroes/) ??? Doesn't seem necessary ???
