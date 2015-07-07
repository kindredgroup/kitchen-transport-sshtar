# kitchen-transport-sshtar

[![Build Status](https://api.travis-ci.org/unibet/kitchen-transport-sshtar.svg)](https://travis-ci.org/unibet/kitchen-transport-sshtar)
[![Gem Version](https://badge.fury.io/rb/kitchen-transport-sshtar.svg)](http://badge.fury.io/rb/kitchen-transport-sshtar)

This transport is based on piping native ssh (usually OpenSSH) and tar commands, so that all files are transferred as a single ssh stream providing dramatic performance improvements. This transport will only work with TK 1.4 and Linux/Unix like systems with mentioned binaries available in the PATH.

Only passwordless (using ssh key pair) communication is supported at the moment.

## Recommended **.kitchen.yml** snippet to activate SSH-Tar transport

```
transport:
  name: sshtar
  compression: zlib
  compression_level: 9
  ssh_key: ~/.vagrant.d/insecure_private_key
  username: vagrant
```

## Gemfile
```
gem 'kitchen-transport-sshtar'
```
