
## Table of Content
- [Traditional approach](#Traditional-Infrastructure-management-approach)
    - [Disadvantages](#Disadvantages)
- [Terraform](#TERRAFORM)
    - [advantages](#advantages)
- [IaC](#what-is-infrastructure-as-code)
    - [Key benifits](#key-benifits)
- [HCL](#hclhashicrop-configuration-language)
- [Terraform workflow](#terraform-workflow)
- [Terraform architecture](#how-terraform-works)
- [API](#apiapplication-programming-interface)

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
- It allows you to define, provision(process of creating and setting up environment) and manage the cloud and on-premises infrastructure using an Configuration Language.

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

## Terraform Workflow:

1. Init:
    + to prepare the current working directory for use with Terraform.
    + download providers and initialize backend.
2. Validate:
    + Validate the syntax and configuration of Terraform files.
3. Plan:
    + Create an execution plan showing what Terraform will do.
    + Shows what resources will be created, modified, or destroyed.
    + Builds dependency graph to determine execution order.
    ### output symbols
    * "+" = Resource will be created.
    * "~" = Resource will be modified.
    * "-" = Resource will be destroyed
4. Apply:
    + Apply the changes required to reach the desired state.
    + Updates the state file with current infrastructure state.
5. Destroy:
    + Destroy all resources managed by Terraform.
    + Removes resources in reverse dependency order.
    + Updates state file to reflect destroyed resources

## How terraform works?

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/0*bJzMGdZBo0zKfbvQ" 
       alt="Terraform Architecture" 
       style="width:500px; height:auto;" />
</p>

1. Terraform configuration file:
    + Terraform configuration file contains definiton of Infrastructure as Code resources that terraform will manage.
    + This file is written in HCL which is designed to be human-readable and easy to write.
    + It uses ***.tf*** file extension.

2. Terraform Core:
    + Terraform core is statically compiled binary written in "GO" language.
    + It uses RPC(Remote Procedure calls) to communicate with terraform plugins.
    + The compiled binary is a command line tool called ***terraform***.

3. Terraform State file:
    + State file are crucial for terraform operations and track the current state of your infrastructure.
    + Maintains records of what terraform created and manages.
    + contains sensitive data, requiring careful security considerations.

4. Terraform Providers:
    + Terraform providers are plugins that enables terraform to interact with the cloud platform through the APIs.
    + Plugins authentication with infrastructure provider.
    + defines managed resources and data sources that map to specific services.

## API(Application Programming Interface):

+ API is a set of rules and protocols that allows different software to communicate with each other.
+ It defines how requests and responses should be structured between systems, acting ike intermediatory that enables different programs to interact and exchange data.