# hot-oat

[![Check Shell Scripts](https://github.com/tonyskapunk/hot-oat/actions/workflows/shellcheck.yaml/badge.svg)](https://github.com/tonyskapunk/hot-oat/actions/workflows/shellcheck.yaml)
[![Release](https://img.shields.io/github/v/release/tonyskapunk/hot-oat?style=plastic)]()
[![License](https://img.shields.io/github/license/tonyskapunk/hot-oat?style=plastic)](/LICENSE)

![Logo of a bowl with oats, steam going out with a red circle in the back representing the sun](./assets/hot-oat.svg)

🔥🥣

A wrapper script to setup and run HOTP (Hash-based message authentication code One Time Password)

## Requirements and Optional Packages

### Required packages

- [openssl](http://www.openssl.org/)
- [oathtool](https://www.nongnu.org/oath-toolkit/) from EPEL

### Optional packages

- [qrencode](http://fukuchi.org/works/qrencode/) - QR generator
- [wl-clipboard](https://github.com/bugaevc/wl-clipboard) - Wayland clipboard copy tool (default)
- [xclip](http://sourceforge.net/projects/xclip)   - Server X clipboard

### Red Hat based

`oathtool` is available in [EPEL](https://docs.fedoraproject.org/en-US/epel/) follow the instructions there to install EPEL depending on your version and distribution

Required:

```Shell
dnf install -y oathtool
```

Optional:

```Shell
dnf install -y qrencode 
```

### Debian based

Required:

```Shell
apt update
apt install -y oathtool
```

Optional:

```Shell
apt update
apt install -y qrencode
```

### Arch Linux

Required:

```Shell
pacman -Sy --noconfirm oath-toolkit
```

Optional:

```Shell
pacman -Sy --noconfirm qrencode
```

## Install

Copy the script `hot-oat` to a directory in your path, e.g. `~/.local/bin`

## Overriding defaults

| Environment Name     | Default             | Description                                              |
|----------------------|---------------------|----------------------------------------------------------|
| HOT_OAT_COPY_TOOL    | wl-copy             | The command to use to copy the password to the clipboard |
| HOT_OAT_COPY_OPTIONS | -n -o               | The options to pass to the copy command                  |
| HOT_OAT_DIR          | `~/.config/hot-oat` | The directory where the key and counter are stored       |

### Example

## Acknowledgments

- Thanks to [pierreblanc](https://github.com/pierreblanc) for the idea
