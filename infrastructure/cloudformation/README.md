# CloudFormation Lab Template

This directory will contain the CloudFormation template (`lab-environment.yaml`) for provisioning the AWS-Native GRC Compliance Lab defined in the PRD.

## Planned Resources

- VPC with public and private subnets
- Internet gateway and routing tables for public subnet access
- EC2 instance (t2.micro) to host demo workloads
- S3 bucket for dummy evidence artifacts
- IAM roles and instance profiles enforcing least privilege
- AWS Config recorder and delivery channel
- CloudTrail trail for audit visibility
- CloudWatch metrics and alarms for compliance violations

## Next Steps

1. Draft the initial `lab-environment.yaml` with core networking resources.
2. Layer IAM roles/policies and EC2 instance configuration.
3. Add Config, CloudTrail, and CloudWatch resources.
4. Validate deployment using the AWS CLI or console.
