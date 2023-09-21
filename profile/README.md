<div id="top" align="center">
<img src="https://github.com/ssh-mitm/ssh-mitm/raw/master/doc/images/ssh-mitm-logo.png" width="200"><br/>
</div>
<a href="https://github.com/ssh-mitm/ssh-mitm"><h1 align="center"> SSH-MITM - ssh audits made simple </h1></a>
<p align="center">
  <a href="https://docs.ssh-mitm.at">
    <img alt="SSH-MITM intercepting password login" title="SSH-MITM" src="https://docs.ssh-mitm.at/_images/ssh-mitm-password.png#20230214" >
  </a>
  <p align="center">ssh man-in-the-middle (ssh-mitm) server for security audits supporting<br> <b>publickey authentication</b>, <b>session hijacking</b> and <b>file manipulation</b></p>
  <p align="center">
   <a href='https://flathub.org/apps/at.ssh_mitm.server'><img height='56' alt='Download on Flathub' src='https://dl.flathub.org/assets/badges/flathub-badge-en.png'/></a>
   <a href="https://snapcraft.io/ssh-mitm">
     <img  height='56' alt="Get it from the Snap Store" src="https://snapcraft.io/static/images/badges/en/snap-store-black.svg" />
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

## Installation

**SSH-MITM** can be installed as a 
[Flatpak](https://flathub.org/apps/at.ssh_mitm.server), 
[Ubuntu Snap](https://snapcraft.io/ssh-mitm), 
[AppImage](https://github.com/ssh-mitm/ssh-mitm/releases/latest) 
and [PIP-Package](https://pypi.org/project/ssh-mitm/).

Community-supported options include installations via `[Nix](https://search.nixos.org/packages?channel=unstable&show=ssh-mitm&type=packages&query=ssh-mitm) and running on [Android devices](https://github.com/ssh-mitm/ssh-mitm/discussions/83#discussioncomment-1531873).

Install from Flathub:

    flatpak install flathub at.ssh_mitm.server
    flatpak run at.ssh_mitm.server

Install from Snap store:

    sudo snap install ssh-mitm

Install as AppImage:

    wget https://github.com/ssh-mitm/ssh-mitm/releases/latest/download/ssh-mitm-x86_64.AppImage
    chmod +x ssh-mitm*.AppImage

Install python package:

    python3 -m pip install ssh-mitm

For more installation methods, refer to the [SSH-MITM installation guide](https://docs.ssh-mitm.at/get_started/installation.html).


## Quickstart

To start SSH-MITM, all you have to do is run this command in your terminal of choice.

    ssh-mitm server --remote-host 192.168.0.x

Now let's try to connect. SSH-MITM is listening on port 10022.

    ssh -p 10022 testuser@proxyserver

You will see the credentials in the log output.

    INFO     Remote authentication succeeded
        Remote Address: 127.0.0.1:22
        Username: testuser
        Password: secret
        Agent: no agent
