# Infrastructure

IaC assets for provisioning the AWS-Native GRC Compliance Lab. Choose the stack that fits your workflow:

- `cloudformation/`: YAML template for a one-click deployment experience.
- `terraform/`: Terraform configuration for iterative development and extension.

Each stack should provision the baseline lab resources defined in the PRD (VPC, EC2 demo workload, S3 evidence bucket, IAM roles, AWS Config, and CloudWatch monitoring).

## Status

Templates are currently being scaffolded. Track progress in this README as components are implemented.
