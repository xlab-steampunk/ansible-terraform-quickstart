## Prepare the environment
python3.10 -m venv .venv\
source .venv/bin/activate\
pip install -r requirements.txt\
ansible-galaxy collection install cloud.terraform

## Insert secrets
In a file secret.tfvars set appropriate values for aws access key, secret key and ssh public key.\
Ssh public key should be of type rsa and private key pair should be found on path "~/.ssh/id_rsa".

## Run example 
ansible-playbook -i inventory.yml playbook.yml
