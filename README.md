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

| Variable                | Default        | Comments (type)                                  |
| :---                    | :---           | :---                                             |
| `tftp_root_directory`   | /tftpboot      | The path to the root directory served by tftp.   |
| `tftp_user`             | nobody         | Default user atftpd should run as                |
| `tftp_group`            | nogroup        | Default group atftpd should run as               |
| `tftp_mode`             | 750            | Default directory access mode                    |
| `tftp_verbose`          | 3              | Increase or set the level of output messages     |
| `tftp_port`             | 69             | Port on which atftp listen                       |
| `tftp_threads`          | 50             | Number of concurrent thread allowed              |

## License

BSD

## Author Information

Christian Poessinger (christian@poessinger.com)

## Example Playbook

```
$ cat tftp_servers.yml
- hosts: tftp-servers
  remote_user: root
  become_method: sudo
  become_user: root
  roles:
    - ansible-role-atftpd
```

