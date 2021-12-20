# cypress-local-https

> Example using Cypress to test Create-React-App site running with custom certificate for domain "my-secure-site"

## Making certificate

Before testing the site, we need to make local self-signed certificate in the folder ".cert". On Mac I used the following commands to create a self-signed certificate for domain "my-secure-site"

```
$ brew install mkcert
$ mkcert -install
$ mkdir .cert
$ mkcert -key-file ./.cert/key.pem -cert-file ./.cert/cert.pem "my-secure-site"
```

You should now have two text files in the folder `.cert`: `cert.pem` and `key.pem`

## Start the local site

Let's use the `react-scripts to start the site with the [.env.development](./.env.development) settings (HTTPS, local certificate)

```
$ npm start
```
