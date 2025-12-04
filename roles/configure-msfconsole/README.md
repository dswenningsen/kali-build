# configure-msfconsole

Configures Metasploit by initializing the local database via `msfdb init`.

## What it does
- Checks for `~/.msf4/database.yml` to determine if Metasploit DB is already configured.
- Runs `msfdb init` if not initialized.

## Tags
- `msf`