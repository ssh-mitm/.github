<div id="top" align="center">
<img src="https://github.com/ssh-mitm/ssh-mitm/raw/master/doc/images/ssh-mitm-logo.png" width="200"><br/>
</div>
<h1 align="center"> SSH-MITM - ssh audits made simple </h1>
<p align="center">
  <a href="https://www.ssh-mitm.at">
    <img alt="SSH-MITM intercepting password login" title="SSH-MITM" src="https://www.ssh-mitm.at/img/ssh-mitm-password.png?20220211" >
  </a>
  <p align="center">ssh man-in-the-middle (ssh-mitm) server for security audits supporting<br> <b>publickey authentication</b>, <b>session hijacking</b> and <b>file manipulation</b></p>
  <p align="center">
   <a href="https://snapcraft.io/ssh-mitm">
     <img alt="Get it from the Snap Store" src="https://snapcraft.io/static/images/badges/en/snap-store-black.svg" />
   </a>
   <br />
   <br />
   <a href="https://docs.ssh-mitm.at"><img src="https://read-the-docs-guidelines.readthedocs-hosted.com/_downloads/d9606423d87d78fcceae4ee2af883b12/logo-wordmark-dark.png" title="read the docs" width="256"></a>
  </p>
</p>


<h3 align="center">Contributors</h3>
<p align="center">
<a href="https://github.com/ssh-mitm/ssh-mitm/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ssh-mitm/ssh-mitm" />
</a>
</p>

## Installation SSH-MITM

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/monitor-loading-progress.svg" align="left" width="138">

The first step to using any software package is getting it properly installed.

To install SSH-MITM, simply run this simple command in your terminal of choice:

    $ pip install ssh-mitm

## Connect to the network

<img src="https://www.ssh-mitm.at/assets/images/streamline-free/programmer-male.svg" align="left" width="138">

To start an intercepting mitm-ssh server on Port 10022, all you have to do is run a single command.

```bash
# start the mitm server
$ ssh-mitm server --remote-host 192.168.0.x

# connect to the mitm server
$ ssh -p 10022 user@proxyserver
```
## Spoofing FIDO Tokens

SSH-MITM is able to spoof FIDO Tokens which can be used for 2 factor authentication.

The attack is called [trivial authentication](https://docs.ssh-mitm.at/trivialauth.html) ([CVE-2021-36367](https://docs.ssh-mitm.at/CVE-2021-36367.html), [CVE-2021-36368](https://docs.ssh-mitm.at/CVE-2021-36368.html)) and can be enabled with the command line argument `--enable-trivial-auth`.

  ssh-mitm server --enable-trivial-auth

Using the trivial authentication attack does not break password authentication, because the attack is only performed when a publickey login is possible.

<p align="center">
  <b>Video explaining the spoofing attack:</b><br/>
  <i>Click to view video on vimeo.com</i><br/>
  <a href="https://vimeo.com/showcase/9059922/video/651517195">
  <img src="https://github.com/ssh-mitm/ssh-mitm/raw/master/doc/images/ds2021-video.png" alt="Click to view video on vimeo.com">
  </a>
</p>

<p align="center">
  <b><a href="https://github.com/ssh-mitm/ssh-mitm/files/7568291/deepsec.pdf">Downlaod presentation slides</a></b>
</p>
