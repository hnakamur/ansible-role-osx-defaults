osx-defaults
============

An Ansible role to set the OS X user defaults

Requirements
------------

None.

Role Variables
--------------

## values to set for Finder

osx_defaults_finder_values:
  - { domain: com.apple.finder, key: AppleShowAllFiles, type: boolean, value: true, state: present }
  - { domain: com.apple.desktopservices, key: DSDontWriteNetworkStores, type: string, value: true, state: present }

## values to set for SystemUIServer

osx_defaults_system_ui_server_values:
  - { domain: com.apple.screencapture, key: disable-shadow, type: boolean, value: true, state: present }

Dependencies
------------

None.


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: hnakamur.osx-defaults }

License
-------

MIT

Author Information
------------------

[Hiroaki Nakamura]( http://hnakamur.github.io/ )
