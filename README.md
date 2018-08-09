<p align="center">
<img src="https://2k18.balccon.org/images/1/16/BalCCon2k18_1.png" />
</p>

# CFFTP ?

Every year @BalCC0n conference bring people wiling to share their knowledge. You can share as well, share your files, movies, books, code .... We will run CFFTP, call for files or Call For FTP servers, torrents etc. Share your IP's/URL's here: "location will be published soon"

We provide h5ai docker container build-ed by our team for this occasion. Easy run, easy go. All you need is to have PC/Server with installed docker, and you are good to go.  

# h5ai Docker image [BalCCon2k18 CFFTP]

This image allows you to run h5ai in a Docker container.

h5ai is a modern file indexer for HTTP web servers with focus on your files.
Directories are displayed in a appealing way and browsing them is enhanced by
different views, a breadcrumb and a tree overview. Initially h5ai was an
acronym for HTML5 Apache Index but now it supports other web servers too.

![alt text](https://cloud.githubusercontent.com/assets/776829/3098666/440f3ca6-e5ef-11e3-8979-36d2ac1a36a0.png)


# Security

This is part where you will learn most from CFFTP. BalCCon2k18 h5ai will provide clean files, and we ask other people sharing, to do the same. If somebody find "bad boys", we will remove their url from public list. You can scan all files online by virus total and opswat for free, for files up to 100MB+-, or if file is to big just generate file MD5 hash and check. This is occasion for some of you to learn how to test and scan files.

If you don't know how to do that, and you want to learn, come to BalCCon2k18 orga team, we will help, or just ask around.

# Thanks

This repository is fork from fr3nd/docker-h5ai repository. As image was not updated for long time, I needed to update Dockerfile, few things to get make this working again, and I just updated h5ai to v0.29.0 (original repository image run on v0.28.0)

# How to run it

Just create the directories you want to share and make sure they are accessible.

On local machine make directory you want to share:

```
mkdir /home/user/share
```

Then run:

```
docker run  -it -p 80:80 -v /home/user/share:/var/www/html/user_home:ro zerof/h5ai-balccon-docker
```

P.S. Replace /home/user/share with directory you want to share. This directory can have subdirectories.

# What is This

Somebody will ask why there is md5 hash in options.json file? It's backdoor? Nop, just small admin panel where you can see information about your h5ai installation, and default MD5, it's empty string :). To see this page add this to end of your url or IP: /_h5ai/public/index.php
