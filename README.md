# ansible_elasticsearch
Ansible to Install [Elasticsearch](https://www.elastic.co/elasticsearch) on Ubuntu

## Requirements

* Tailscale installed and configured for ssh
    ```bash
    sudo adduser --disabled-password --comment "" ansible
    sudo echo 'ansible    ALL=(ALL:ALL) NOPASSWD: ALL' > /etc/sudoers.d/ansible
    sudo apt install curl
    curl -fsSL https://pkgs.tailscale.com/stable/ubuntu/$(lsb_release -cs).noarmor.gpg | sudo tee /usr/share/keyrings/tailscale-archive-keyring.gpg >/dev/null
    curl -fsSL https://pkgs.tailscale.com/stable/ubuntu/$(lsb_release -cs).tailscale-keyring.list | sudo tee /etc/apt/sources.list.d/tailscale.list
    sudo apt update
    sudo apt install tailscale
    sudo tailscale up --ssh --advertise-tags "tag:servers,tag:elasticsearch"
    ```