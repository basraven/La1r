# La1r
A personal collection of server configs with Kubernetes and Ansible, enjoy!


## Prerequisites
* Docker
* id_rsa and id_rsa.pub in ```/credentials/ssh/``` (generate these yourself)

## How to run
Run the control (Ansible) client with:
```powershell
./control/control.ps1
```

## Ansible configuration
The Ansible configuration can be found at ```/playbooks/Makefile``` which you should run in the Ansible control container by:
```bash
cd /playbook
make all
```
## Kubernetes configuration
The Kubernetes configuration can be found at ```/kubernetes/Makefile``` which you should run in the Ansible control container by:
```bash
cd /kubernetes
make all
```

## Components
* [/ansible-control](/ansible-control): The control host for Ansible in a Docker container
* [/playbooks](/playbooks): The playbooks collection to manage servers
* [/credentials](/credentials): Place your credentials here (and ```.gitignore``` them)

## Roadmap
Find the project roadmap on [ROADMAP.md](ROADMAP.md)

### [Optional] Running on Windows with Powershell
Sometimes Powershell gives the error "run.ps1 is not digitally signed. You cannot run this script on the current system."
Please use the following command in a Powershell window as Administrator to (permanently solve this)
```powershell
Set-ExecutionPolicy unrestricted
```