** Make sure to pip install ansible, apt has an older copy **

# 🚣‍♀️Flow
* Start with Kali image in Azure
* Install Ansible (python3 -m pip install ansible)
* Clone and enter the repo (git clone)
* ansible-galaxy install -r requirements.yml
* Make sure we have a sudo token (sudo whoami)
* ansible-playbook main.yml

## 👟Quick Start (Non-root with sudo)

Follow this order exactly in a fresh terminal:

1. Update and upgrade APT
	- `sudo apt update`
	- `sudo apt -y upgrade`
2. Install `pipx`
	- `sudo apt -y install pipx`
3. Install Ansible via `pipx`
	- `python3 -m pipx install ansible`
4. Ensure `pipx` path is set
	- `pipx ensurepath`
    - `sudo pipx ensurepath`
5. Restart the terminal (close and reopen)
6. Install `ansible-core` with `pipx`
	- `pipx install ansible-core`
    - `sudo pipx install ansible-core`
7. Clone this repository
	- `git clone https://github.com/dswenningsen/kali-build.git`
	- `cd kali-build`
8. Install role dependencies
	- `ansible-galaxy install -r requirements.yml`
9. Run the playbook (prompts for sudo password)
	- `ansible-playbook -K main.yml`

🗒️Notes:
- `-K` asks for your sudo password to escalate tasks that use `become: true`.
- If running locally without SSH, no inventory file is required; the playbook defaults to localhost.
