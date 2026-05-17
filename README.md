# Network Infrastructure

Per-account network infra — VPC, subnets, TGW, NAT, KMS, SGs, SSM, VPCE, flow logs.

## Structure
```
accounts/
├── nonprod/
│   └── {account_id}/
│       ├── main.tf
│       ├── variables.tf
│       └── tags.tfvars
├── prod/
└── dr/
```

## Pipeline order
1. Log Account Pipeline
2. Checkov Account File
3. TGW Pipeline
4. **Network Infra Pipeline** ← this repo

## Tags
All 24 mandatory tags must be set in `tags.tfvars` before pipeline runs.
