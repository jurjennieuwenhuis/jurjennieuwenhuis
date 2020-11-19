---
layout: post
title:  "Create JWT SSL keys"
date:   2020-11-19 21:00:00 +0200
categories: symfony jwt
---
First open the `.env` file with the JWT_PASSPHRASE - we'll need it to create the private key.

Create the directory to store the keys:

```bash
mkdir -p config/jwt
```

Execute the following command to generate the private key:

```bash
openssl genrsa -out config/jwt/private.pem -aes256 4096
```

Supply the passphrase if the generator asks for it.

Execute the next command to create the public key:

```bash
openssl rsa -pubout -in config/jwt/private.pem -out config/jwt/public.pem
```

When asked for the passphrase, paste the passphrase you used when generating the private key.