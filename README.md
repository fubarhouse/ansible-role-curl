# Ansible Role: Curl

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-curl.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-curl)

* Designed for systems lacking Curl, or systems wanting a specific version of curl.
* Builds and Installs specified Curl from [released source](https://curl.haxx.se/download/).

## Development state

  This role is still under development, please use at own risk.
  It has only been tested so far on OSX Sierra, unless Travis says otherwise.

## Requirements

  None known, but we're still looking into a complete list.

## Role Variables

Select location to install temporary data whilst installing curl
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