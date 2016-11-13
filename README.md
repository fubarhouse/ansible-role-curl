# Ansible Role: Curl

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-curl.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-curl)

* Designed for systems lacking Curl, or systems wanting a specific version of curl.
* Builds and Installs specified Curl from [released source](https://curl.haxx.se/download/).

## Requirements

  None.

## Role Variables

Select location to install temporary, or accept the default below:
````
curl_path: /tmp
````

Select which version to install, or accept the default below:
````
curl_version: "7.51.0"
````

Select which archive type to download/extract, or accept the default below:
`````
curl_extension: "tar.gz"
`````

If you want to build from git source code, ensure the following boolean is true:
````
curl_buildfromgit: True
````

## Dependencies

  None.

## Example Playbook
````
- hosts: localhost
  roles:
    - fubarhouse.curl
````

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Karl Hepworth](https://twitter.com/fubarhouse).