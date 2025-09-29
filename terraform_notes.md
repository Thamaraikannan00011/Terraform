# Traditional Infrastructure management approach:
1. Manual console management - web based interface, point and click, form based configuration
2. Script based automation - shell scripts with CLI commands, custom automation for repetitive task.
3. Manual monitoring and maintenance - manual health check, troubleshooting when problem arise.

## Disadvantages:

1. Error prone process.
2. Inconsistency.
3. More time required.
4. Scaling challenges(adding new resources requires repeating manual process).
5. Limited collaboration.
6. No change tracking.
7. Poor documentation(configuration exist only in peoples mind).

# **TERRAFORM:**
- Terraform is an open source Infrastructure as Code tool developed by Hashicrop.
- It allows you to define, provision(process of creating and setting up environment) and manage the cloud and on-premises infrastructure using an Hashicrop Configuration Language.

## advantages:

- Support multi cloud (AWS, Azurerm, GCP, etc,.).
- Plan before apply.
- State mangement.

## What is Infrastructure as Code?
The Process of managing and provisioning the cloud resources through the machine-readable definition files, rather than physical hardware configuration.

### Key benifits:
+ consistency - same infra every time.
+ Version control - Track changes like application code.
+ Automation - reduce manual error.
+ Scalablity - easy to replicate accross the environment.
+ Documentation - Infrastructure becomes self documenting.

## HCL(Hashicrop Configuration Language)

- A domain specific language used to define infrastructure as code, primarly tools like Terraform, OpenTofu.
- It is designed to be human-readable while enabling structured data generation.