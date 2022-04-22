# hello-packer

Tutorial based on https://learn.hashicorp.com/collections/packer/aws-get-started 

Getting Started with AWS

HashiCorp Packer automates the creation of any type of machine image, including AWS AMIs. You'll build an Ubuntu machine image on AWS in this tutorial.

## Prerequisites

Authenticate to AWS: provide AWS credentials to Packer

$ export AWS_ACCESS_KEY_ID="<YOUR_AWS_ACCESS_KEY_ID>"
$ export AWS_SECRET_ACCESS_KEY="<YOUR_AWS_SECRET_ACCESS_KEY>"

## deployment

Initialize your Packer configuration.
$ packer init .

Format and validate your Packer template
$ packer fmt .


Validate your template.
$ packer validate .

Build Packer image (with variable from the file example.auto.pkrvars.hcl)
$ packer build .

Build Packer image with name from command line flag
$ packer build --var ami_prefix=learn-packer-aws-redis-var-flag .