# ionoscloud-terraform-snippets
Here you'll find various Terraform examples for the IONOS cloud (https://cloud.ionos.de/compute).
The official IONOS cloud Terraform plugin is located at https://github.com/ionos-cloud/terraform-provider-ionoscloud

## Disclaimer
This is not an official IONOS cloud repository.

The examples are provided _as is_ without any warranty to run on any combination of IONOS Cloud API, GO SDK, Terraform Plugin, Terrafom version, language, climate, life, universe and everything.

An at least basic knowledge of IONOS cloud's solution and Terraform is expecteded.

## Overview

All examples are expecting the API credentials as environment variables, i.e.
```
$ export IONOS_USERNAME="ionoscloud_username"
$ export IONOS_PASSWORD="ionoscloud_password"
```
Alternativaly you can add an additional `.tf` file with these credentials.

All examples are organized in directories where each of them should have a (minimal )README. 

I, personally, tend to split the Terraform configuration into separate files and to provide some kind of structure by using a prefix. e.g. like
```
00_ionoscloud-provider.tf
00_ssh-default-key.rsa
00_ssh.tf
01_demo-tenant.auto.tfvars
01_demo-tenant-vars.tf
10_demo-pcc.tf
11_demo-tenant-vdc.tf
20_demo-main-connect.tf
```

This should
* give a rough overview on the dependencies for different tasks
* allow to disable some tasks by simply renaming the files (e.g. to xyz.tf.disabled)

But don't expect consistency :-/

Please note, that the graphical representation in the DCD will initially be - well - strange. The API does not know about the GUI and the placement of resource icons and you have to rearrange this manually in DCD (this will change nothing for Terraform). It may even occur that some resource icons are stacked at the same position.
