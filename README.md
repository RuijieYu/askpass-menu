# askpass-menu
Some small helper programs to enable askpass functionalities using menus like
[dmenu](https://tools.suckless.org/dmenu/) and
[bemenu](https://github.com/Cloudef/bemenu).

## Installation

TODO. 

One should clone this repository or download and extract the repository archive,
then run `sudo` in any of the following methods:

- invoke `sudo` as: `SUDO_ASKPASS=/path/to/askpass-* sudo -A other-arguments`
- modify `/etc/sudo.conf` to contain the following line: `Path askpass
  /path/to/askpass-*`

## Synopses

All `askpass-*` programs have the same usage: a prompt is taken as its
first argument, and the entered password is output in standard output.

By design, all `askpass-*` programs should satisify the requirements
for `SUDO_ASKPASS` (see `man:sudo(8)` and `man:sudo.conf(5)`).

## Dependencies

### Runtime Dependencies

- `sudo`, or other password-prompting programs that suits the usage description.
  - support for `askpass` and `-A` was first introduced in commit `ee0491416` on
    2008-03-02.
- any POSIX-compliant shell located at `/bin/sh` for the shell scripts.

### Compile-time Dependencies

Currently none.

## Miscellaneous

Currently the following menus are implemented (with a crossmark) or planned.

- [ ] [dmenu](https://tools.suckless.org/dmenu/)
- [ ] [rofi](https://github.com/davatorium/rofi/) (using dmenu simulation mode)
- [x] [bemenu](https://github.com/Cloudef/bemenu)
