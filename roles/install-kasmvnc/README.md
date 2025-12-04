Install KasmVNC Server

This role downloads and installs the latest KasmVNC server `.deb` for Debian bookworm on `amd64`.

Variables:
- `kasmvnc_download_dir`: Where to store the downloaded package (default `/tmp`).

Usage:
Add the role to your play:

```
- hosts: localhost
  become: true
  roles:
    - install-kasmvnc
```
