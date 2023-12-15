# DevOps
This Repo contains shared code for CI/CD

### Ansible

Falls der INTE Service User ein neues Passwort bekommt, muss im Inventory das Passwort angepasst werden. Dafür muss das neue Passwort zuerst mit dem Ansible-Vault verschlüsselt werden. Das Vault Passwort muss auf das Ansible Vault Passwort in Minidock gesetzt werden, damit der Github-Runner weiterhin das verschlüsselte Passwort des INTE-Service User während dem Ausführen des Playbook entschlüsseln kann.
> ansible-vault encrypt_string '<pw-value>' --name '<pw-key>'
