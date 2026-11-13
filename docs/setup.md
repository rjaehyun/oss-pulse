# Azure Environment Setup

## Account
- Offer: Azure free account ($200 credit / 30 days)
- MFA: enabled
- Region: Southeast Asia (southeastasia)

## Naming Convention
`<type>-<workload>-<env>-<region>-<nn>`  (see table below)

| Resource | Name |
|---|---|
| Resource group | rg-osspulse-dev-sea-001 |
| Storage account | stosspulsedevsea001 |
| Key Vault | kv-osspulse-dev-xxxx |

## Tags
project=oss-pulse, env=dev, owner=<name>

## Cost Controls
- Budget: $10/month, alerts at 50/80/100% actual + 100% forecast
- Policy: delete or stop unused resources at the end of every work session

## CLI Setup
az login
az account set --subscription "<subscription-name>"