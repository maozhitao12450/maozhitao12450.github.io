https://mirrors-i.tuna.tsinghua.edu.cn/help/postmarketOS/

官网: [[Installation/Using pmbootstrap - postmarketOS](https://wiki.postmarketos.org/wiki/Installation/Using_pmbootstrap)](https://wiki.postmarketos.org/wiki/Installation/Using_pmbootstrap)

```bash
   47  source ~/.profile

   55  git clone --depth=1 https://gitlab.com/postmarketOS/pmbootstrap.git
   56  mkdir -p ~/.local/bin
   57  ln -s "$PWD/pmbootstrap/pmbootstrap.py" ~/.local/bin/pmbootstrap
   58  pmbootstrap --version
   59  mkdir -p /home/zhitao/.local/var/pmbootstrap
   60  pmbootstrap --version
   62  ~/.local/bin/pmbootstrap init
   63  ls
   64  cd pmbootstrap/
   65  ls
   66  pmbootstrap pull
   67  PATH="$HOME/.local/bin:$PATH"
   68  pmbootstrap --mirror-pmOS=http://mirrors.tuna.tsinghua.edu.cn/postmarketOS/ --mirror-alpine=http://mirrors.tuna.tsinghua.edu.cn/alpine/ init
   69  pmbootstrap --mirror-pmOS=http://mirrors.tuna.tsinghua.edu.cn/postmarketOS/ --mirror-alpine=http://mirrors.tuna.tsinghua.edu.cn/alpine/ install
   70 pmbootstrap  --mirror-pmOS=http://mirrors.tuna.tsinghua.edu.cn/postmarketOS/ --mirror-alpine=http://mirrors.tuna.tsinghua.edu.cn/alpine/  export /mnt/d/tmp/pmbootstra
p/export 
   
```

[[Xiaomi Mi Mix 2S (xiaomi-polaris) - postmarketOS](https://wiki.postmarketos.org/wiki/Xiaomi_Mi_Mix_2S_(xiaomi-polaris)#Installation)](https://wiki.postmarketos.org/wiki/Xiaomi_Mi_Mix_2S_(xiaomi-polaris)#Installation)

```bash
zhitao@PDZL77528BJ:~$ pmbootstrap init
[11:01:23] Location of the 'work' path. Multiple chroots (native, device arch, device rootfs) will be created in there.
[11:01:23] Work path [/home/zhitao/.local/var/pmbootstrap]:
[11:01:24] NOTE: pmaports path: /home/zhitao/.local/var/pmbootstrap/cache_git/pmaports
[11:01:24] Choose the postmarketOS release channel.
[11:01:24] Available (9):
[11:01:24] * edge: Rolling release / Most devices / Occasional breakage: https://postmarketos.org/edge
[11:01:24] * v23.12: Latest release / Recommended for best stability
[11:01:24] * v23.06: Old release (unsupported)
[11:01:24] Channel [edge]:
[11:01:24] NOTE: pmaports is on master branch, copying git hooks.
[11:01:24] Choose your target device vendor (either an existing one, or a new one for porting).
[11:01:24] Available vendors (85): acer, alcatel, amazon, amediatech, apple, ark, arrow, asus, beelink, bq, clockworkpi, cubietech, cutiepi, dongshanpi, essential, fairphone, finepower, fly, generic, goclever, google, gp, hisense, htc, huawei, inet, infocus, jolla, klipad, kobo, lark, leeco, lenovo, lg, librecomputer, linksys, mangopi, medion, meizu, microsoft, mobvoi, motorola, nextbit, nobby, nokia, nvidia, odroid, oneplus, oppo, ouya, pine64, planet, pocketbook, powkiddy, purism, qemu, radxa, raspberry, realme, samsung, semc, sharp, shift, sipeed, sony, sourceparts, surftab, t2m, thundercomm, tokio, tolino, trekstor, valve, vernee, videostrong, vivo, volla, wexler, wiko, wileyfox, xiaomi, xunlong, yu, zte, zuk
[11:01:24] Vendor [xiaomi]:
[11:01:24] Available codenames (48): aries, armani, begonia, beryllium, cactus, cancro, cepheus, cereus, clover, daisy, davinci, dior, elish, equuleus, ferrari, fire, fog, gemini, ido, kenzo, laurel, lavender, libra, markw, merlin, mido, monet, natrium, olive, once, onclite, pine, platina, polaris, riva, rolex, sagit, santoni, scorpio, surya, tissot, tulip, vayu, vince, whyred, willow, wt88047, ysl
[11:01:24] Device codename [polaris]:
[11:01:24] Username [user]:
[11:01:25] Available providers for postmarketos-base-ui-wifi (2):
[11:01:25] * wpa_supplicant: Use wpa_supplicant as the WiFi backend. (default)
[11:01:25] * iwd: Use iwd as the WiFi backend (but may not work with all devices)
[11:01:25] Provider [wpa_supplicant]:
[11:01:26] Available user interfaces (22):
[11:01:26] * none: Bare minimum OS image for testing and manual customization. The "console" UI should be selected if a graphical UI is not desired.
[11:01:26] * asteroid: (Wayland) Smartwatch UI from AsteroidOS
[11:01:26] * bananui: (Wayland) Keypad controlled UI for feature phones
[11:01:26] * cage: (Wayland) Kiosk WM
[11:01:26] * console: Console environment, with no graphical/touch UI
[11:01:26] * fbkeyboard: Plain framebuffer console with touchscreen keyboard support
[11:01:26] * framebufferphone: Minimalist framebuffer menu/keyboard UI accessible via touch/volume keys & compatible scripts
[11:01:26] * gnome: (Wayland) Gnome Shell
[11:01:26] * gnome-mobile: (Wayland) Gnome Shell patched to adapt better to phones (Experimental)
[11:01:26] * i3wm: (X11) Tiling WM (keyboard required)
[11:01:26] * kodi: (GBM) 10-foot UI useful on TV's
[11:01:26] * lxqt: (X11) Lightweight Qt Desktop Environment (stylus recommended)
[11:01:26] * mate: (X11) MATE Desktop Environment, fork of GNOME2 (stylus recommended)
[11:01:26] * openbox: (X11) A highly configurable and lightweight X11 window manager (keyboard required)
[11:01:26] * phosh: (Wayland) Mobile UI initially developed for the Librem 5
[11:01:26] * plasma-desktop: (X11/Wayland) KDE Desktop Environment (works well with tablets)
[11:01:26] * plasma-mobile: (Wayland) Mobile variant of KDE Plasma (does not run without hardware acceleration)
[11:01:26] * shelli: Plain console with touchscreen gesture support
[11:01:26] * sway: (Wayland) Tiling WM, drop-in replacement for i3wm (DOES NOT RUN WITHOUT HW ACCELERATION!)
[11:01:26] * sxmo-de-dwm: Simple Mobile: Mobile environment based on SXMO and running on dwm
[11:01:26] * sxmo-de-sway: Simple Mobile: Mobile environment based on SXMO and running on sway
[11:01:26] * weston: (Wayland) Reference compositor (demo, not a phone interface)
[11:01:26] * xfce4: (X11) Lightweight desktop (stylus recommended)
[11:01:26] User interface [phosh]:
[11:01:27] Additional options: extra free space: 0 MB, boot partition size: 256 MB, parallel jobs: 9, ccache per arch: 5G, sudo timer: False, mirror: http://mirror.postmarketos.org/postmarketos/
[11:01:27] Change them? (y/n) [n]:
[11:01:31] Additional packages that will be installed to rootfs. Specify them in a comma separated list (e.g.: vim,file) or "none"
[11:01:31] Extra packages [vim]:
[11:01:32] Your host timezone: Asia/Shanghai
[11:01:32] Use this timezone instead of GMT? (y/n) [y]:
[11:01:33] Choose your preferred locale, like e.g. en_US. Only UTF-8 is supported, it gets appended automatically. Use tab-completion if needed.
[11:01:33] Locale [en_US]: UTF-8
[11:01:40] WARNING: this locale is not in the list of known valid locales.
[11:01:40] Continue? (y/n) [n]:
[11:01:46] Locale [en_US]:
[11:01:47] Device hostname (short form, e.g. 'foo') [xiaomi-polaris]:
[11:01:49] After pmaports are changed, the binary packages may be outdated. If you want to install postmarketOS without changes, reply 'n' for a faster installation.
[11:01:49] Build outdated packages during 'pmbootstrap install'? (y/n) [y]:
[11:01:51] Zap existing chroots to apply configuration? (y/n) [y]:
[11:01:55] % rm -rf /home/zhitao/.local/var/pmbootstrap/chroot_native
[11:01:55] % rm -rf /home/zhitao/.local/var/pmbootstrap/chroot_buildroot_aarch64
[11:01:55] % rm -rf /home/zhitao/.local/var/pmbootstrap/chroot_buildroot_armv7
[11:01:55] % rm -rf /home/zhitao/.local/var/pmbootstrap/chroot_rootfs_xiaomi-polaris
[11:01:56] Cleared up ~280 MB of space
[11:01:56] WARNING: The chroots and git repositories in the work dir do not get updated automatically.
[11:01:56] Run 'pmbootstrap status' once a day before working with pmbootstrap to make sure that everything is up-to-date.
[11:01:56] DONE!
```

https://developer.android.com/tools/releases/platform-tools

```bash
fastboot devices #查看手机是否连接
fastboot.exe erase  boot
fastboot.exe erase  system
fastboot.exe erase  userdata

# processo 为处理器平台 YYYYMMDD 为日期 model 为手机代号
fastboot flash boot boot.img
fastboot flash system boot.img
fastboot -S 100M flash userdata xiaomi-polaris.img
fastboot erase dtbo
fastboot reboot

```

<aside>
💡 有关Notion安装或者使用上的问题，欢迎您在底部评论区留言，一起交流~

</aside>

ssh连接手机: 

1. 打开设置, 
2. system → sercure shell → 开启
3. 查看wifi连接中的ip,ssh 即可