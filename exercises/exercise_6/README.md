# Exercise - Share your application

With this exercise you will learn how to share your application.

Using the commands `push` and `pull`, you can share your bundle on any public or private registry.

`docker-app` will create a manifest and push the `bundle.json` with it. It will also push the invocation image and reference it from the manifest. This is a totally valid way to create an image, compatible with the OCI reference, and then with all the registries (`docker hub`, `docker registry` or the enterprise `docker trust registry`).

## `push` and `pull`

```sh
$ docker-app push --help

Usage:  docker-app push [<app-name>] [flags]

Push the application to a registry

Options:
      --insecure           Use insecure registry, without SSL
      --namespace string   Namespace to use (default: namespace in metadata)
      --repo string        Name of the remote repository (default: <app-name>.dockerapp)
  -t, --tag string         Tag to use (default: version in metadata)
```
**NOTE** about the namespace: it is defined as a registry hostname+ the organisation or the user.
* `--namespace=localhost:5000/myuser` to target a registry run locally
* `--namespace=my.private.registry/myteam` to target a remote registry
* `--namespace=myteam` to target the DockerHub



## inspect

## install

## Summary
