# Configuration Files

### Purpose

This repository's purpose is to hold configuration files securely, using AES-256
encryption.

It uses `openssl` and a `[environment].key` to encrypt your decrypted files (put
in the `./decrypted` folder.

### Initial setup

In order to install the commit hooks, just run `bin/setup`.

You will need a matching `[environment].key` file in order to en/decrypt files
for this repository.

### Decrypting files

Upon changing branches or updating the repository, it automatically decrypts the
remote contents, overwriting your local decrypted files.

### Committing Changes

In order to commit your changes to configuration files you will want to run

    bin/run encrypt

This encrypts your files, at which point you can add them to staging.

### Usage with other repositories

If you would like your config files to remain in sync, you'll want to create a
script in other repositories that symlinks in the decrypted files.
