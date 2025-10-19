# Firefox-user-config-Role

[![Alma9-CI](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/alma9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/alma9-ci-caller.yml)  [![Rocky9-CI](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/rocky9-ci-caller.yml)  [![CentOSStream9-CI](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/centosstream9-ci-caller.yml)  [![Debian12-CI](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/debian12-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/debian12-ci-caller.yml)  [![Ubuntu2204-CI](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/ubuntu2204-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox-user-config/actions/workflows/ubuntu2204-ci-caller.yml)

Role description

This role includes a vagrant based molecule testing setup as a submodule at `molecule`

## Structure

```code
📦 ansible-firefox-user-config
 ┣ 📂defaults
 ┃ ┗ 📜main.yml
 ┣ 📂meta
 ┃ ┗ 📜main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂tasks
 ┃ ┣ 📜absent.yml
 ┃ ┣ 📜extensions.yml
 ┃ ┣ 📜main.yml
 ┃ ┣ 📜present.yml
 ┃ ┣ 📜profile.yml
 ┃ ┗ 📜tests.yml
 ┣ 📂templates
 ┃ ┣ 📜installs.ini.j2
 ┃ ┣ 📜profiles.ini.j2
 ┃ ┗ 📜user.js.j2
 ┣ 📜.gitignore
 ┣ 📜.gitmodules
 ┣ 📜README.md
 ┗ 📜requirements.yml

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * `state` - Set to '*present*' since this role got no '*absent*' implementation
  * `firefox_source` - Install source (*default*, *esr* or *flatpak*), default is '*default*'
  * `firefox_flatpak_extensions` - Install flatpak based firefox extensions
  * `user` - Username to apply this config to

## Dependencies

List role ansible-galaxy dependencies

* [philnewm.firefox](https://galaxy.ansible.com/ui/standalone/roles/philnewm/firefox/)

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-firefox-user-config present
    ansible.builtin.include_role:
      name: ansible-firefox-user-config
    vars:
      state: present
      firefox_source: default
      firefox_flatpak_extensions: true
      user: "test_user"

...
```

## License

Add license - if any.
