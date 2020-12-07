# Ansible Role: ansible-apps_domain_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_domain_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_domain_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__domain_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_domain_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_domain_exporter/tags)

Deploy [domain_exporter](https://github.com/caarlos0/domain_exporter/) to expose domain metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `domain_exporter_version` | 1.8.0 | domain_exporter version |
| `domain_exporter_port` | 9116 | port to expose prometheus metrics |
| `domain_exporter_temp_dir` | /tmp | temporary directory to uncompress package |
| `domain_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `domain_exporter_force_install` | false | force install variable |

## Examples

	---
	- hosts: apps_domain_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_domain_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
