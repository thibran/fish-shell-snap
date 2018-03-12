Fish-Shell Snap
===============

Unofficial [fish](https://fishshell.com) snap package.

Caution:  
This package needs more testing before it can be declared stable.

Later the snap might be added to the
[Snap Store](https://snapcraft.io/store).


| Tested with:        | Snapd version: | Status:                       |
|---------------------|----------------|-------------------------------|
| Ubuntu 16.04        | 2.31.1         | works                         |
| Ubuntu 17.10        | 2.31.1         | works                         |
| openSUSE Tumbleweed | 2.27.6-1.5     | $TERM is set to `ansi`        |
| Fedora 27           | 2.30-1.fc27    | doesn't support classic snaps |
| Debian testing      | 2.31.1         | works                         |


To install the snap package manager follow [these instructions](https://docs.snapcraft.io/core/install). Don't forget to check if your
distribution of choice supports [classic snaps](https://docs.snapcraft.io/core/install#support-overview).


Building the Snap
-----------------

Checkout the code:

    git clone https://github.com/thibran/fish-shell-snap.git

    cd fish-shell-snap


Install Snapcraft:

    sudo snap install --classic snapcraft


To build the snap, run inside the `fish-shell-snap` folder:

    snapcraft


To install the snap-package:

    sudo snap install fish-thibran_*.snap --classic --dangerous

The `--dangerous` is because the snap is not signed by the snap-store right now.


Optional, the snapcraft build folders & files can be cleaned with:

    snapcraft clean fish-shell -s pull


Fish as default shell
---------------------

To make fish the default shell, add to `/etc/shells` the line:

    /snap/bin/fish-thibran.fish

Then run:

    chsh -s /snap/bin/fish-thibran.fish


Links
=====

[Snapcraft Docs](https://docs.snapcraft.io/)  
[Snap Build Service](https://build.snapcraft.io/)  
[About Snaps](https://www.ubuntu.com/desktop/snappy)