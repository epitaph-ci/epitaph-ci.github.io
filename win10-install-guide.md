# Epitaph CI Windows 10 Install Guide

> ***Notice: The epitaph-ci core program is not finished already, so wait until I finish the epitaph-ci core package***

## Install CI

To install epitaph-ci, you can either use npm or chocolatey.

**Chocolatey**

``` powershell
choco install epitaph-ci
```

**NPM**

``` bash
npm install @epitaph/core -g
```

## Install Docker

See the documentation on [Docker](https://docs.docker.com/docker-for-windows/install/) to install docker on Windows 10, if you are not using Windows 10, there's not a official support to epitaph-ci, but you can use the **Native RT** function for epitaph-ci. To use **Native RT** function of epitaph-ci, see [Native RT User Guide](native-rt-install).

## Start CI Server

Run command below to start epitaph-ci on `0.0.0.0:8711`(You should be able to access it from `localhost:8711`), and initialize the registry lib, then enter the **Epitaph Subshell**:

``` bash
ept --host=0.0.0.0 --port=8711 --init --subshell
```

There should be some messages like below

```
Epitaph CI v0.0.1
Generating data directory at `%USERPROFILE%\.epitaph`
Generating config at `%USERPROFILE%\.epitaph.js`
Set host to `0.0.0.0`
Set port to `8711`
Start listening request on `0.0.0.0:8711`
Status URL is `0.0.0.0:8711`
Registry URL is `0.0.0.0:8711/registry`
Build Request URL is `0.0.0.0:8711/buildReq`

Entering Epitaph CI Subshell...

Epitaph CI Subshell v0.0.1

epitaph-ci(0)>
```

The last line of the message above is the subshell of Epitaph CI, you can manage your server at the subshell.

**For more documentation, see [Epitaph Subshell](subshell)**

