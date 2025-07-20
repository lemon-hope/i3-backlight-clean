i3-backlight
=========
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)][license]

Backlight control [i3wm] using brightnessctl utility and dunstify.

## i3-backlight changelog 
* Use brightnessctl utility instead of xbacklight
* Adapt the codebase from [i3-volume](https://github.com/hastinbe/i3-volume) to [i3-backlight](https://github.com/fmorisan/i3-backlight)
* Clean source file : delete functions, varibles, etc.
* Create a minimal version of the main script by using only [dunst]   

## Installation

#### Requirements
* [i3wm]
* [brightnessctl](https://man.archlinux.org/man/brightnessctl.1.en)

#### Optional
* [notify-osd], [dunst], or any [libnotify] compatible notification daemon
* `notify-send` (provided by [libnotify]) or `dunstify` (provided by [dunst])

#### Arch Linux
To be uploaded to the AUR

#### Notifications
Notifications are provided by [libnotify]. Any [libnotify] compatible notification daemon can be used for notifications. The most common are [notify-osd] and [dunst].

If you are using [dunst], you may optionally choose to use `dunstify` instead of `notify-send` by adding the `-y` option.

Expiration time of notifications can be changed using the `-e <time_in_milliseconds>` option. Default is 1500 ms. (Ubuntu's Notify OSD and GNOME Shell both ignore the expiration parameter.)

### Guide
Clone this repository: `git clone https://github.com/lemon-hope/i3-backlight-clean`

Append the contents of the sample configuration file `i3-backlight.conf` to your i3 config, such as `~/.config/i3/config`

Reload i3 configuration by pressing `mod+Shift+r`

## Usage
* If you added the content from `i3-backlight.conf` to your i3 configuration file, you can use your keyboard backlight keys to manage (increase or decrease) your backlight level. 
* You can also run the script directly from the cli by using
    ```sh
    ./backlight -d 5  -n -y # to decrease the brightness by -5%
    ./backlight -i 5  -n -y # to increase the brightness by +5%
    ```

When notifications are enabled a popup will display the brightness level.

Example of notifications using [dunstify](https://github.com/dunst-project/dunst):  

![Brightness Notification](https://github.com/lemon-hope/i3-backlight-clean/blob/master/dunst-notification.png) 

## Special thanks
* Felipe Buiras [@fmorisan](https://github.com/fmorisan/)

## License
`i3-backlight` is released under [GNU General Public License v2][license]

Copyright (C) 1989, 1991 Free Software Foundation, Inc.

[dunst]: https://dunst-project.org
[i3wm]: https://i3wm.org
[libnotify]: https://developer.gnome.org/libnotify
[license]: https://www.gnu.org/licenses/gpl-2.0.en.html
