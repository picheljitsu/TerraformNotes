# TerraformNotes
Terraform brain dump


# Check if element in a map exists

Can't do boolean type so use ternary between 1 : 0

    kms_enabled = length([for k,v in local.server-configs: 
                          k if v.encrypted == true]) > 0 ? 1 : 0
                          
