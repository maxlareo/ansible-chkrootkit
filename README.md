chkrootkit
==========

[![Build Status](https://travis-ci.org/maxlareo/ansible-chkrootkit.svg?branch=master)](https://travis-ci.org/maxlareo/ansible-chkrootkit) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-chkrootkit-blue.svg)](https://galaxy.ansible.com/maxlareo/chkrootkit/)

Install and configure Chkrootkit

## Role Variables

### About the `/etc/chkrootkit.conf` file

- `chkrootkit_run_daily`: [default: `'false'`]: Set this to yes to enable chkrootkit daily runs
- `chkrootkit_run_daily_opts`: [default: `'-q'`]: Set the list of options to use with chkrootkit, see man chkrootkit
- `chkrootkit_diff_mode`: [default: `'false'`]: If this is set to "true" chrootkit compares the files /var/log/chkrootkit/log.expected with /var/log/chkrootkit/log.today

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: all
  roles:
    - chkrootkit
```

## License

MIT
