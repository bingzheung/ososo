---
title: Handbooks - Bing Jheung
description: Handbooks
keywords: handbook
---

[FreeBSD Handbook](freebsd)

[Fedora Handbook](fedora)

[macOS Handbook](macosx)

Compress
```bash
tar -cf - ./folder | xz -c9e --threads=0 - > ./compressed.xz
``` 

OpenSSL encrypt/decrypt
```bash
openssl enc -e -salt -pbkdf2 -aes-256-cfb -in notes.txt -out notes.txt.bin
openssl enc -d -pbkdf2 -aes-256-cfb -in notes.txt.bin -out notes.txt
```   

OpenSSL - generate dhparam
```bash
openssl dhparam -out ./dhparam.pem 4096
```

GnuPG Usage
```bash
gpg --encrypt --recipient [KEYID] --output notes.txt.gpg notes.txt
gpg --sign --encrypt --recipient [KEYID] --output notes.txt.gpg notes.txt
gpg --decrypt --output notes.txt notes.txt.gpg
gpg --symmetric --cipher-algo AES256 --output notes.txt.gpg notes.txt

gpg --list-keys --keyid-format LONG
``` 

GnuPG Configuration

[Creating newer ECC keys for GnuPG](https://www.gniibe.org/memo/software/gpg/keygen-25519.html)

[Creating the perfect GPG keypair](https://alexcabal.com/creating-the-perfect-gpg-keypair)

export gpg keys: 

https://gist.github.com/chrisroos/1205934

https://www.phildev.net/pgp/gpg_moving_keys.html

```bash
gpg --export --armor KEYID > PublicKey.asc
gpg --export-secret-keys --armor KEYID > SecretKey.asc
gpg --export-ownertrust > OwnerTrust.asc
```  

Generate SSH Keys
```bash
ssh-keygen -t ed25519 -C "name@email.com"
```

.vimrc
```
syntax on
set number
set encoding=utf-8
set expandtab
set softtabstop=8
set shiftwidth=8
set cindent
set autoindent
set smartindent
```

Run on background
```bash
./a.out > /dev/null 2>&1 &
```   

Change permissions
```bash
find . -type d -print0 | xargs -0 chmod 0755
find . -type f -print0 | xargs -0 chmod 0644
```
