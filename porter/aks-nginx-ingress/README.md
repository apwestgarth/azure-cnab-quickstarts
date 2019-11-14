# Installs an nginx ingress controller to an AKS cluster

## Simple deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-cnab-quickstarts%2Faks-nginx-ingress-2%2Fporter%2Faks-nginx-ingress%2Fazuredeploy-simple.json" target="_blank"><img src="https://raw.githubusercontent.com/endjin/CNAB.Quickstarts/master/images/Deploy-from-Azure.png"/></a>

## Advanced deployment

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-cnab-quickstarts%2Faks-nginx-ingress-2%2Fporter%2Faks-nginx-ingress%2Fazuredeploy-advanced.json" target="_blank"><img src="https://raw.githubusercontent.com/endjin/CNAB.Quickstarts/master/images/Deploy-from-Azure.png"/></a>

This Quickstart installs an nginx ingress controller onto an existing AKS cluster, and configures a cert-manager with a Let's Encrypt certificate issuer.

## Parameters and Credentials

 | Name | Description | Default | Required | 
 | --- | --- | --- | --- | 
 | azure_client_id | AAD Client ID for Azure account authentication - used for Az CLI |  | Yes
azure_client_secret | AAD Client Secret for Azure account authentication - used for Az CLI |  | Yes
azure_subscription_id | Azure Subscription Id used to set the subscription where the account has access to multiple subscriptions |  | Yes
azure_tenant_id | Azure AAD Tenant Id for Azure account authentication  - used for Az CLI |  | Yes
cert_manager_helm_chart_version | Version number for the cert-manager Helm chart |  | No
cert_manager_installation_name | Installation name for cert-manager Helm deployment |  | No
cert_manager_namespace | Kubernetes namespace for nginx-ingress installation |  | No
controller_replica_count | Replica count for ingress controller |  | No
dns_name | The DNS name to to associate with public IP address for the FQDN |  | Yes
kubeconfig |  |  | Yes
letsencrypt_email | Valid email address to use for Let's Encrypt certificate |  | Yes
letsencrypt_environment | The environment to use for Let's Encrypt certificates |  | No
nginx_ingress_helm_chart_version | Version number for the nginx-ingress Helm chart |  | No
nginx_ingress_installation_name | Installation name for nginx-ingress Helm deployment |  | No
nginx_ingress_namespace | Kubernetes namespace for nginx-ingress installation |  | No
porter-debug | Print debug information from Porter when executing the bundle |  | No | 