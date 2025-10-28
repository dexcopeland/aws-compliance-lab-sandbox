# Compliance Automation

This module will host Lambda functions, supporting utilities, and tests that automate compliance validation for the AWS-Native GRC Compliance Lab.

## Directory Layout

- `lambdas/`: Python Lambda handlers that execute compliance checks.
- `tests/`: Pytest suite validating Lambda logic and control coverage.

## Planned Checks

1. `s3_encryption_check.py` – Ensures target S3 buckets enforce default encryption.
2. `iam_key_rotation_check.py` – Verifies IAM access keys are rotated within policy windows.
3. `cloudtrail_enabled_check.py` – Confirms CloudTrail is enabled and logging to the evidence bucket.

Each Lambda will publish metrics or findings that integrate with CloudWatch alarms for near-real-time monitoring.
