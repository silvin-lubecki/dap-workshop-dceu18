# Exercise 1 - Set up your environment

> **Time**: Approximately 10 minutes

## Create a Docker Hub account

You need a Docker Hub account.

**1.** If you already have a Docker Hub account, go to **step 5**

**2.** Go to https://hub.docker.com

![hub login](dockerhub-login.png)

**3.** Sign up with a `login`, `password` and email

**4.** Check your mailbox and confirm your email

![hub confirmation](confirmation.png)

**5.** Sign in to Docker Hub

https://hub.docker.com

![hub sign in](sign-in.png)


## Set Up 'Play With Docker'

This workshop uses [Play With Docker](https://labs.play-with-docker.com), so everyone can have the same experience and we don't rely on WiFi to push/pull Gigabytes of images.
You can still follow the instructions locally with your own engine.

**Don't forget to save on your laptop all your exercises before leaving the workshop**.

**1.** Go to https://labs.play-with-docker.com

![pwd](pwd.png)

**2.** Click on the `Login` dropdown, choose `Docker` and sign in using your `Docker Hub` credentials

![pwd sign in](pwd-login.png)

**3.** Start !

![pwd start](pwd-start.png)

**4.** A new session is opened, which will be closed in 4 hours. You can add multiple new instances and delete them. Each one has it's own engine and own prompt. You can also ssh directly to it if you feel more comfortable with your own terminal. Now **add a new instance**.

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

**6.** Run the workshop image.

We prepared an image containing everything needed for the workshop (docker CLI, docker-compose, docker-app, swarm, ...) and your prefered editors (nano, emacs, even vi!). Please run it, everything will happen in this container. 

```sh
$ docker run -it -v /var/run/docker.sock:/var/run/docker.sock -v /root/workshop:/workshop --network host dapworkshop/workshop
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

## How to save your work

**You may want to set a reminder to save your exercises locally before leaving the workshop. We will remind you at the end as well.**.

For those using PWD, you can copy/paste the `SSH` address and use it to `SCP` (Secure File Copy through SSH) all your files:

![ssh](ssh.png)

```sh
# run this locally
$ scp -rp ip172-18-0-23-bg01fj0v0j3g00d0atfg@direct.labs.play-with-docker.com:/root/workshop .
```
