Ansible playbook for deploying the server `dev.fxe-gear.com`.

Installed software
---

- common tools: VIM, htop, unzip, ...
- build-essential
- Python 3 (+ venv, pip, requests)
- Supervisor
- GIT
- Apache 2
- PHP 7.0 (with Apache FPM bridge)
- MySQL (MariaDB)
- Certbot (with certificate autorenew)
- [Adminer](https://www.adminer.org/) ([here](https://dev.fxe-gear.com/adminer))
- [Gogs](https://gogs.io/) ([here](https://dev.fxe-gear.com/git))

Deploying
---

Prerequisities:

- Ansible >= 2.2
- cloned repository
- certificate-based SSH access as `deploy` user with passwordless `sudo` ability
- MySQL root password stored as plain-text in `credentials/mysql_root`
- requirements installed: `ansible-galaxy install -r requirements.yml`

Deploying:

`ansible-playbook main.yml`
