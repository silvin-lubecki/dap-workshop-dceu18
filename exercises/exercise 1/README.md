# Exercise - Setup your environment

During this exercise you will setup your environment for the workshop.
Please follow these steps:

## Create a Docker Hub account

We will need a Docker Hub account all along the workshop, to use `Play With Docker` and to push/pull images to your own repository.

**1.** If you already have a Docker Hub account, go directly to step 5
**2.** Open a browser and go to https://hub.docker.com

![hub login](dockerhub-login.png)

**3.** Sign up with a `login`, `password` and email
**4.** Check your mailbox and confirm your email

![hub confirmation](confirmation.png)

**5.** Sign in Docker Hub

![hub sign in](sign-in.png)


## Play With Docker

This workshop is tuned to be used with [Play With Docker](https://labs.play-with-docker.com), so everyone can have the same experience and we don't rely on WiFi to push/pull Giga Bytes of images.
You can still follow the instructions locally with your own engine.

**1.** Open a browser and go to https://labs.play-with-docker.com

![pwd](pwd.png)

**2.** Click on the `Login` dropdown, choose `Docker` and sign in using your `Docker Hub` credentials

![pwd sign in](pwd-login.png)

**3.** Start !

![pwd start](pwd-start.png)

**4.** A new session is opened, which will be closed in 4 hours. You can add multiple new instances and delete them. Each one has it's own engine and own prompt. You can also ssh directly to it if you feel more comfortable with your own term. Now **add a new instance**.

![pwd create instance](pwd-create-instance.png)

**5.** Login to the Docker Hub using your credentials

```sh
$ docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: dapworkshop
Password:
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
```

**6.** We prepared an image containing everything needed for the workshop (docker CLI, docker-compose, docker-app, swarm, ...) and your prefered editors (nano, emacs, even vi!). Please run it, everything will happen in this container. 

```sh
$ docker run -it -v /var/run/docker.sock:/var/run/docker.sock -v /root:/workshop dapworkshop/workshop
Unable to find image 'dapworkshop/workshop:latest' locally
latest: Pulling from dapworkshop/workshop
32802c0cfa4d: Pull complete
da1315cffa03: Pull complete
fa83472a3562: Pull complete
f85999a86bef: Pull complete
4cc80afb35c1: Pull complete
bf894faa191a: Pull complete
45a03e053592: Pull complete
864df6dd1c39: Pull complete
09ce7fe1c5dc: Pull complete
14338ab52e32: Pull complete
8675173c233b: Pull complete
e5c15956bd51: Pull complete
29ad70ea4980: Pull complete
Digest: sha256:830725944470dfe2cd7c2eb87ad49633338d8f63080ab8a0d826f2bfa1ce6d72
Status: Downloaded newer image for dapworkshop/workshop:latest
➜  /workshop
```

Now the workshop can really start!

**Don't forget to save on your laptop all your exercises before leaving the workshop**.
