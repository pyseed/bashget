# bashget

bash scripts lite package manager

LICENSE: MIT

## about

to add a package from github

```bash
bashget add package user [branch]
```

binaries location:

if the repo contains files like [slug] and/or [slug].sh, they are copied to $HOME/.local/bin

if the repo contains a bin directory, files of this directory are copied to $HOME/.local/bin

### features

- installed package are located in $HOME/.bashget
- add package through ssh
- other git providers are supported (like gitlab)
- dependencies support (bashget.cfg)
- custom bins support (bashget.cfg)
- update a package
- update all packages
- delete package

see more using `bashget help`

## getting started

please retrieve, install with itself, then read help

```bash
wget -O $HOME/.local/bin/bashget https://raw.githubusercontent.com/pyseed/bashget/master/bashget
chmod u+x $HOME/.local/bin/bashget
bashget add bashget pyseed
bashget help
```

## package config file

you can add a bashget.cfg inside the root of you repo

example: https://github.com/pyseed/bashget_test_package/blob/master/bashget.cfg

### dependencies

```bash
deps=( "package1@user1" "package2@user1" "package3@user2")
```

### custom bins

paths are package relative

```bash
bins=( "mydir/myscript.sh" "myscript.sh" )
```

## test package

https://github.com/pyseed/bashget_test_package