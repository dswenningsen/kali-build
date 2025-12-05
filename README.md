** Make sure to pip install ansible, apt has an older copy **

# 🚣‍♀️Flow
* Start with Kali image in Azure
* Install Ansible (python3 -m pip install ansible)
* Clone and enter the repo (git clone)
* ansible-galaxy install -r requirements.yml
* Make sure we have a sudo token (sudo whoami)
* ansible-playbook main.yml

## 👟Quick Start (Non-root with sudo no password needed)

Follow this order exactly in a fresh terminal:

1. Update and upgrade APT
	- `sudo apt update`
	- `sudo apt -y upgrade`
2. Install `pipx`
	- `sudo apt -y install pipx`
3. Install Ansible via `pipx`
	- `python3 -m pipx install ansible`
	- `sudo python3 -m pipx install ansible`
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
	- `ansible-playbook main.yml`

🗒️Notes:
- To start `kasmvncserver` from the user's home directory, run the following:
	- `./kasm.sh`
	- When asked about desktop environment select `Manually edit xstartup`. No editing will be needed.
	- Navigate to https://<kali ip>:8443
	- Ignore certificate errors if needed
	- Log in with username and the password of `password`
		- This can be changed with `kasmpasswd` command
- If running locally without SSH, no inventory file is required; the playbook defaults to localhost.
