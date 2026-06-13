# AWS IAM User and Access Management

## Project Overview

This project demonstrates AWS Identity and Access Management (IAM) by creating users, groups, managed policies, and custom policies to implement secure access control for Amazon S3 resources.

The project follows the Principle of Least Privilege by assigning users only the permissions required for their responsibilities.

## AWS Services Used

* AWS IAM (Identity and Access Management)
* Amazon S3

## Project Objectives

* Create IAM users and groups
* Assign AWS managed policies
* Create and attach custom IAM policies
* Implement role-based access control
* Validate permissions through user testing
* Understand security best practices

## IAM Users Created

### cloud-user

* Group: S3-ReadOnly-Group
* Policy: AmazonS3ReadOnlyAccess
* Access Level: Read Only

### s3-admin-user

* Group: S3-FullAccess-Group
* Policy: AmazonS3FullAccess
* Access Level: Full Administrative Access

### custom-s3-user

* Group: Custom-S3-Group
* Policy: Custom-S3-ReadOnly-NoDelete
* Access Level: Read Access with Delete Restrictions

## IAM Groups Created

* S3-ReadOnly-Group
* S3-FullAccess-Group
* Custom-S3-Group

## AWS Managed Policies Used

* AmazonS3ReadOnlyAccess
* AmazonS3FullAccess

## Custom IAM Policy

Policy Name:
Custom-S3-ReadOnly-NoDelete

## Custom Policy JSON

The custom IAM policy used in this project is available in the policies directory:

policies/custom-s3-readonly-nodelete.json

Purpose:

* Allow users to list S3 buckets
* Allow users to read S3 objects
* Explicitly deny deletion of S3 objects

This demonstrates fine-grained access control using custom IAM policies.

## Permission Validation

The configured permissions were tested to verify access control:

### cloud-user

* Can view S3 resources
* Cannot perform administrative actions

### s3-admin-user

* Can create, modify, and delete S3 resources
* Has full access to Amazon S3

### custom-s3-user

* Can view S3 buckets and objects
* Cannot delete S3 objects due to explicit deny rules

## Security Concepts Demonstrated

* Identity and Access Management (IAM)
* Role-Based Access Control (RBAC)
* AWS Managed Policies
* Custom Policies
* Principle of Least Privilege
* Permission Validation
* Access Governance

## Project Architecture

IAM Users
↓
IAM Groups
↓
IAM Policies
↓
Amazon S3 Resources

## Screenshots

* IAM Dashboard
* User Creation
* Group Creation
* AWS Managed Policy Assignment
* Custom Policy Creation
* ReadOnly User Permissions
* FullAccess User Permissions
* Custom Policy Configuration
* Permission Validation

## Skills Gained

* AWS IAM
* User Management
* Group Management
* Policy Management
* Access Control
* AWS Security
* Principle of Least Privilege
* Identity Management

## Outcome

Successfully implemented secure access control in AWS using IAM users, groups, managed policies, and custom policies while demonstrating the Principle of Least Privilege and role-based access management.

<img width="1357" height="384" alt="IAM_users" src="https://github.com/user-attachments/assets/5eb30185-34ac-4ee8-b863-6fba6109f3b6" />
<img width="1359" height="314" alt="iam-groups" src="https://github.com/user-attachments/assets/051b93c3-031f-4298-82b8-c2b0fc6d299e" />

