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

Check if you already have [GIT](https://github.com/git-guides/install-git#install-git-on-linux)

```bash
git --version

# if it returns error, install it with the commands below

sudo apt-get update
sudo apt-get install git-all
```
To install [POSTGRESQL](https://www.postgresql.org/download/linux/ubuntu/)

```bash
# Create the file repository configuration:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

# Import the repository signing key:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# Update the package lists
sudo apt-get update
```
To install [MYSQL](https://computingforgeeks.com/how-to-install-mysql-on-debian-linux-system/)
```bash
wget https://dev.mysql.com/get/mysql-apt-config_0.8.18-1_all.deb

# Once downloaded, we need to install the repository package

sudo dpkg -i mysql-apt-config_0.8.18-1_all.deb

```

