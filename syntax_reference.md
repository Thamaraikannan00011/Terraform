# HCL (HashiCorp Configuration Language)
## Syntax Reference
## 1. Basic Structure and Comments
- Comments

```
    # single-line comment
    // Another single-line comment style

    /*
    Multi-line comment
    Can span multiple lines
    */
```

- File Structure
```
    # configuration block that contains settings about Terraform itself
    
    terraform {

        # Specifies which versions of Terraform CLI can run this configuration
        required_version = ">= 1.0"
    }

    /*
    * PROVIDER BLOCK - The Bridge Between Terraform and Cloud Services
    * The provider block tells Terraform HOW and WHERE to create resources.
    * Think of it as a "plugin" that knows how to talk to a specific service (AWS, Azure, GCP, etc.)
    */

    provider "aws" {
      region = "us-west-2"
    }

    resource "aws_instance" "example" {
      ami           = "ami-12345678"
      instance_type = "t2.micro"
    }
```