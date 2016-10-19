# Kamailio Snapcraft

Spec files for building Ubuntu Snap package.

More about snap packages can be found at:

  * http://snapcraft.io

Kamailio SIP Server project:

  * https://www.kamailio.org

## Installation

These installation instructions were used on Ubuntu 16.04.

First you have to install snapcraft:

```
apt-get install snapcraft
```

Clone this repository and inside its root directory run:

```
snapcraft
```

The above command will build the kamailio snap package, a file named like:

```
kamailio-dev_5.0_amd64.snap
```

To install it on dev mode, use:

```
sudo snap install kamailio-dev_5.0_amd64.snap --devmode --dangerous
```

After installation, Kamailio should be started. It can be controlled via systemd:

```
systemctl start snap.kamailio-dev.kamailio
systemctl stop snap.kamailio-dev.kamailio
systemctl restart snap.kamailio-dev.kamailio
```

The snap package can be removed with:

```
sudo snap remove kamailio-dev
```

## Remarks

This is a basic snap spec file, intended to get one started with Kamailio and snapcraft. There can be many improvements, contributions are more than welcome.

The work was done during TADHack Global - Berlin 2016. A short presentation related to it is available at:

  * http://www.slideshare.net/miconda/snappy-kamailio

Enjoy!
