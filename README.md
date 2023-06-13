Ansible Role: pwch
==================

An ansible role that installs [pwch](https://github.com/nonce9/pwch) on Linux.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below.

Variables                 | Default
--------------------------|---
`pwch_version:`           | pwch version to install; e.g. `1.1.1`
`pwch_base_url:`          | pwch download URL; should not be changed
`pwch_domain:`            | your mailserver's fqdn; default: `example.org`
`pwch_url_prefix:`        | URL prefix to append to all http server responses; default: `/selfservice`; can be emtpy as well
`pwch_assets_path:`       | absolute path where html/css assets will be stored; default: `/usr/local/src/pwch`
`pwch_listen_address:`    | `127.0.0.1`
`pwch_listen_port:`       | `8080`
`pwch_db_host:`           | `/run/postgresql`
`pwch_db_name:`           | `mail`
`pwch_db_user:`           | `mail`
`pwch_db_password:`       | `secretPassword`
`pwch_ssl_mode:`          | `disable`
`pwch_bcrypt_cost:`       | `14`
`pwch_smtp_host:`         | `example.org`
`pwch_smtp_port:`         | `587`
`pwch_smtp_user:`         | `noreply@example.org`
`pwch_smtp_password:`     | `secretPassword`
`pwch_smtp_sender:`       | `"PWCH <noreply@example.org>"`
`pwch_pw_policy_min:`     | `12`
`pwch_pw_policy_max:`     | `128`
`pwch_pw_policy_lower:`   | `true`
`pwch_pw_policy_upper:`   | `true`
`pwch_pw_policy_digits:`  | `true`
`pwch_pw_policy_special:` | `true`
`pwch_otl_valid_for:`     | how long password change request links are valid; default: `10m`
`pwch_apparmor_enabled:`  | whether or not AppArmor profiles should be loaded; default: `false`

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - nonce9.pwch

License
-------

AGPL-3.0

Author Information
------------------

This role was created by nonce9
