# 42_remote_dev_env

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/6299392e511f431e881286679980aaa5)](https://app.codacy.com/manual/juanlamarao/42_remote_dev_env?utm_source=github.com&utm_medium=referral&utm_content=juanlamarao/42_remote_dev_env&utm_campaign=Badge_Grade_Dashboard)
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

A docker image with an environment ready to code in C :D

## How it works

This project aims to support people programming in C with an environment containing:
-   Text editors: vim, \*emacs and nano;
-   Compilers: gcc, clang and make;
-   Debugger: lldb and valgrind;
-   Version control: git;
-   There is a folder called docker\_files located at `/docker_files` which is mounted at the host machine.

\* if you use emacs (don't know why :D) change the `srcs/deploy.sh` and uncomment the `L_PKG_EMACS="emacs"` line (line 19)  

>	`comment` TO DO add an image showing a circle of how it works  
>	`comment` build image -> run a container from the image -> use docker_files folder as a bridge beteewn the container and your host machine

## How to build the image

1.  `git clone https://github.com/juanlamarao/42_remote_dev_env`
2.  Enter the `42_remote_dev_env` folder
3.  `docker build . -t remote_42_img`

## How to run the container

First change the `run_container.sh` file with your informations

### Linux || MacOS

`bash run_container.sh`

### Windows

`on progess..`

## How to execute a command at a running container

`docker exec remote_42_ctn command`

## How to stop a running container

-   Option 1: from the host's terminal  
`docker stop remote_42_ctn`

-   Option 2: from the container's terminal  
`exit`

## Removing images

`docker rmi remote_42_img debian:buster`

## It time to help :D

Fell free to help improve this environment to help others.  
You can fork to make your own, but would be better if you fork it and
submmit your changes as pull requests, and help it grow :D

### Check this _To do_

-   check permision of the docker volume at the host; (Linux OK, Mac OK, Windows FAIL)
-   improve terminal bash; (more collors and cool funcs :D) DONE
-   add pt-br language (acentos);
-   add support for graphical projects;
-   add norminette support;
-   test libft-unit\_test (not working yet, something is missing?);
-   test 42 header for emacs and vim;
