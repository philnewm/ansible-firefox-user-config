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
 ┃ ┣ 📜favorite.yml
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
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies

* philnewm.firefox

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
      firefox_gnome_favorite: true
      user: "{{ username }}"

...
```

## License

Add license - if any.

## Notes

Includes special git configuration for submodule files that are most likely to get local overrides
`.git/info/attributes`

```code
molecule/default/cleanup.yml merge=ours
molecule/default/converge.yml merge=ours
molecule/default/verify.yml merge=ours
```

## Changes to role template

* Add github action that flags empty directories on release creation
