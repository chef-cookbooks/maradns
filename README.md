# maradns Cookbook

[![Build Status](https://travis-ci.org/chef-cookbooks/maradns.svg?branch=master)](http://travis-ci.org/chef-cookbooks/maradns) [![Cookbook Version](https://img.shields.io/cookbook/v/maradns.svg)](https://supermarket.chef.io/cookbooks/maradns)

Installs and configures maradns.

## Requirements

### Platforms

- Debian 7 (8 has no maradns package)
- Ubuntu 12.04+

### Chef

- Chef 12.1+

### Cookbooks

- None

## Attributes

- `node['maradns']['recursive_acl']` -

## Recipes

### default

Installs the maradns package, manages the `maradns` and `zoneserver` services and writes out the configuration files.

## Usage

In order to use this recipe, create the DNS entry configuration file as `templates/default/db.DOMAIN.erb`, where `DOMAIN` is the domain detected by `ohai` on the node. For example, if the node's domain is `example.com`, the file would be `db.example.com.erb`. Refer to the maradns zone file documentation for more information on how to write this configuration.

- <http://www.maradns.org/notes.html>

## License & Authors

**Author:** Cookbook Engineering Team ([cookbooks@chef.io](mailto:cookbooks@chef.io))

**Copyright:** 2009-2016, Chef Software, Inc.

```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
