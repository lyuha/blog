## Dvorak or Programmer Dvorak

나는 Qwerty를 쓰지 않는다. 평소에는 Dvorak을 쓰고, 개발할 일이 있으면 [Programmer Dvorak](http://www.kaufmann.no/roland/dvorak/)으로 바꾸어서 쓰고 있다. 그래서 문제가 생기는데, 보통 기본 키보드가 Qwerty로 되어 있어서 익숙하지 않다. 그래서 보통 Dvorak이나 Programmer Dvorak으로 바꾸고 작업을 한다.

## Ubuntu

```shell
sudo dpkg-reconfigure keyboard-configuration
```

명령을 치고 적당한 키보드/언어/키맵을 고르고 사용한다.

### 참고

- [Thread: change keyboard in ubuntu server](ubuntuforums.org/showthread.php?t=1818071)
- [Changing TTY keyboard layout on a server?](http://askubuntu.com/a/158895)

## Archlinux

```shell
localectl list-keymaps
localectl list-keymaps | grep -i <search_term>
find /usr/share/kbd/keymaps/ -type f
```

어떤 keymap을 있는 지 확인한다.

```shell
# persistent
localectl set-keymap --no-convert <keymap>
# temporary
loadkeys <keymap>
```

keymap을 설정한다.

### 참고

- [Keyboard configuration in console](https://wiki.archlinux.org/index.php/Keyboard_configuration_in_console)