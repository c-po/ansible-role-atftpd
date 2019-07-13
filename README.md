# Ansible role `atftpd`

An Ansible role for installing advanced TFTP (Trivial File Transfer Protocol) server Debian/Ubuntu.

- install all necessary packages
- manage configuration

For more relevant documentation on TFTP, see:
- [`atftpd(8)` man page](https://linux.die.net/man/8/atftpd)

## Requirements

none

## Dependencies

none

## Role Variables

| Variable                      | Default                              | Comments (type)                                                |
| :---                          | :---                                 | :---                                                           |
| `tftp_root_directory`         | /tftpboot                            | The path to the root directory served by tftp.                 |

## License

BSD

## Author Information

Christian Pössinger (christian@poessinger.com)
