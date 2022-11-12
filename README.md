# go-development
Learning GO

## Development Environment Setup

### Setup Windows Subsystem for Linux (WSL 2)
1. [Installation Instructions](https://docs.microsoft.com/en-us/windows/wsl/install)
2. [Tutorial](https://docs.microsoft.com/en-us/windows/wsl/setup/environment)

### Install Docker Desktop
[Installation Instructions](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-containers#install-docker-desktop)
_Optional_ - Create a Docker Hub account

### Setup VS Code Extensions
1. Global
    * Remote - WSL
    * Remote - SSH
    * Remove - SSH: Editing Configuration Files
    * Remote - Containers
2. WSL
    * Docker
    * GitLens -- Git supercharged

### Install GO
```
# Connect to Ubuntu through VS Code via Terminal
$ cd /opt
$ sudo su
$ mkdir wsluser/
$ cd wsluser/
$ curl -OL https://golang.org/dl/go1.16.7.linux-amd64.tar.gz
$ cd ../
$ chown -R wsluser:wsluser wsluser/
$ exit
$ tar -C /usr/local -xvzf go1.16.7.linux-amd64.tar.gz
$ vi ~/.profile 
# set PATH so it includes go's bin if it exists
if [ -d "/usr/local/go/bin" ] ; then
    PATH=$PATH:/usr/local/go/bin
fi

$ source ~/.profile 
$ echo $PATH
$ go version
$ cd ~/git/go-development/
```
