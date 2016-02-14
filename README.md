Erlang/OTP on Alpine Linux
=====

Erlang/OTP minimal environment.

Latest version: **18.1**  
Image size: **24 MB**  
Parent: [janeczku/docker-alpine-kubernetes](https://github.com/janeczku/docker-alpine-kubernetes)

This is based on work for `msaraiva/erlang` but includes an init system for PID 1 and DNS fixes for Alpine's lack of support for `search` in `resolv.conf`.

See [Erlang/Elixir on Alpine Linux](https://github.com/msaraiva/alpine-erlang) to learn more about creating **minimal Erlang/Elixir docker images with Alpine Linux**.

The following packages are pre-installed:

- s6
- dnsmasq
- ncurses-libs
- erlang-kernel
- erlang-stdlib
- erlang-compiler
- erlang

> **Notice:** In order to keep images as compact as possible, Erlang libraries for Alpine Linux are split into many different packages. The full list of Erlang packages available can be found [here](https://pkgs.alpinelinux.org/packages?name=erlang%25&repo=all&arch=x86_64&maintainer=all)

## Usage

```
$ docker run --rm -it pmbauer/erlang erl
Erlang/OTP 18 [erts-7.1] [source] [64-bit] [smp:4:4] [async-threads:10] [kernel-poll:false]

Eshell V7.1  (abort with ^G)
1> io:fwrite("Hello, world!\n").
Hello, world!
ok
2>
```
