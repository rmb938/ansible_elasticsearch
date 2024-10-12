# ansible_elasticsearch
Ansible to Install [Elasticsearch](https://www.elastic.co/elasticsearch) on Ubuntu

## Requirements

* Tailscale installed and configured for ssh
    ```bash
    sudo tailscale up --ssh --advertise-tags "tag:servers,tag:elasticsearch"
    ```