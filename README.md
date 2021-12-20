# cypress-local-https

> Example using Cypress to test Create-React-App site running with custom certificate for domain "my-secure-site"

## Making certificate

```
$ brew install mkcert
$ mkcert -install
$ mkdir .cert
$ mkcert -key-file ./.cert/key.pem -cert-file ./.cert/cert.pem "my-secure-site"
```

## Start the local site

```
$ HTTPS=true SSL_CRT_FILE=./.cert/cert.pem SSL_KEY_FILE=./.cert/key.pem npm start
```
