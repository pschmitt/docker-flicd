# Docker container for flicd

## Usage

```
docker run -it --rm --cap-add NET_ADMIN --net=host -v $PWD/config:/config pschmitt/flicd
```

## Notes

This docker file exposes port 5551 by default.

If you have more than one bluetooth adapter append `-h hciX` where `X` is the id
of the bluetooth adapter (obtainable via `hcitool dev`).

Bear in mind that bluez should be turned off for this to work correctly.

## Systemd service file

confer [flicd.service](flicd.service)

## Upstream

https://github.com/50ButtonsEach/fliclib-linux-hci
