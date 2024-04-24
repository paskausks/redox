# Redox VIA Layouts

This is my [Redox](https://github.com/mattdibi/redox-keyboard) keyboard layout for the [VIA](https://github.com/the-via) firmware. Its primary purpose is for typing in English and for coding in GDScript and TypeScript.

`redox.colemak.json` utilizes the [Colemak-DH](https://colemakmods.github.io/mod-dh/) layout, with a fallback QWERTY layout available on layer 3. `redox.qwerty.json` is essentially the same with the primary layout being QWERTY, for gaming without having to remap.

You can edit and flash the layout at <https://usevia.app/>.

## Received invalid protocol version from device

If, when using usevia.app, you fail to connect to the keyboard (likely on linux), then its probably a permission issue.

Go to `chrome://device-log/`, note the address of the device (e.g. `/dev/hidraw3`), and just give yourself ownership of it:

```
sudo chown $USER:$USER /dev/hidraw3
```

Source: [github.com](https://github.com/the-via/app/issues/91#issuecomment-1505095474)
