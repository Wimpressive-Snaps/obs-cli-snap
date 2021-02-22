# obs-cli-snap

[![obs-cli](https://snapcraft.io/obs-cli/badge.svg)](https://snapcraft.io/obs-cli)
[![obs-cli](https://snapcraft.io/obs-cli/trending.svg?name=0)](https://snapcraft.io/obs-cli)

[obs-cli](https://github.com/leafac/obs-cli) is a thin wrapper around [obs-websocket-js](https://github.com/haganbmj/obs-websocket-js),
which in turn is a wrapper around [obs-websocket](https://obsproject.com/forum/resources/obs-websocket-remote-control-obs-studio-from-websockets.466/).
It supports authentication and everything else that obs-websocket provides.

An unofficial snap built with ❤︎ by Martin Wimpress using configuration at 
<https://github.com/Wimpressive-Snaps/obs-cli-snap> from the upstream project source <https://github.com/leafac/obs-cli>

## Install

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/obs-cli)

```
snap install obs-cli
```

## Usage

```
Usage: obs-cli [options] <request[=arguments]...>

Remote control OBS from the command line.

Arguments:
  request[=arguments]        a request name (for example, ‘GetRecordingFolder’), optionally followed by arguments (for
                             example, ‘SetRecordingFolder='{ "rec-folder": "/tmp/" }'’) (see
                             https://github.com/Palakis/obs-websocket/blob/4.x-current/docs/generated/protocol.md for the
                             complete list of requests and their arguments)

Options:
  -a, --address <address>    the address to the machine in which OBS is running and the port configured in OBS under Tools >
                             WebSockets Server Settings (default: "localhost:4444")
  -p, --password <password>  the password configured in OBS under Tools > WebSockets Server Settings
  -f, --field <field>        project a field out of the OBS response, for example, given an OBS response of ‘[{ ...,
                             "streaming": false, ...}]’ and a <field> of ‘0.streaming’, obs-cli outputs just ‘false’; this is
                             a convenience for applications that need only one part of the response
  -V, --version              output the version number
  -h, --help                 display help for command
```
