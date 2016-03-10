---
title: Cabal 컴파일해서 설치하기
layout: post
permalink:
published: true
categories: []
tags: []
---

## Prerequirement

- `GHC`

## Intro

우선, Cabal이라고 부르는 것은 2개의 프로그램으로 이루어져 있다. Cabal library와 cabal-install로 구성되어 있다. Cabal library는 실제로 cabal 패키지들을 관리하는 프로그램이다. cabal-install은 commandline tool이다. cabal-install을 설치하지 않아도 cabal을 사용은 가능하다. 하지만 편하게 쓰려면 설치하는 것을 권장한다. 또한 user에 설치하기 때문에, system에 설치하는 것은 옵션이 다르다.

## Sourcee code

- [공식 Github](https://github.com/haskell/cabal)
- [공식 문서](https://www.haskell.org/cabal/download.html)

둘 중에서 원하는 데서 Source Code를 가져오자.

## `Cabal`

1. `ghc -threaded --make Setup`
1. `./Setup configure --user --prefix=$HOME ----enable-library-profiling --enable-profiling`
1. `./Setup build`
1. `./Setup install`

library profiling을 설정하지 않으면 cabal-install에 `hackage-network`가 컴파일되지 않는다.

## `cabal-install`

1. `./bootstrap.sh --user --no-doc`

`--no-doc`이 없으면 `network`를 컴파일하다가 `parse error`를 만나게 된다.

## 참고

- [Github](https://github.com/haskell/cabal) README
- [Haskell Wiki](https://wiki.haskell.org/Cabal-Install#Unix)
- [Cabal Docs : user guide](https://www.haskell.org/cabal/release/cabal-latest/doc/users-guide/installing-packages.html#building-and-installing-a-user-package)