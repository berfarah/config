# Configuration Files

### Purpose

This repository's purpose is to hold configuration files securely, using AES-256
encryption.

It uses `openssl` and a `.key` to encrypt your decrypted files (put in the
`./decrypted` folder.

### Decrypting files

Upon changing branches or updating the repository, it automatically decrypts the
remote contents, overwriting your local decrypted files.

You will need the matching `.key` in order to decrypt the files successfully.

### Committing Changes

In order to commit your changes to configuration files you will want to run the
`bin/commit` command. This will encrypt your files in their parallel directory
and initiate a `git commit`.

### Usage with other repositories

If you would like your config files to remain in sync, you'll want to create a
script in other repositories that symlinks in the decrypted files. You could
also create a script to commit changes to your configuration automatically.
