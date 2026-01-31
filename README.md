# Locales Ansible Role (ansible-role-locales) from Blunix GmbH

This Ansible role installs and configures locales on Debian systems. Baseline playbooks run it across all hosts with a standard set of locales.

The Ansible Role is written and actively maintained by <a href="https://www.blunix.com" target="_blank">Blunix GmbH</a>.
It is used in the Blunix <a href="https://www.blunix.com/linux-managed-hosting.html" target="_blank">Linux Managed Hosting</a> Stack.
Its usage is documented at our <a href="https://www.blunix.com/manual" target="_blank">Linux Managed Hosting Documentation</a>.


## Features

- Installs `tzdata`, `locales` and `locales-all`.
- Ensures a list of locales are generated and available.
- Optionally removes unwanted locales.
- Exposes variables for present/absent locales and default locale environment variables.


## Requirements

- Ansible: **>= 2.20.0**
- Managed operating systems:
  - Debian **trixie**



## Role variables and example playbook

The example is split under `example/`:

- <a href="https://github.com/Blunix-GmbH/ansible-role-locales/blob/main/example/inventory/group_vars/all/locales.yml" target="_blank">`example/inventory/group_vars/all/locales.yml`</a> — locales to present/absent and default `LANG`.
- <a href="https://github.com/Blunix-GmbH/ansible-role-locales/blob/main/example/play.yml" target="_blank">`example/play.yml`</a> — baseline play applying the role.

Defaults already include `en_US.UTF-8`; group or host vars can add/remove locales or set other `LANG/LC_*` values if needed.


## Author Information

Blunix GmbH Berlin  

`root@Linux:~# Support | Consulting | Hosting | Training`

Blunix GmbH provides 24/7/365 Linux emergency support and consulting, Service Level Agreements for Debian Linux managed hosting using Ansible Configuration Management as well as Linux trainings and workshops.

Learn more at <a href="https://www.blunix.com" target="_blank">https://www.blunix.com</a>.

## Contact Information

Click here to see our <a href="https://www.blunix.com/#contact" target="_blank">Contact Information</a>.

For bug reports and feature requests, please open an issue in this repository’s GitHub issue tracker.


## License

Apache-2.0

Please refer to the `LICENSE` file in the root of this repository.

### Tests

The directory `test/` contains an example `play.yml` as well as `inventory/group_vars/`, if applicable to the role. the script `example/run-tests.sh` creates a IONOS cloud instance with terraform, uses the example inventory and playbook to run the role and then run pytest tests located in `example/tests/`. Destroy the terraform using `./run-tests.sh -d`.
