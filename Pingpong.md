# Running Pingpong

### Hardware Requirement
- Ubuntu 22.04 or above / Debian
- 8GB Memory
- 100GB Disk
- 4-core processor and better

### Software Requirement
- Docker:
> Run the following command to uninstall all conflicting packages:
```bash
for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done
```
> Set up Docker's apt repository
```bash
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```
> Install the Docker packages
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
### Installing 
> Download app:
```bash
wget https://pingpong-build.s3.ap-southeast-1.amazonaws.com/linux/latest/PINGPONG
chmod +x PINGPONG
```
> Running App:
```bash
./PINGPONG --key=<Device_Key>
```

### Configuration
- 0G
```bash
./PINGPONG config set --0g=<Private_Key>
./PINGPONG stop --depins=0g
./PINGPONG start --depins=0g
```
- Grass
```bash
./PINGPONG config set --grass.access=<accessToken> --grass.refresh=<refreshToken>
./PINGPONG stop --depins=grass
./PINGPONG start --depins=grass
```
- Dawn
install dawn [here](https://chromewebstore.google.com/detail/dawn-validator-chrome-ext/fpdkjdnhkakefebpekbdhillbhonfjjp?authuser=0&hl=en)
> code : `7v9fdrg`
```bash
./PINGPONG config set --dawn.email=<email>  --dawn.pwd=<password_account_dawn>
./PINGPONG stop --depins=dawn
./PINGPONG start --depins=dawn
```
