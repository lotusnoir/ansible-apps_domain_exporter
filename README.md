# Ansible Role: ansible-apps_domain_exporter

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_domain_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_domain_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_domain_exporter.svg)](https://github.com/lotusnoir/ansible-apps_domain_exporter/releases/latest)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_domain_exporter?color=orange&style=flat)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_domain_exporter)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)


Deploy [domain_exporter](https://github.com/caarlos0/domain_exporter/) to expose domain metrics to prometheus.

## Role variables

| Name                            | Default Value  | Description                        |
| ------------------------------- | -------------- | -----------------------------------|
| `domain_exporter_version`       | 1.14.0         | domain_exporter version |
| `domain_exporter_port`          | 9116           | port to expose prometheus metrics |
| `domain_exporter_temp_dir`      | /tmp           | temporary directory to uncompress package |
| `domain_exporter_install_dir`   | /usr/local/bin | directory to install binary |
| `domain_exporter_force_install` | false          | force install variable |

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

## Prometheus rules

TODO

## Grafana Dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13924](https://grafana.com/grafana/dashboards/13924)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
