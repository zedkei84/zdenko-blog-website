---
date: 2020-10-14 00:00:00
title: Install kubelogin on WSL
categories:
  - kubernetes
description: Jekyll template for digital agencies
type: Document
---
`kubelogin` is a kubectl plugin for [Kubernetes OpenID Connect (OIDC) authentication](https://kubernetes.io/docs/reference/access-authn-authz/authentication/#openid-connect-tokens), also known as `kubectl oidc-login`.

Kubelogin is designed to run as a [client-go credential plugin](https://kubernetes.io/docs/reference/access-authn-authz/authentication/#client-go-credential-plugins).

When you run kubectl, kubelogin opens the browser and you can log in to the provider.

Then kubelogin gets a token from the provider and kubectl access Kubernetes APIs with the token.

Take a look at the diagram:

![Diagram of the credential plugin](https://github.com/int128/kubelogin/blob/master/docs/credential-plugin-diagram.svg?raw=true)

## How to install

~~~ bash
export KUBELOGIN_VERSION="v1.21.0"

# Download the release and test the checksum
wget -O ~/kubelogin.zip "https://github.com/int128/kubelogin/releases/download/$KUBELOGIN_VERSION/kubelogin_linux_amd64.zip"
unzip ~/kubelogin.zip
rm /kubelogin.zip
mv ~/kubelogin /usr/local/bin/kubectl-oidc_login
~~~
