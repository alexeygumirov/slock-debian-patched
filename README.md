# Suckless Slock with Debian patches

> **Attention**: This is `slock` v1.4 with Debian patches applied. It works correctly on Debian, Ubuntu and most probably other forks of Debian. But it **DOES NOT** work on Arch and its forks. And I have not tested it on other distros.

I am using Ubuntu on my work PC and I use [Suckless `slock`](https://tools.suckless.org/slock/).

And I can install **suckless-tools** package using **apt** from Ubuntu repositories but this `slock` binary comes with default configuration and you cannot change it.
I wanted to use `slock` with different background color, and with couple more patches from the Suckless web site.

But when I cloned [slock Git repo](https://git.suckless.org/slock) and applied all patches, it did not work.
Just simply compiled `slock` does not unlock computer.

I looked into Debian **suckless-tool** sources and found that Debian version is modified with additional patches which remove unused dependcies and allowing `slock` to work with PAM, therefore correctly unlock system.

Source files with Debian patches are downloaded here: [http://archive.ubuntu.com/ubuntu/pool/universe/s/suckless-tools/suckless-tools_44-1.debian.tar.xz](http://archive.ubuntu.com/ubuntu/pool/universe/s/suckless-tools/suckless-tools_44-1.debian.tar.xz).

> **Important**: You don't need to patch this source with Debian patches, they are already applied by me.
But for the sake of reference, all applied Debian patches are put in the `deb-patches/` subfolder, hence you can check if I applied patches correctly. 😉

## Patching with Suckless patches

This source code can be patched with all [patches from suckless.org](https://tools.suckless.org/slock/patches/) but most of them shall be applied manually because `slock.c` and `config.mk` here differ from the original.
