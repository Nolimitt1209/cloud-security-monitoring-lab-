Cloud Security Monitoring & Detection Lab

Overview

This project demonstrates a hands-on Google Cloud security monitoring workflow using Cloud Audit Logs and Logs Explorer.

The lab focuses on reviewing administrative activity, identifying security-relevant events, and documenting audit evidence that could be used during a cloud security investigation.

Objectives

Review Google Cloud Audit Logs
Investigate administrative activity
Identify security-relevant events
Analyze service and resource activity
Capture audit-log evidence
Apply security monitoring and investigation concepts
Document findings in a recruiter-friendly format
Environment

Cloud Platform: Google Cloud Platform (GCP)
Project: Cloud-Security-Monitoring-Lab
Monitoring Tool: Cloud Logging / Logs Explorer
Logging Source: Cloud Audit Logs
Investigations

1. Project Creation Activity

Event: CreateProject

Service: cloudresourcemanager.googleapis.com

Analysis:
The audit log records the creation of a Google Cloud project. Project creation is an important administrative event because new projects establish separate cloud environments and can introduce new resources, identities, APIs, and security configurations.

Security relevance:
Monitoring project creation can help security teams identify unauthorized or unexpected changes to the cloud environment.

Evidence:
01-project-creation-audit-log.jpg



2. Service/API Enablement

Event: ServiceUsage.EnableService

Analysis:
The audit log records the enabling of a Google Cloud service/API. Enabling additional services can expand the capabilities available within a project and may increase the project's attack surface.

Security relevance:
Security teams can monitor service enablement to identify unexpected changes and verify that newly enabled services are authorized and necessary.

Evidence:
02-service-enabled-audit-log.jpg



3. Service Account Creation

Event: google.iam.admin.v1.CreateServiceAccount

Analysis:
A test service account was created to generate and investigate an IAM-related audit event.

Security relevance:
Service-account creation is security-sensitive because service accounts can be used by applications and automated processes to access cloud resources. Monitoring their creation helps organizations identify unauthorized identities and maintain appropriate access controls.

Evidence:
03-service-account-creation-audit-log.jpg

Security Findings

Finding

Risk Consideration

Recommended Control

Project creation activity

Unauthorized projects can introduce unmanaged cloud resources

Monitor and review project creation events

Service/API enablement

Unnecessary services can expand the attack surface

Review newly enabled services and restrict unnecessary APIs

Service account creation

Unauthorized service accounts can create persistent identities

Monitor service-account creation and apply least privilege

Key Takeaways

This lab demonstrates how cloud security analysts can use audit logs to:

Establish visibility into administrative activity
Investigate changes within a cloud environment
Identify security-relevant events
Review identity-related activity
Document evidence for security investigations
Skills Demonstrated

Google Cloud Platform (GCP)
Cloud Security
Cloud Logging
Cloud Audit Logs
Identity and Access Management (IAM)
Security Monitoring
Threat Detection
Security Investigation
Access Control
Risk Analysis
Evidence

Screenshots documenting the investigations are located in the screenshots/ directory.

Future Improvements

Potential extensions to this lab include:

Creating additional controlled IAM events
Developing log-based security alerts
Building detection queries for suspicious activity
Monitoring service-account key activity
Integrating Security Command Center
Developing an incident-response workflow
