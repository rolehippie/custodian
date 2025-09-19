# custodian

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/custodian)
[![General Workflow](https://github.com/rolehippie/custodian/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/custodian/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/custodian/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/custodian/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/custodian/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/custodian/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/custodian)](https://github.com/rolehippie/custodian/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.custodian-blue)](https://galaxy.ansible.com/rolehippie/custodian)

Ansible role to install and configure docker-custodian.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [custodian_dangling_volumes](#custodian_dangling_volumes)
  - [custodian_exclude_container_label](#custodian_exclude_container_label)
  - [custodian_exclude_image](#custodian_exclude_image)
  - [custodian_image](#custodian_image)
  - [custodian_interval](#custodian_interval)
  - [custodian_max_container_age](#custodian_max_container_age)
  - [custodian_max_image_age](#custodian_max_image_age)
  - [custodian_pull_image](#custodian_pull_image)
  - [custodian_version](#custodian_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### custodian_dangling_volumes

Remove dangling volumes

#### Default value

```YAML
custodian_dangling_volumes: false
```

### custodian_exclude_container_label

List of labels to exclude+

#### Default value

```YAML
custodian_exclude_container_label: []
```

### custodian_exclude_image

List of images to exclude

#### Default value

```YAML
custodian_exclude_image: []
```

### custodian_image

Docker image to use for deployment

#### Default value

```YAML
custodian_image: toolhippie/docker-custodian:{{ custodian_version }}
```

### custodian_interval

Interval for the systemd timer

#### Default value

```YAML
custodian_interval: daily
```

### custodian_max_container_age

Max container age

#### Default value

```YAML
custodian_max_container_age: 3days
```

### custodian_max_image_age

Max image age

#### Default value

```YAML
custodian_max_image_age: 3days
```

### custodian_pull_image

Pull image as part of the tasks

#### Default value

```YAML
custodian_pull_image: true
```

### custodian_version

Version of docker custodian to use

#### Default value

```YAML
custodian_version: 0.7.4
```

## Discovered Tags

**_custodian_**

## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)
- [community.docker](https://github.com/ansible-collections/community.docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
