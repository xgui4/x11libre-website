---
title: XLibre - Home
layout: page
---

# X11Libre X Server — A Modern, Inclusive Xorg Fork

Xlibre is a fork of the [Xorg Xserver](https://gitlab.freedesktop.org/xorg/xserver), with 
major code cleanups and enhanced functionality aimed at modernizing the X11 server 
with a focus on **security**, **performance**, and **maintainability**.

This fork was created because problematic elements within the Xorg project, including 
influence from large corporations, were blocking substantial progress. After journalists
began covering the planned Xlibre fork on June 6th, 2025, freedesktop.org administrators
banned the Xlibre founder’s GitLab account, which led to the deletion of repositories, 
tickets, and merge requests. Xorg has also removed prior work and contributions from [@Metux](https://github.com/metux).

This is an entirely **independent project**, contributed to and maintained by a community 
of independent developers — anyone who wants to modernize, clean up, document, test, 
and advance X11 as the primary graphics and rendering system for UNIX and UNIX-like 
operating systems such as: **FreeBSD, OpenBSD, NetBSD, GNU/Linux, Illumos**, and even 
non-UNIX platforms like **Windows (via Cygwin)**.

X11 has served as the backbone of many desktop environments since its initial release 
in **1984** (as X1), including **Xfce, MATE, Trinity, Blackbox, CDE, Lumina**, and 
many others.

This project is **not affiliated with or endorsed by** the Xorg efforts of freedesktop.org, 
Red Hat, or GNOME.

We believe in equity of opportunity, openness, and community. It doesn’t matter what 
country you’re from, what your political views are, your race, gender, age, dietary 
habits, fashion style, whether you’re furry, fairy, Conan, McKay, a comic character, 
a neurodivergent person, or a small furry creature from Alpha Centauri, **you are welcome here**.
As long as you treat others with respect, you belong.This is a truly inclusive, 
community-led project where everyone gets a fair opportunity to contribute and grow.

Together we’ll make X great again by modernizing it *and* making it for everyone.

[Are we XLibre Yet?](https://gist.github.com/probonopd/301319568a554abe7426c02eb5e19b5a)

Together we’ll make X great again!

## Upgrade notice
- Module ABIs have changed - drivers MUST be recompiled against
  this Xserver version, otherwise the Xserver can crash or fail to start
  up correctly.

- If your console is locked up (no input possible, not even VT switch), then
  most likely the input driver couldn’t be loaded due to a version mismatch.
  When unsure, it’s best to be prepared to ssh into your machine from another
  one or set a timer that’s calling `chvt 1` after certain time, so you don’t
  need a cold reboot. Or, make sure that you have magic `SysRq` key enabled
  (`Alt+PrtSc`) via sysctl (`kernel.sysrq=1`), then press following combination
  depending on keyboard layout to make kernel regain control over keyboard to
  make VT switching work:
  - QWERTY/AZERTY keyboard layout: `SysRq + R`
  - Dvorak/Colemak keyboard layout: `SysRq + P`
<p></p>
- Proprietary Nvidia drivers might break: they still haven’t managed to do even
  simple cleanups to catch up with Xorg master for about a year. All attempts to
  get into direct mail contact have failed. We’re trying to work around this,
  but cannot give any guarantees. But you can make it work by adding `Option
  "IgnoreABI" "1"` line to `ServerFlags` section in Xorg config.

- Most Xorg drivers should run as-is (once recompiled!), with some exceptions.
  See `.gitlab-ci.yml` for the versions/branches built along with Xlibre.

## [Are We XLibre Yet ? by @probonopd](https://gist.github.com/probonopd/301319568a554abe7426c02eb5e19b5a#file-arewexlibreyet-md)
