ansible timedatectl
===================
[![Build Status](https://travis-ci.org/ypsman/ansible-timedatectl.svg?branch=master)](https://travis-ci.org/ypsman/ansible-timedatectl)

Setting up Systemd timedatectl NTP config.
Tested on Ubuntu 16.04/18.04, Debian 8/9 and Centos7.
Role is skipped if systemd is not used on the Systen.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: ypsman.timedatectl
          timedatectl_timeservers:
            - 0.debian.pool.ntp.org
            - 1.debian.pool.ntp.org
          timedatectl_timeservers_fallback:
            - 2.debian.pool.ntp.org
            - 3.debian.pool.ntp.org
          timedatectl_timezone: Europe/Berlin
