# Terraform S3 Backend with DynamoDB Locking

This Terraform project creates an S3 bucket for storing Terraform state files and a DynamoDB table for state locking. The S3 bucket is configured with versioning, server-side encryption, and strict access controls to ensure security.

## Resources Created 1

1. **S3 Bucket**:
   - Name: `terraform-backend-bucket08` (replace with your unique bucket name).
   - Versioning is enabled to keep track of state file changes.
   - Server-side encryption (SSE) is enabled using AES-256.
   - A bucket policy enforces HTTPS for all requests and blocks public access.

2. **DynamoDB Table**:
   - Name: `terraform-dynamodb-table01` (replace with your unique table name).
   - Used for Terraform state locking to prevent concurrent operations.
   - Billing mode: Pay-per-request.

## Prerequisites

- **Terraform**: Ensure Terraform is installed on your machine. You can download it from [here](https://www.terraform.io/downloads.html).
- **AWS Account**: You need an AWS account with credentials configured (access key and secret key).
- **AWS CLI**: Optional but recommended for managing AWS credentials. Install it from [here](https://aws.amazon.com/cli/).

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
