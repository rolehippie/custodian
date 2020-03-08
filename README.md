# custodian

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/custodian/status.svg)](https://cloud.drone.io/rolehippie/custodian)

Ansible role to configure docker-custodian

## Table of content

* [Default Variables](#default-variables)
  * [custodian_dangling_volumes](#custodian_dangling_volumes)
  * [custodian_exclude_container_label](#custodian_exclude_container_label)
  * [custodian_exclude_image](#custodian_exclude_image)
  * [custodian_image](#custodian_image)
  * [custodian_interval](#custodian_interval)
  * [custodian_max_container_age](#custodian_max_container_age)
  * [custodian_max_image_age](#custodian_max_image_age)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

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

Docker image to use

#### Default value

```YAML
custodian_image: toolhippie/docker-custodian:latest
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

## Dependencies

- '['
- '  "[docker](https://github.com/rolehippie/docker)"'
- ']'

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
