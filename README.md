# ericsysmin.selinux

Using this module you are able manage the SELinux configuration on the host. It can also reboot the host if required.

## Requirements

- `libselinux-python` package is required on the host executing the role:  

## Role Variables

| Variable | Required | Default | Comments |
|-----------------------|----------|-----------|---------|
| `selinux_policy` | No | `targeted` | The name of the SELinux policy to use |
| `selinux_state` | No | `enforcing` | The SELinux mode to be used. |
| `reboot_host` | No | `false` | This flag will tell the remote machien to reboot after modifying. |

## Example Playbooks

### Example
```

- hosts: service_engines
  roles:
    - role: ericsysmin.selinux
      reboot_host: true
```

## License

MIT

## Author Information

Eric Anderson  
[ericsysmin.com](http://ericsysmin.com)
