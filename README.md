# KAMIICO-development-requirements

### This tutorial contains all the necessary development requirements installation guide for the DEV-KAMICO team

We will use:
- [GITHUB](https://docs.github.com/pt)
- [VSCODE](https://code.visualstudio.com)
- [DOCKER](https://www.docker.com)
- [POSTGRESQL](https://www.postgresql.org)
- [MYSQL](https://www.mysql.com)
- [DBEAVER](https://dbeaver.io)

# Installation:

Install wget on Ubuntu/Debian
```bash
apt-get install wget
```

### Check if you already have [GIT](https://github.com/git-guides/install-git#install-git-on-linux)

```bash
git --version

# if it returns error, install it with the commands below

sudo apt-get update
sudo apt-get install git-all
```
#

### To install [POSTGRESQL](https://www.postgresql.org/download/linux/ubuntu/)

```bash
# Create the file repository configuration:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

# Import the repository signing key:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# Update the package lists
sudo apt-get update

# check if the installation is ok
psql
```
#

### To install [MYSQL](https://computingforgeeks.com/how-to-install-mysql-on-debian-linux-system/)
```bash
wget https://dev.mysql.com/get/mysql-apt-config_0.8.18-1_all.deb

# Once downloaded, we need to install the repository package

sudo dpkg -i mysql-apt-config_0.8.18-1_all.deb

```
 
Note that MySQL 5.7 repository is not yet availaible for Debian 11 (Bullseye). In this case, we are going to select Debian 10 (Buster) for both Debian 11 and Debian 10.

![alt text](https://user-images.githubusercontent.com/87615776/203994061-e1717646-6156-412b-ad3f-6741c7a3f317.jpg)

Ensure mysql-8.0 is selected.

![alt text](https://user-images.githubusercontent.com/87615776/203994063-b857dd7b-2690-439e-9a49-fe7abc1e4d4e.jpg)

Next select mysql-5.7 as shown

![alt text](https://user-images.githubusercontent.com/87615776/203995855-11e2ce9a-d1ba-4759-a72c-f6c170f04d8d.jpg)

Next, use the down arrow key to select Ok then click Ok and the package will be installed.

![alt text](https://user-images.githubusercontent.com/87615776/203994085-5117169a-67c9-4303-903d-f4210798b013.jpg)

```bash
# check if the installation is ok
mysql -V
```
#

### To install [VSCODE](https://www.cyberciti.biz/faq/howto-install-curl-command-on-debian-linux-using-apt-get/)

```bash
# install curl if dont have

sudo apt-get install curl

curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg

sudo install -o root -g root -m 644 microsoft.gpg /usr/share/keyrings/microsoft-archive-keyring.gpg

sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/usr/share/keyrings/microsoft-archive-keyring.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

```
Then update the package cache and install the package using

```bash
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install code # or code-insiders
```
#

### To install [DBEAVER](https://www.cyberciti.biz/faq/howto-install-curl-command-on-debian-linux-using-apt-get/)
![alt text](https://user-images.githubusercontent.com/87615776/203999828-85a23077-8375-4f71-a6b9-8564c3e9f638.png)

### To install [DOCKER](https://docs.docker.com/engine/install/ubuntu/)

Uninstall old versions
Older versions of Docker went by the names of docker, docker.io, or docker-engine. Uninstall any such older versions before attempting to install a new version:
```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

Set up the repository
Update the apt package index and install packages to allow apt to use a repository over HTTPS:

```bash
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
Add Docker’s official GPG key:

```bash
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

Use the following command to set up the repository:

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
  
Update the apt package index:

```bash
sudo apt-get update
```
Install Docker Engine, containerd, and Docker Compose.

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

Verify that the Docker Engine installation is successful by running the hello-world image:

```bash
sudo docker run hello-world
```
#

## Step by Step configuration of Odoo environment:

First install the components below and follow [this](https://github.com/devkami/tutorial_odoo_tecnativa) tutorial

```bash
python3 -m pip install --user pipx
pipx install docker-compose
pipx install copier
pipx install invoke
pipx install pre-commit
pipx ensurepath
```
#

# Now get Odoo and addons code following [this](https://github.com/Tecnativa/doodba-copier-template/blob/main/docs/daily-usage.md#environments) tutorial



