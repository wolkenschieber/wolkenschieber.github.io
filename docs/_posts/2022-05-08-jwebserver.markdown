---
layout: post
title:  "Share a file quickly using a java web server"
date:   2022-05-08 18:45:50 +0200
categories: java share pyhton
---

# Share a file quickly using a java web server

My favorite trick to quickly share a file within a network is to go to its directory and spin up a web server.

In Python 3 that's this classic one-liner:
```shell
cd $directory && python3 -m http.server 8000
```
Anyone opening in `http://<your-machine>:8000` in their browser, will see the files of `$directory` and is able to download them.

Since JDK18, Java can do a similar trick, there the future classic one-liner is:
```shell
cd $directory && jwebserver -b 0.0.0.0
```