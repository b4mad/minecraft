# B4mad Minecraft on Operate First!

This project is to run a community operated private Minecraft server to teach kids coding, operating resources and community collaboration

## Server

Connect to `minecraft.b4mad.net:31904`

## Development

To apply changes

```
kustomize build --enable-alpha-plugins manifests | oc apply -f -
```

## Secrets

If you add a new public key to [manifests/.sops.yaml](manifests/.sops.yaml) you have to re-encrypt [manifests/secrets.enc.yaml](manifests/secrets.enc.yaml)

```
cd manifests && sops updatekeys secrets.enc.yaml
```

### Resources

https://github.com/operate-first/support/issues/139
