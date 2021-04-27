# bashget

bash scripts lite package manager

LICENSE: MIT

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

path are package relative

```bash
bins=( "mydir/myscript.sh" "myscript.sh" )
```

## test package

https://github.com/pyseed/bashget_test_package