# premier-terraform

Infrastructure AWS décrite en code avec Terraform : un serveur EC2 qui lance automatiquement une application Docker.

## Ce que ça crée

- un groupe de sécurité (pare-feu) qui ouvre uniquement le port 8000
- un serveur EC2 (t3.micro, Amazon Linux 2023, région eu-north-1)
- au démarrage, le serveur installe Docker et lance l'image de l'application

## Utilisation

terraform init
terraform plan
terraform apply
terraform destroy

## Attention

Un serveur oublié coûte de l'argent : toujours lancer `terraform destroy` après un test.
Le fichier `terraform.tfstate` n'est jamais publié (voir `.gitignore`).
