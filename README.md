# terraform
Learnings of terraform tool

# terraform install

Manual Installation: Install from https://www.terraform.io/downloads.html
For windows: choco install terraform
For Mac: 
  >  brew tap hashicorp/tap
  >  brew install hashicorp/tap/terraform

# terraform commands

init -- Prepare the working directory. It installs the required providers modules
plan -- shows the action plan what will be the resource created
apply -- create or update the infrastructure
destroy -- deletes previously created infrastructure
validate -- check whether the configfile is valid
    > PS C:\Users\212801747\hashicorp-terraform> terraform validate                                                                                                                                Success! The configuration is valid.

    > PS C:\Users\212801747\hashicorp-terraform> terraform validate                                                                                                                                ╷
│ Error: Invalid required_providers object
│
│   on main.tf line 4, in terraform:
│    4:       source1  = "hashicorp/aws"
│
│ required_providers objects can only contain "version", "source" and "configuration_aliases" attributes. To configure a provider, use a "provider" block.

# Define Input Variables
Specify variables.tf file and modify the main.tf file with var.<variable_name>. To override default value provide while applying the changes
   > terraform apply -var "<variable_name>=<value>"
  
# Query Data with outputs
  
  Create outputs.tf and do a terraform apply 
   > terraform output will show all the outputs
   > terraform output <key> --> queries the specific output

