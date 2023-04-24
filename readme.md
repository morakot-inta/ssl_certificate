### How to Create Self Sign Certificate

1. Genarate Private Key.
```
openssl genras -out ca.key
```

3. Genareate Self Sign Cert from Private Key.
```
openssl req -x509 -new -nodes -sha512 -day 365 -key ca.key -out ca.crt
```

5. Genarate PFX file from private key and self sign.
```
openssl pkcs12 -inkey ca.key -in ca.crt -export -out ca.pfx
```
