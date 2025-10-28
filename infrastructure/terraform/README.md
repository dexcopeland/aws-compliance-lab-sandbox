# Terraform Lab Configuration

This directory will house Terraform configuration (`main.tf` and supporting files) for provisioning the AWS-Native GRC Compliance Lab defined in the PRD.

## Planned Modules

- Networking (VPC, subnets, routing tables, IGW)
- Compute (EC2 instance with IAM instance profile)
- Storage (S3 evidence bucket + bucket policies)
- Identity (IAM roles and policies enforcing least privilege)
- Monitoring (Config recorder, CloudTrail trail, CloudWatch alarms)

## Next Steps

1. Scaffold `main.tf` with providers, backend, and networking module.
2. Add IAM and EC2 resources.
3. Integrate S3 evidence bucket and encryption policies.
4. Configure AWS Config, CloudTrail, and CloudWatch.
5. Validate with `terraform init`, `plan`, and `apply` in a test account.
