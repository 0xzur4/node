# Nesa Node
-----

## Dokumentasi
- https://docs.nesa.ai/nesa


## Prerequisites

#### System Requirements

- CPU: Multi-core processor
- Memory: 4 GB RAM minimum
- Storage: 50 GB free disk space (or more depending on the size of the model(s) you'd like to power)
- Network: Stable internet connection

#### Software Requirements
- [Docker](https://docs.docker.com/engine/install/ubuntu/) - install docker
- [Curl](https://curl.se/docs/install.html) - install curl
- jq: 
```
sudo apt update
sudo apt install jq -y
```
- gum:
```
# Download 
wget https://github.com/charmbracelet/gum/releases/download/v0.10.0/gum_0.10.0_Linux_x86_64.tar.gz

# Ekstrak 
tar -xvzf gum_0.10.0_Linux_x86_64.tar.gz

# Move binari gum ke folder /usr/local/bin
sudo mv gum /usr/local/bin/

sudo chmod +x /usr/local/bin/gum
```
- Hugging Face API Token - [HuggingFace](https://huggingface.co/settings/tokens)
## Installation
```
# For all operating systems
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)
```
#### Check status node
- get id: 
```
cat ~/.nesa/identity/node_id.id
```
- check status node in https://node.nesa.ai/
