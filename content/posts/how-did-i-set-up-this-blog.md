---
date: 2022-02-20
draft: false
title: How did I set up this blog?
vim: spell spelllang=en_us
---

I thought it would be worthwhile to write this post and laugh at how obsolete it
is a few years away from now. This is mostly an exercise to see how much I enjoy
the process of transcribing my thoughts.

Every 15 minutes a systemd one-shot
[service](https://github.com/jupblb/nix-config/blob/20da07cfed57c86ec617d553ed38c47f5b18013a/dionysus.nix#L302)
downloads contents of this blog's [repository](https://github.com/jupblb/blog)
and builds it. The resulting source files are later served by
[Caddy](https://github.com/jupblb/nix-config/blob/20da07cfed57c86ec617d553ed38c47f5b18013a/dionysus.nix#L111).
All of this is done on my home server (the box in the bottom right):

![Photo of my home server](/images/home-server.jpg)

It runs AMD Ryzen 5 3400GE with 8GB of RAM and an NVMe drive which is good
enough for all my personal workflows. Buying a motherboard for this particular
CPU was quite tricky as model 3400 is Zen+ and 3500 is Zen 2. Both of them use
the same socket but the motherboards implementing them are not compatible.
Initially I thought this setup would be working as my home theater PC box but I
ended up using Nvidia Shield for that purpose instead.

The domain of this website is registered with OVH. I also use it with
[Migadu](https://www.migadu.com/), the email provider which I can highly
recommend. My ISP does not grant a static IP address unless a customer pays an
unfair amount of money so I wrote a small
[script](https://github.com/jupblb/nix-config/blob/20da07cfed57c86ec617d553ed38c47f5b18013a/config/script/ip-updater.sh)
that runs periodically and refreshes the DNS resolution. This does facilitate
some downtime that happens every now and then but I refuse to worry about this
considering the traffic this blog is having (which at the time of writing is
just me :smiley:).

Blogs require some content that needs to be created first. This calls for some
cozy environment! I am currently based in Wroclaw, my home city in which I've
spent most of my life (but not all of it). I work from home since February 2018
and have a dedicated space for interacting with computer(s):

![Photo of my desk setup](/images/sienkiewicza-desk.jpg)

I type in a sitting position on my [Ultimate Hacking Keyboard](https://uhk.io/).
Neovim is my word processor and I couldn't be happier with anything else,
especially after trying migrating to Emacs 6 or 7 times. It runs within
[Kitty](https://sw.kovidgoyal.net/kitty/) terminal emulator. PragmataPro pleases
my eyes but hadn't I bought it on a Black Friday sale I'd gladly roll with
Iosevka instead. I use exactly one screen with one app window per virtual
desktop to reduce distraction.

When I'm done writing I'd switch to fish shell and use git to commit and upload
all the changes to the remote repository. You can go back to the second
paragraph of this post to see what happens next. :slightly_smiling_face:
