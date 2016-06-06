# Ansible Role: Elasticsearch


[![Build Status](https://travis-ci.org/devops/ansible-role-elasticsearch.svg?branch=master)](https://travis-ci.org/devops/ansible-role-elasticsearch)

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

* `elasticsearch_packages:`
    ```
      - elasticsearch
      - java     
    ```

    Supported formats
    ```
      - elasticsearch
      - https://repos.influxdata.com/centos/7/x86_64/stable/elasticsearch-0.13.0.x86_64.rpm
      - /tmp/elasticsearch-0.13.0.x86_64.rpm
    ```
* `elasticsearch_repo: True`
* `elasticsearch_repo_baseurl: 'https://packages.elastic.co'`
* `elasticsearch_cluster_name: 'elastic'`
* `elasticsearch_node_name: '{{ ansible_hostname }}'`
* `elasticsearch_node_rack: 'r1'`
* `elasticsearch_path_data: '{{ elasticsearch_base_dir/data }}'`
* `elasticsearch_path_logs: '{{ elasticsearch_base_dir/logs }}'`
* `elasticsearch_network_host: '127.0.0.1'`
* `elasticsearch_http_port: 9200`
* `elasticsearch_cluster: False`
* `elasticsearch_zen_minimum_master_nodes: 3`
* `elasticsearch_zen_ping_unicast_hosts: []`

## Dependencies

None.

## Example Playbook

`see tests/test.yml`

## License

MIT / BSD

## Author Information

z.
