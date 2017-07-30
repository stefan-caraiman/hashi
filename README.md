# Hashicorp suite

1. What is Terraform?

- build change and version infrastracture through code, Infrastracture as Code
- already manages many popular service providers(AWS, Docker etc.)
- generates a plan based on the file description
- executes it to build the described infrastructure, HCL DSL files/blueprints
- can manage: instances, storage, networking, DNS, etc.

## N-th tier application example setup:

Dependencies between web servers and database, thus Terraform will ensure the database tier is available before web servers and that the Load balancers are aware of the newly created web nodes.

## Installation

Visit https://www.terraform.io/downloads.html
Download package through browser or wget/curl
Unzip it
Move it or symlink it to binaries


# Arhitectural notes:

- define inputs variables in vars.tf
- keep it DRY(Don't Repeat Yourself), use modules
- in our case it would be best to simply save .tfstate files, since we are using the opensource version of Terraform, in order to avoid deleting instances or removing changes of other commiters
- regarding the note above, everyone should pull latest changes when working with the Terraform repo and take precautions with the changes

