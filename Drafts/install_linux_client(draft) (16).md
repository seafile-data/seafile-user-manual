# Install Seafile Client on Linux

## Ubuntu

Ubuntu users can install Seafile client from the [Official PPA](https://code.launchpad.net/~seafile/+archive/ubuntu/seafile-client):

```sh
sudo add-apt-repository ppa:seafile/seafile-client
sudo apt-get update
sudo apt-get install seafile-gui

```

If you only want to install the command-line client, run `sudo apt-get install seafile-cli` instead.

If you want to install the debug symbols (for example, when you want to report a bug), you can install the following packages:

```sh
sudo apt-get install libsearpc-dbg ccnet-dbg libccnet-dbg seafile-daemon-dbg libseafile-dbg seafile-gui-dbg

```

Now you can start seafile client from Unity's dash.

## Debian

Debian users can install Seafile client from our debian repo:

To install the client, first add the signing key:

```sh
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 8756C4F765C9AC3CB6B85D62379CE192D401AB61

```

Then add the repo to your apt source list, using the line corresponding to your debian version :

```
# For Debian 7
echo deb http://deb.seadrive.org wheezy main | sudo tee /etc/apt/sources.list.d/seafile.list

# For Debian 8
echo deb http://deb.seadrive.org jessie main | sudo tee /etc/apt/sources.list.d/seafile.list

# For Debian 9
echo deb http://deb.seadrive.org stretch main | sudo tee /etc/apt/sources.list.d/seafile.list

```

Update your local apt cache :

```
sudo apt-get update

```

Now install the client:

```sh
sudo apt-get install seafile-gui

```

If you only want to install the command-line client, run `sudo apt-get install seafile-cli` instead.

## CentOS/RHEL

Since 7.0.3 version, we provide official repo for CentOS or RHEL. Currently only CentOS/RHEL 7 is supported.

Add the repo (The same repo is used for seadrive.)

```
wget -O- https://git.io/seadrive-centos7-repo | sudo tee /etc/yum.repos.d/seadrive.repo

```

Install Seafile Client

```
sudo yum install -y epel-release
sudo yum install -y seafile --enablerepo=cr

```

## Fedora (Community Maintained)

There is a _community maintained_ Seafile Client RPM package in Fedora's [official repository](https://src.fedoraproject.org/rpms/seafile).

## Arch Linux (Community Maintained)

There is a _community maintained_ Seafile Client package for Arch Linux:

<https://aur.archlinux.org/packages/seafile-client/>

## Linux CLI Usage

Please refer to [this documentation](linux-cli.md) for how to use Linux client on a command line server.
