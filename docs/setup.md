# AWS Environment Setup

## Account
- Offer: AWS Free Tier (12-month + always-free services)
- Root MFA: enabled (never used day-to-day)
- IAM user: oss-pulse-dev (AdministratorAccess + MFA enabled)
- Region: ap-southeast-1 (Singapore)

## Naming Convention
`<workload>-<env>-<initials>-<4-digit-suffix>`

| Resource | Name |
|---|---|
| S3 bucket | oss-pulse-dev-rj-0421 |
| Glue database | oss_pulse_dev |
| Redshift namespace | oss-pulse-dev |
| Secrets Manager | oss-pulse/dev/<secret-name> |
| CloudFormation stack | oss-pulse-dev-infra |
| IAM roles | oss-pulse-dev-<service>-role |

## Tags
Project=oss-pulse, Env=dev, Owner=<your-name>

## Cost Controls
- Budget: $5/month, alerts at 50/80/100% actual spend
- Free Tier usage alerts: enabled
- Policy: delete or stop unused resources at the end of every work session
- Check Cost Explorer weekly

## CLI Setup
aws configure
aws sts get-caller-identity

## Note
> Power BI Desktop remains for visualization (connects to Redshift via ODBC).
> Same medallion architecture (Bronze → Silver → Gold), different managed services.