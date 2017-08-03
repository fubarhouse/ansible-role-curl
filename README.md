# Ansible Role: Curl

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-curl.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-curl)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-fubarhouse--curl-13298.svg)](https://galaxy.ansible.com/fubarhouse/curl)

* Designed for systems lacking Curl, or systems wanting a specific version of curl.
* Builds and Installs specified Curl from [released source](https://curl.haxx.se/download/).

## Requirements

  None.

## Role Variables

Additional installation flags are optional, to run these flags on `configure`, specify the flags as follows:
````
curl_configure_flags:
  - disable-shared
  - with-ssl
````

The above configuration will validate to the following:
````
./configure --disable-shared --with-ssl
````

As a result of failing travis tests the option to use a supported mirror is available.

To use one of the mirrors, specify the http/s address like this:
````
curl_source: http://curl.haxx.se/download
````

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