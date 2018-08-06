
<span style="display:block;text-align:center">
![alt text](https://2k18.balccon.org/index.php?title=File:BalCCon2k18_1.png)
</span>

# CFFTP ?

Every year @BalCC0n conference have about 30 to 40 people coming to share their knowledge. You can share too as well, share your files, movies, books, code .... We will run CFFTP, call for files or Call For FTP servers, torrents etc. Send your h5ai IP's/URL's to @BalCC0n twitter account (0 = number) or contact us https://2k18.balccon.org/index.php?title=Contact

This image allows you to run h5ai in a Docker container.

# h5ai Docker image [BalCCon2k18 CFFTP]

h5ai is a modern file indexer for HTTP web servers with focus on your files.
Directories are displayed in a appealing way and browsing them is enhanced by
different views, a breadcrumb and a tree overview. Initially h5ai was an
acronym for HTML5 Apache Index but now it supports other web servers too.

![alt text](https://cloud.githubusercontent.com/assets/776829/3098666/440f3ca6-e5ef-11e3-8979-36d2ac1a36a0.png)


# History and thanks

This repository is fork from fr3nd/docker-h5ai repository. As image was not updated for long time, I needed to update few things to make new image to work, and I just updated h5ai to v0.29.0 (original repository image run 0.28.0)

# How to run it

Just mount the directories you want to show and make sure they are accessible:

```
docker run  -p 80:80 -v /home/user/:/var/www/html/user_home:ro zerof/h5ai-balccon-docker
```

P.S. Replace /home/user with directory you want to share. This directory can have subdirectories.

Somebody will ask why there is md5 hash in options.json file? It's backdoor? Nop, just small admin panel where you can see information about your h5ai installation, and it's empty string :). To see this page on your url add: /_h5ai/public/index.php
