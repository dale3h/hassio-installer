# Hass.io Installer for Raspberry Pi 3 B+

[![Documentation][badge-docs]][hass-io]
[![Discord][badge-discord]][discord]
[![Version][badge-version]][hassio-installer]
[![Donate][badge-donate]][donate]

This script will install all [requirements][requirements], and then install
[Hass.io][hass-io]. Please report any [issues][issues] that experience.

## Requirements

- [Raspberry Pi 3 B+][raspberry-pi]
- [Raspbian Stretch Lite][stretch-lite]

## Useful Tips

- Be sure to secure your Raspberry Pi by disabling SSH and changing the
  password for `pi` user.

- If you plan to install via SSH, be sure to [create a file named `ssh` on your
  SD card][enable-ssh] in `/boot` to enable SSH on first boot.

- If you plan to connect via WiFi, be sure to setup your `wpa_supplicant.conf`
  file in `/boot` prior to your first boot.

## Installation Instructions

1. Flash the latest [Raspbian Stretch Lite][stretch-lite] image.
1. Run this as root user (`sudo su`):

```bash
curl -sL https://raw.githubusercontent.com/dale3h/hassio-installer/master/hassio_rpi3bp | bash -s
```

## Known Issues

- **Bluetooth BCM43xx** add-on does not work

- **SSH server** add-on (from **Official add-ons**) does not work
  - ***Fix:** use community SSH add-on instead*

- Port conflict when using SSH add-on
  - ***Fix:** change the port in the SSH add-on options*

## Changelog & Releases

This project keeps a [change log][changelog]. The format of the log is based
on [Keep a Changelog][keep-a-changelog].

Releases are based on [Semantic Versioning][semantic-versioning], and use the
format of ``MAJOR.MINOR.PATCH``. In a nutshell, the version will be incremented
based on the following:

- ``MAJOR``: Incompatible or major changes.
- ``MINOR``: Backwards-compatible new features and enhancements.
- ``PATCH``: Backwards-compatible bugfixes and package updates.

## License

MIT License

Copyright (c) 2018 Dale Higgs <@dale3h>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[changelog]: CHANGELOG.md
[discord]: https://discord.gg/u26F9Kw
[donate]: https://www.buymeacoffee.com/dale3h
[enable-ssh]: https://howchoo.com/g/ote0ywmzywj/how-to-enable-ssh-on-raspbian-jessie-without-a-screen
[hass-io]: https://www.home-assistant.io/hassio/
[hassio-installer]: https://github.com/dale3h/hassio-installer
[issues]: /issues
[keep-a-changelog]: https://keepachangelog.com/en/1.0.0/
[raspberry-pi]: http://a.co/ciXqByX
[requirements]: https://github.com/home-assistant/hassio-build/blob/master/install/README.md#requirements
[semantic-versioning]: https://semver.org/spec/v2.0.0.html
[stretch-lite]: https://downloads.raspberrypi.org/raspbian_lite_latest

[badge-discord]: https://img.shields.io/discord/330944238910963714.svg?style=for-the-badge&maxAge=3600
[badge-docs]: https://img.shields.io/badge/read-docs-blue.svg?style=for-the-badge
[badge-donate]: https://img.shields.io/badge/beerpay-$5-orange.svg?style=for-the-badge
[badge-version]: https://img.shields.io/badge/version-1.1.1-red.svg?style=for-the-badge
