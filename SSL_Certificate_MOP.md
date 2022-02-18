## Generating Private KEY and CSR ##

```
openssl genrsa -out keyNAME.key 2048

```
## Create a Certificate Sign Request ##

```
openssl req -new -key keyNAME.key -out csrNAME.csr

```

## Generate a self Sign request ##

```
openssl x509 -req -days 365 -in csrNAME.csr -signkey keyNAME.key -out CertNAME.crt

```

## Display Certificate ##

```
openssl x509 -in CertNAME.crt -noout -text

```
## Convert Certificate into PEM format ##

```
openssl x509 -in CertNAME.crt -out CertNAME.pem -outform PEM
```

