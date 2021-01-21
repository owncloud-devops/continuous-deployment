# Server Provisioning

## Usage

### Install requirements

1. run `pip install -r py-requirements.txt`
1. run `ansible-galaxy role install -r requirements.yml`
1. run `ansible-galaxy collection install -r requirements.yml`

### run `docker-ubuntu-docker` role on existing host

1. add your server to the inventory file `inventory-base-ubuntu-docker.yml`
1. run `ansible-playbook -i inventory-base-ubuntu-docker.yml playbook-base-ubuntu-docker.yml`

### run all (create hcloud server, configure ubuntu, deploy docker-compose project)

1. add your server and docker-compose projects to `servers.json`
1. run `export HCLOUD_API_TOKEN=...` with a valid Hetzner cloud api token
1. run `ansible-playbook playbook-all.yml`
