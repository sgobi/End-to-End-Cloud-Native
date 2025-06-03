infra-aws-terraform/
├── .gitignore
├── environments/
│   └── dev/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
└── modules/
    ├── vpc/
    │   ├── main.tf
    │   ├── variables.tf
    │   └── outputs.tf
    └── eks/
        ├── main.tf
        ├── variables.tf
        └── outputs.tf


# Shell Commands to Run

mkdir -p infra-aws-terraform/environments/dev
mkdir -p infra-aws-terraform/modules/vpc
mkdir -p infra-aws-terraform/modules/eks

# Create Terraform files in environments/dev
touch infra-aws-terraform/environments/dev/main.tf
touch infra-aws-terraform/environments/dev/variables.tf
touch infra-aws-terraform/environments/dev/outputs.tf

# Create Terraform files in modules/vpc
touch infra-aws-terraform/modules/vpc/main.tf
touch infra-aws-terraform/modules/vpc/variables.tf
touch infra-aws-terraform/modules/vpc/outputs.tf

# Create Terraform files in modules/eks
touch infra-aws-terraform/modules/eks/main.tf
touch infra-aws-terraform/modules/eks/variables.tf
touch infra-aws-terraform/modules/eks/outputs.tf

# Create .gitignore with recommended Terraform ignores
cat <<EOF > infra-aws-terraform/.gitignore
**/.terraform/
*.tfplan
*.tfstate
*.tfstate.backup
crash.log
override.tf
override.tf.json
*_override.tf
*_override.tf.json
.terraform.lock.hcl
terraform.tfvars
terraform.tfvars.json
*.swp
*.swo
*.DS_Store
.idea/
.vscode/
EOF