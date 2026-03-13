# Linux

Initial Linux hardening helper:

```bash
bash Invoke-Harden.sh
```

To also remediate unsafe `NOPASSWD` rules interactively:

```bash
sudo bash Invoke-Harden.sh --remediate
```

Current behavior:
- Checks whether the current user can run `sudo` without a password.
- Scans readable `sudoers` files for `NOPASSWD` entries.
- Can comment out detected `NOPASSWD` entries after prompting, with backup creation and `visudo` validation.
