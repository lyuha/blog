---
title: Fish shell에서 환경변수 설정하기
layout: post
permalink:
published: true
categories:
tags:
---
`Fish shell`(이하 fish)에서 환경 변수를 설정하기 위해선 `set` 명령어를 쓴다. 하지만 fish 2.2.0(released July 12, 2015)에 `export`가 추가되어서 `export`로도 환경변수를 설정할 수 있다.

## 환경변수 설정하기

임시로 쓸 환경변수는 fish에 입력하면 된다. fish가 실행될 때마다 설정해야 한다면 `$HOME/.config/fish/config.fish`에 등록해야 한다.

## `set`을 이용

```shell
set --global --export <NAME> <VALUE>
set -g -x <NAME> <VALUE>
```

환경변수를 추가한다. `-g`는 `--global`의 짧은 형태고, `-x`는 `--export`랑 같다.

### `export`를 이용(Fish v2.2.0 이상)

`export`는 v2.2.0에 추가된 함수다. 다른 Shell과의 호환성을 위해서 추가했다. `functions export`를 fish에 실행해보면 내용을 볼 수 있다. 다른 shell들과 같은 형태로 쓰면 된다.

```shell
export <NAME>=<VALUE>
```

## `PATH` 설정하기

fish에서 `PATH`를 설정하는 방법에는 2가지가 있다. `$PATH`를 수정하는 것과 fish 내의 미리 정의된 변수를 변경하는 것이다.

## $PATH에 추가하기

```shell
set -x -g PATH <VALUE> $PATH
export <NAME>=<VALUE>
```

`~/.config/fish/config.fish`에 위의 코드를 추가하면 fish가 실행될 때마다 해석한다.

## `fish_user_paths` 추가하기

```shell
set -U fish_user_paths /usr/local/bin $fish_user_paths
```

위의 명령을 fish에 한번만 실행해주면 된다. 실행하면, 현재 열려있는 fish에 모두 적용된다. `fish_user_paths`는 자동으로 `$PATH`에 추가되는 변수다.

## 참고

- [Fish $PATH](http://fishshell.com/docs/current/tutorial.html#tut_path)
- [Fish 2.2.0 Release note](http://fishshell.com/release_notes.html)