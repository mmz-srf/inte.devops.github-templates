# DevOps
This Repo contains shared code for CI/CD


## Erstinstallation/Wartung Windows Deployment
Für das Windows deployment wird Ansible verwendet. 
Das Ansible Playbook und Inventory befindet sich im Repo [devops.windows](https://github.com/mmz-srf/inte.devops.windows). 

Damit das private Repo vom Runner ausgecheckt werden kann, müssen folgende Schritte vorgenommen werden.

* [SSH key lokal generieren](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)
* Public key als deployment key im [devops.windows](https://github.com/mmz-srf/inte.devops.windows) repo unter settings hinzufügen
* Private key als [organisations secret](https://github.com/organizations/mmz-srf/settings/secrets/actions) mit namen `INTE_DEVOPS_WINDOWS_REPO_SSH_PRIVATE_KEY` für folgende Repos freigeben
  * inte.srv.fileoperation
  * 

