# Onboard custom files of Japanese keyboard layout (OADG 109A Full-size Keyboard)

<img width="2400" height="600" alt="Image" src="https://github.com/user-attachments/assets/b39c2cb6-a4eb-4861-a3f4-fddee9fb2eb0" />

## :: Description ::

This is a custom layouts definition files for [Onboard](https://github.com/onboard-osk/onboard), the on-screen keyboard.
It replicates the layouts of a Japanese keyboard (compliant with OADG109A/JIS X 4064).

This file was created by copy & customizing the "Linux Mint 22.3 Zena"'s `Full Keyboard*` and `Compact*` files in `/usr/share/onboard/layouts/` directory.
You can check which parts have been modified by comparing the differences between these files.

```console:
    ## e.g.:
    $ diff layouts/OADG109A_Full_Keyboard.onboard /usr/share/onboard/layouts/Full\ Keyboard.onboard
```

You will need a Linux desktop environment with a Japanese environment setup. maybe.


## :: Installation ::

### >> for Developpers

Please clone this repository using the `git clone` command.
This will create the `layouts` directory. Place it in an XDG compliant directory.
You can install it in your home directory using the following commands:

```console:
    $ git clone https://github.com/9hnder/onboard-layout-jp.git
    $ mkdir -p ~/.local/share/onboard
    $ cp -r onboard-layout-jp/layouts  ~/.local/share/onboard/
```

The `themes` directory is optional. Use the design if you need it.
Requires `fonts-migmix` package. Or please edit `Nightshade.theme` file to an appropriate font.
Depending on the font, the glyph backslash `\` may be displayed as the JP yen sign `¥`, so we recommend using a source code fonts. e.g. `MigMix 1M`, `Migu 1M`, `Migu 1C`, `Source Code Pro` that can clearly distinguish between them.

⚠️ WARNING ⚠️  
If you have already modified `key_defs.xml`, please merge it manually.

### >> for Non-Developpers

1. Download the ZIP file from the GitHub Web UI.
2. Unzip the downloaded `onboard-layout-jp-main.zip`.
3. Move all files to the `~/.local/share/onboard/` directory.


## :: Usage ::

After installation, if Onboard is already running, close it and restart it.
Then, open the Onboard settings screen and select *[Layout] > [My Layouts] > [OADG109A_Full_Keyboard]*.

To try it from the CLI:

```console:
    $ pkill onboard
    $ onboard-settings
    -- (Set "OADG109A_Full_Keyboard" layout or Use onboard -l option) --
    $ onboard &
```

Let's do this!


## :: License ::

Following the original project, the license is as follows. Modification and redistribution are permitted as long as the license terms are adhered to.

[GPL-3+](https://www.gnu.org/licenses/gpl.txt)

The following person own the copyright only to the differences from the original.

© Ken Shirakawa (9hnder)
Since: 2026-04-18 - 2026-05-12


## :: Disclaimer ::

The author assumes no responsibility for any issues that may arise from using these settings.
Please use at your own risk.


## :: Test Environment ::

The author’s test environment is as follows.
It is a physical machine, not a virtual environment... maybe.
(Unless this world is a simulator...)

This is the result of the `neofetch` command.

    OS: Linux Mint 22.3 x86_64
    Kernel: 6.17.0-19-generic
    Shell: bash 5.2.21
    Resolution: 2400x1600
    DE: Cinnamon 6.6.7
    WM: Mutter (Muffin)
    WM Theme: Mint-Y-Dark-Red (Mint-Y)
    Theme: Mint-Y-Dark-Red [GTK2/3]
    Icons: Mint-Y-Red [GTK2/3]
    Terminal: gnome-terminal
    CPU: Intel Pentium 4415Y (4) @ 1.600GHz
    GPU: Intel HD Graphics 615

    Onboard: 1.4.1+mint4+willma (base on 1.4.1-5ubuntu6)

## :: References ::

I referred to the following web pages while creating this. Thanks a lot!

[Bochibochi Blog](https://mypace.sasapurin.com/entry/impossible-input-underscore-onboard/)

Also, if you want to change the font on the keycaps or modify the Super key label, the following page will be helpful.

[kledgeb](https://kledgeb.blogspot.com/2014/06/ubuntu-onboard-17.html)


## :: About the Author ::

Related articles are published below.

[\[Linux Mint\] Make Onboard layout compatible with OADG109 Japanese keyboard - Qiita](https://qiita.com/9hnder/items/ec6efda6a59bcd5b1c1d)

**Sorry, dear foreign friends! Only Japanese articles. DW.**


## :: Acknowledgments ::

I would like to thank the reference sites and the Onboard developers.
Thanks for the SUPER wonderful software!



<!-- vim:set ts=4 tw=0 ff=unix ft=markdown : This is vim modeline -->

