# Ansible Role: Elasticsearch

[![Build Status](https://travis-ci.org/picturemaxx/ansible-elasticsearch.svg?branch=master)](https://travis-ci.org/picturemaxx/ansible-elasticsearch)

An Ansible Role that installs Elasticsearch on RedHat/CentOS or Debian/Ubuntu.

## Requirements


Requires Java 8. See [`ansible-java`](https:////github.com/picturemaxx/ansible-java.git).


## Role Variables
Available variables are listed below, along with default values (see `defaults/main.yml`):

    elasticsearch_network_host: localhost

Network host to listen for incoming connections on. By default we only listen on the localhost interface. Change this to the IP address to listen on a specific interface, or `0.0.0.0` to listen on all interfaces.

    elasticsearch_http_port: 9200

The port to listen for HTTP connections on.

    elasticsearch_script_inline: true
    elasticsearch_script_indexed: true

Whether to allow inline scripting against ElasticSearch. You should read the following link as there are possible security implications for enabling these options: [Enable Dynamic Scripting](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-scripting.html#enable-dynamic-scripting). Available options include: `true`, `false`, and `sandbox`.

## Dependencies


  - https://github.com/picturemaxx/ansible-java.git


## Example Playbook

    - hosts: search
      roles:
        - ansible-java
        - ansible-elasticsearch

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).

Tobias Kramheller @tkramheller
