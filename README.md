# aws-service-linked-roles

CloudFormation with custom resource to create all AWS serviced linked roles if not exist. This template can then be deployed all AWS accounts via [Customizations for AWS Control Tower Solution](https://github.com/aws-solutions/aws-control-tower-customizations)

This repository contains an AWS CloudFormation template that is used to provide a CloudFormation custom resource that creates
all service-linked roles idempotently. This means:

(1) If a role doesn't exist, create the role. If the role is successfully created, return SUCCESS otherwise return FAILED.
(2) If all roles already exist, return SUCCESS.

Check comments in source code for details

## Reference

This was inspired by these repos:

- https://github.com/jeffscottlevine/aws-idempotent-create-service-linked-role
- https://github.com/plus3it/terraform-aws-tardigrade-service-linked-roles
- https://groups.google.com/g/boto-users/c/2KEZVzxxZ2Y
