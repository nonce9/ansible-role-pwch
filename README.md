Ansible Role: pwch
==================

An ansible role that installs [pwch](https://github.com/nonce9/pwch) on Linux.

Requirements
------------

None

Role Variables
--------------

Available variables are listed below.

`pwch_version:`           pwch version to install; e.g. `1.1.1`

`pwch_base_url:`          pwch download URL; should not be changed

`pwch_domain:`            your mailserver's fqdn; default: `example.org`

`pwch_url_prefix:`        URL prefix to append to all http server responses; default: `/selfservice`; can be emtpy as well

`pwch_assets_path:`       absolute path where html/css assets will be stored; default: `/usr/local/src/pwch`

`pwch_listen_address:`    default: `127.0.0.1`
`pwch_listen_port:`       default: `8080`

`pwch_db_host:`           default: `/run/postgresql`
`pwch_db_name:`           default: `mail`
`pwch_db_user:`           default: `mail`
`pwch_db_password:`       default: `secretPassword`
`pwch_ssl_mode:`          default: `disable`

`pwch_bcrypt_cost:`       default: `14`

`pwch_smtp_host:`         default: `example.org`
`pwch_smtp_port:`         default: `587`
`pwch_smtp_user:`         default: `noreply@example.org`
`pwch_smtp_password:`     default: `secretPassword`
`pwch_smtp_sender:`       default: `"PWCH <noreply@example.org>"`

`pwch_pw_policy_min:`     default: `12`
`pwch_pw_policy_max:`     default: `128`
`pwch_pw_policy_lower:`   default: `true`
`pwch_pw_policy_upper:`   default: `true`
`pwch_pw_policy_digits:`  default: `true`
`pwch_pw_policy_special:` default: `true`

`pwch_otl_valid_for:`     how long password change request links are valid; default: `10m`

`pwch_apparmor_enabled:`  whether or not AppArmor profiles should be loaded; default: `false`

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
