---
title: Shell에서 Command가 설치되어 있는지 확인하기
layout: post
permalink:
published: true
categories: []
tags:
  - terminal
  - shell
---

`command` 명령어는 `shell`이 프로그램을 실행하도록 하는 명령어다. 하지만 옵션을 주면 CLI에서 PATH에서 외부 프로그램을 찾을 수 있다.

## Fish

> command forces the shell to execute the program `COMMANDNAME` and ignore any functions or builtins with the same name.
>
> The following options are available:
> - `-s` or `--search` returns the name of the disk file that would be executed, or nothing if no file with the specified name could be found in the $PATH.

`command -s COMMANDNAME`의 형태로 가능하다. POSIX 호환성을 위해서 `command -v COMMANDNAME`은 `command -s COMMANDNAME`를 실행한다.

## Zsh

> The simple command argument is taken as an external command instead of a function or builtin and is executed. If the `POSIX_BUILTINS` option is set, builtins will also  be  executed but certain special properties of them are suppressed. The -p flag causes a default path to be searched instead of that in `$path`. With the `-v` flag, command is similar to `whence` and with `-V`, it is equivalent to whence `-v`.

`command -v COMMANDNAME`로 사용한다. 

## 예제

Alias를 설정할 때 사용할 수 있다.

### Fish

```shell
if command -v git > /dev/null
    abbr -a g="git"
end
```

### Zsh

```shell
if command -v git > /dev/null; then
    alias g="git"
fi
```