# Product Requirements Document (PRD)  
**Project Title:** AWS-Native GRC Compliance Lab  
**Author:** Dex-Xavier  
**Intended Use:** Portfolio project demonstrating GRC engineering, automation, and AI-assisted compliance workflows.  

---

## 1. Purpose & Goals
The purpose of this lab is to create a **fully functional, AWS-native compliance lab environment** that demonstrates the following:

- **Compliance Framework Implementation:** Build and maintain controls aligned with SOC 2, ISO 27001, HIPAA, PCI DSS, and NIST CSF.  
- **Crosswalks & Mappings:** Implement a framework-agnostic common-control library with mappings across multiple standards.  
- **Automation & Monitoring:** Deploy automated compliance checks (e.g., AWS Config rules, Lambda functions, CloudWatch alarms).  
- **AI-Augmented Workflows:** Provide examples of LLM-assisted compliance guidance (e.g., control rationales, remediation suggestions).  
- **Beginner-Friendly Learning:** Include step-by-step instructions, dummy data, and modular templates for replication.  
- **Portfolio Value:** Demonstrate technical, instructional, and product-thinking skills aligned with the Vanta GRC Engineer role.  

---

## 2. Target Audience
- **Primary:** Hiring managers and recruiters evaluating GRC engineering skills.  
- **Secondary:** Students, junior analysts, and professionals seeking to replicate the lab for their own learning.  

---

## 3. Scope
The lab will include:

1. **AWS Infrastructure (Cost-Effective):**
   - VPC with public/private subnets  
   - EC2 instance (t2.micro) for demo workloads  
   - S3 bucket with dummy compliance evidence files  
   - IAM roles/policies for least privilege  
   - AWS Config enabled with sample rules (e.g., encryption, MFA, logging)  
   - CloudWatch for monitoring  

2. **Compliance Framework Content:**
   - YAML/JSON files defining canonical controls (dummy IDs, rationales, acceptance criteria)  
   - Crosswalk mappings across SOC 2, ISO 27001, HIPAA, PCI DSS, NIST CSF  
   - Evidence dictionary (dummy file names, log sources, configs)  

3. **Automation & Continuous Monitoring:**
   - Lambda functions for compliance checks (e.g., S3 encryption enabled, IAM key rotation)  
   - CloudFormation/Terraform templates for reproducible setup  
   - Automated test scripts (Python/pytest) validating compliance rules  

4. **AI-Augmented Features:**
   - Prompt templates for LLM-assisted compliance guidance (e.g., “Explain SOC 2 CC6.1 in plain English”)  
   - Example remediation suggestions generated via AI  
   - Safe-use guidelines for AI in compliance (dummy playbook)  

5. **Beginner-Friendly Documentation:**
   - Step-by-step setup guide (Markdown in repo)  
   - Walkthrough tasks (e.g., “Deploy lab,” “Trigger compliance violation,” “Run automated test,” “Review AI guidance”)  
   - Screenshots or diagrams (auto-generated placeholders)  

---

## 4. Functional Requirements
| Requirement | Description | Acceptance Criteria |
|-------------|-------------|----------------------|
| **Infrastructure Setup** | Deploy AWS-native lab with minimal cost | CloudFormation/Terraform script provisions VPC, EC2, S3, IAM, Config |
| **Control Library** | Define canonical controls with mappings | JSON/YAML files with at least 10 controls mapped across 3+ frameworks |
| **Evidence Simulation** | Provide dummy evidence files | S3 bucket contains placeholder logs, configs, PDFs |
| **Compliance Automation** | Automated checks for key controls | Lambda functions validate encryption, IAM, logging |
| **Continuous Monitoring** | Alerts for violations | CloudWatch alarms trigger on non-compliance |
| **AI-Augmented Guidance** | Provide LLM prompt templates | Markdown file with 5+ reusable compliance prompts |
| **Documentation** | Beginner-friendly setup & usage | README includes step-by-step instructions with screenshots |

---

## 5. Non-Functional Requirements
- **Cost Efficiency:** Use free-tier eligible AWS resources where possible.  
- **Reproducibility:** All infrastructure defined as code (IaC).  
- **Beginner Accessibility:** Clear instructions, dummy data, no prior AWS expertise required.  
- **Extensibility:** Modular design for adding new frameworks, controls, or automations.  
- **Emoji Usage Constraint:**  
  - Emojis are **permitted only in `README.md` files** (top-level or within subfolders).  
  - Emojis are **prohibited in all code artifacts**, including CloudFormation, Terraform, Python, JSON, YAML, and AI playbooks.  
  - Acceptance Criteria: No emojis appear in any code/config files; emojis appear only in documentation where appropriate.  

---

## 6. Deliverables
- **Infrastructure-as-Code (IaC):** CloudFormation/Terraform templates  
- **Control Library:** JSON/YAML files with mappings  
- **Automation Scripts:** Python/Lambda functions for compliance checks  
- **Evidence Files:** Dummy logs, configs, PDFs in S3  
- **Documentation:** README.md with setup guide, walkthrough tasks, and diagrams  
- **AI Playbook:** Markdown file with prompt templates and safe-use guidelines  

---

## 7. Example Walkthrough Tasks
1. Deploy the lab using CloudFormation/Terraform.  
2. Upload dummy evidence files to S3.  
3. Trigger a compliance violation (e.g., disable S3 encryption).  
4. Run Lambda compliance check and observe CloudWatch alert.  
5. Use AI prompt template to generate remediation guidance.  
6. Review crosswalk mapping for the violated control.  

---

## 8. Success Metrics
- **Portfolio Impact:** Demonstrates alignment with GRC Engineer JD.  
- **Replicability:** At least 3 external users can replicate lab successfully.  
- **Automation Coverage:** At least 5 automated compliance checks implemented.  
- **AI Integration:** At least 3 AI-assisted workflows demonstrated.  

---

## 9. Future Enhancements
- Add FedRAMP/NIST 800-53 mappings.  
- Integrate with AWS Security Hub.  
- Expand AI workflows (e.g., automated assessor Q&A triage).  
- Add risk quantification module (FAIR-lite).  

---

## 10. Repository Structure

The project repository must follow this structure to ensure clarity, reproducibility, and alignment with the PRD:

aws-grc-compliance-lab/
│
├── infrastructure/
│   ├── cloudformation/lab-environment.yaml
│   ├── terraform/main.tf
│   └── README.md
│
├── controls/
│   ├── canonical-controls.yaml
│   ├── mappings/
│   │   ├── soc2-mapping.json
│   │   ├── iso27001-mapping.json
│   │   ├── hipaa-mapping.json
│   │   └── nist-csf-mapping.json
│   └── evidence-dictionary.yaml
│
├── automation/
│   ├── lambdas/
│   │   ├── s3_encryption_check.py
│   │   ├── iam_key_rotation_check.py
│   │   └── cloudtrail_enabled_check.py
│   ├── tests/test_compliance_checks.py
│   └── README.md
│
├── evidence/
│   ├── dummy-logs/cloudtrail-log.json
│   ├── dummy-logs/config-log.json
│   ├── dummy-policies/access-policy.pdf
│   └── README.md
│
├── ai-playbook/
│   ├── prompt-templates.md
│   ├── remediation-samples.md
│   └── safe-use-guidelines.md
│
├── docs/
│   ├── setup-guide.md
│   ├── walkthrough-tasks.md
│   ├── architecture-diagram.png
│   └── faq.md
│
├── .gitignore
├── LICENSE
└── README.md

---

## 11. Security Considerations & Best Practices

The lab environment must be designed and documented with security in mind, even though it uses dummy data and minimal AWS resources.  

**Infrastructure Security**
- Enforce **least privilege IAM policies** for all roles and users.  
- Enable **multi-factor authentication (MFA)** for IAM users (where applicable).  
- Require **encryption at rest** (S3 buckets, EBS volumes) and **in transit** (TLS for endpoints).  
- Use **VPC segmentation** (public vs. private subnets) to isolate resources.  
- Enable **CloudTrail** and **Config** for auditing and traceability.  

**Application & Automation Security**
- Lambda functions must use **least privilege execution roles**.  
- Store no secrets in code; use **AWS Secrets Manager** or **SSM Parameter Store** for dummy credentials.  
- Validate inputs in automation scripts to avoid misconfigurations.  

**Data Handling**
- All evidence files are **dummy placeholders**; no real sensitive data should ever be used.  
- Document safe handling practices to reinforce compliance culture.  

**AI-Augmented Workflows**
- Provide **safe-use guidelines** for prompts and agents (e.g., no sensitive data in prompts, versioning of templates).  
- Include **evaluation sets** to measure accuracy and drift.  
- Document **refusal policies** for unsafe or privacy-violating requests.

**Operational Best Practices**

- Apply **infrastructure-as-code (IaC)** for reproducibility and auditability.
- Version control all mappings, controls, and automation scripts.
- Provide **logging and monitoring** for compliance checks (CloudWatch, Config).
- Document **incident response steps** for when a compliance violation is detected in the lab.
