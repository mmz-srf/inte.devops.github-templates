# DevOps
This Repo contains shared code for CI/CD

## Erstinstallation/Wartung Windows Deployment
Für das Windows Deployment wird Ansible verwendet. Das Ansible Playbook und Inventory befindet sich im
Repo [inte.infra.ansible](https://github.com/mmz-srf/inte.infra.ansible).

Damit das private Repo vom Runner ausgecheckt werden kann, müssen folgende Schritte vorgenommen werden.

* [SSH Key lokal generieren](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)
* Public Key als Deployment Key im [inte.infra.ansible](https://github.com/mmz-srf/inte.infra.ansible) Repo unter
  settings hinzufügen
* Private Key als [organisations secret](https://github.com/organizations/mmz-srf/settings/secrets/actions) mit
  namen `INTE_DEVOPS_WINDOWS_REPO_SSH_PRIVATE_KEY` für folgende Repos freigeben
    * inte.srv.fileoperation
    * inte.srv.watermarksacn
    * inte.srv.watchservice
