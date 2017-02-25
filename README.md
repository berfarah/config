# Configuration Files

### Purpose

This repository's purpose is to hold configuration files securely, using AES-256
encryption.

It uses `openssl` and a `[environment].key` to encrypt your files.

### Initial setup

In order to install the necessary dependencies, just run `bin/setup`.

You will need a matching `[environment].key` file in order to en/decrypt files
for this repository.

Available environments:
- development
- staging

### Usage with other repositories

If you would like your config files to remain in sync, you'll want to create a
script in other repositories that symlinks them.
