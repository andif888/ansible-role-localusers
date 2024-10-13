# ansible-role-localusers

Role to manage local users.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [local_authorized_keys](#local_authorized_keys)
  - [local_groups](#local_groups)
  - [local_sudoers](#local_sudoers)
  - [local_sudoers_groups](#local_sudoers_groups)
  - [local_sudoers_groups_nopass](#local_sudoers_groups_nopass)
  - [local_sudoers_nopass](#local_sudoers_nopass)
  - [local_users](#local_users)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.1`

## Default Variables

### local_authorized_keys

Authorized Keys to be present

#### Default value

```YAML
local_authorized_keys: []
```

#### Example usage

```YAML
local_authorized_keys:
  - name: local_admin
    key: "somekey"
  - name: second_user
    key: "otherkey"
```

### local_groups

Groups to be present

#### Default value

```YAML
local_groups: []
```

#### Example usage

```YAML
local_groups: ["sudo", "adm"]
```

### local_sudoers

Sudoers to be present

#### Default value

```YAML
local_sudoers: []
```

#### Example usage

```YAML
local_sudoers: ["localadmin", "second_user"]
```

### local_sudoers_groups

Sudoers to be present

#### Default value

```YAML
local_sudoers_groups: []
```

#### Example usage

```YAML
local_sudoers_groups: ["domain-admins", "other-group"]
```

### local_sudoers_groups_nopass

Sudoers to be present

#### Default value

```YAML
local_sudoers_groups_nopass: []
```

#### Example usage

```YAML
local_sudoers_groups_nopass: ["domain-admins", "other-group"]
```

### local_sudoers_nopass

Sudoers to be present

#### Default value

```YAML
local_sudoers_nopass: []
```

#### Example usage

```YAML
local_sudoers_nopass: ["localadmin", "second_user"]
```

### local_users

Users to be present

#### Default value

```YAML
local_users: []
```

#### Example usage

```YAML
local_users:
  - name: local_admin
    expires: -1
    groups: ["sudo", "adm"]
    password_hash: "somehash"
    password_expire_max: -1
    shell: "/bin/bash"
  - name: second_user
    groups: ["sudo"]
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
