ansible-role-homebrew
=====================

Ansible role to install Homebrew on a Mac and to configure packages, taps, and cask apps with supplied variables

![Build status](https://travis-ci.org/bmacauley/ansible-role-homebrew.svg?branch=master)


Requirements
------------
None

Role Variables
--------------
default values (see defaults/main.yml):

```
homebrew_repo: https://github.com/Homebrew/brew             # homebrew github repo

homebrew_prefix: /usr/local
homebrew_install_path: "{{ homebrew_prefix }}/Homebrew"
homebrew_brew_bin_path: /usr/local/bin

homebrew_installed_packages:                                # homebrew packages
  - ssh-copy-id
  - pv

homebrew_upgrade_all_packages: no                           # upgrade homebrew packages

homebrew_taps:                                              # homebrew taps
  - homebrew/core
  - caskroom/cask

homebrew_cask_apps:                                         # homebrew casks
  - firefox

homebrew_cask_appdir: /Applications                         #homebrew cask install dir

homebrew_use_brewfile: true                                 # use a brewfile to install homebrew packages and casks
homebrew_brewfile_dir: '~'
```




Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - { role: ansible-role-homebrew }

Dependencies
------------

elliotweiser.osx-command-line-tools


License
-------

[MIT](https://github.com/bmacauley/ansible-role-homebrew/blob/master/LICENSE)

Author 
------
Heavily influenced by geerlingguy/ansible-role-homebrew

[Brian Macauley](https://github.com/bmacauley)  
bmacauley@deloitte.co.uk

