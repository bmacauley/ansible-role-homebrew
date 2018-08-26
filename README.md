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
# homebrew github repo
homebrew_repo: https://github.com/Homebrew/brew

# homebrew install path
homebrew_prefix: /usr/local
homebrew_install_path: "{{ homebrew_prefix }}/Homebrew"

# homebrew binary path
homebrew_brew_bin_path: /usr/local/bin

# homebrew packages to install
homebrew_installed_packages:
  - ssh-copy-id
  - pv

# upgrade homebrew  packages
homebrew_upgrade_all_packages: no

# homebrew taps to install
homebrew_taps:
  - homebrew/core
  - caskroom/cask

# homebrew casks to install
homebrew_cask_apps:
  - firefox

# homebrew cask install dir
homebrew_cask_appdir: /Applications

# use a brewfile to install homebrew packages and casks
homebrew_use_brewfile: true
homebrew_brewfile_dir: '~'

# remove the Hombrew cache after any new software is installed
homebrew_clear_cache: false
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
geerlingguy.homebrew


License
-------

[MIT](https://github.com/bmacauley/ansible-role-homebrew/blob/master/LICENSE)

Author 
------
Heavily influenced by geerlingguy/ansible-role-homebrew

[Brian Macauley](https://github.com/bmacauley)  
bmacauley@deloitte.co.uk

