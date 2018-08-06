<p align="center">
<img src="https://2k18.balccon.org/images/1/16/BalCCon2k18_1.png" />
</p>

# CFFTP ?

Every year @BalCC0n conference bring 30 to 40 people coming to share their knowledge. You can share as well, share your files, movies, books, code .... We will run CFFTP, call for files or Call For FTP servers, torrents etc. Send your IP's/URL's to @BalCC0n twitter account (0 = number) or contact us https://2k18.balccon.org/index.php?title=Contact

If you want easy way to share your files, here you can find information about h5ai app, and how to run simple share using Docker.

# h5ai Docker image [BalCCon2k18 CFFTP]

h5ai is a modern file indexer for HTTP web servers with focus on your files.
Directories are displayed in a appealing way and browsing them is enhanced by
different views, a breadcrumb and a tree overview. Initially h5ai was an
acronym for HTML5 Apache Index but now it supports other web servers too.

![alt text](https://cloud.githubusercontent.com/assets/776829/3098666/440f3ca6-e5ef-11e3-8979-36d2ac1a36a0.png)


# History and thanks

This repository is fork from fr3nd/docker-h5ai repository. As image was not updated for long time, I needed to update Dockerfile, few things to get make this working again, and I just updated h5ai to v0.29.0 (original repository image run on v0.28.0)

# How to run it

Just mount the directories you want to show and make sure they are accessible.

On local machine make directory you want to share:

```
make /home/user/share
```

Then run:

```
docker run  -it -p 80:80 -v /home/user/share:/var/www/html/user_home:ro zerof/h5ai-balccon-docker
```

P.S. Replace /home/user/share with directory you want to share. This directory can have subdirectories.

Somebody will ask why there is md5 hash in options.json file? It's backdoor? Nop, just small admin panel where you can see information about your h5ai installation, and default MD5, it's empty string :). To see this page add this to end of your url or IP: /_h5ai/public/index.php

