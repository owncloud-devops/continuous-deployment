# Continuous Deployment

## Usage

This continuous deployment playbook assumes:
- you are using Hetzner Cloud for your servers
- you are using Cloudflare for your DNS records
- your deployments are defined with docker-compose

### Install requirements

1. run `pip install -r py-requirements.txt`
1. run `ansible-galaxy role install -r requirements.yml --upgrade`
1. run `ansible-galaxy collection install -r requirements.yml --upgrade`

### run all (create hcloud server, add cloudflare DNS record, configure ubuntu, deploy docker-compose project)

1. add your server and docker-compose projects to `servers.yml`
1. run `export HCLOUD_API_TOKEN=...` with a valid Hetzner cloud api token
1. run `export CLOUDFLARE_API_TOKEN=...` with a valid Cloudflare api token
1. run `ansible-playbook playbook-all.yml`
