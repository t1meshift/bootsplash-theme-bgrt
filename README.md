# bootsplash-theme-bgrt
Kernel Bootsplash theme for Manjaro Linux using BGRT logo

# Installation:
The package is in [AUR](https://aur.archlinux.org/packages/bootsplash-theme-bgrt/), so just run
`yaourt -S bootsplash-theme-bgrt` 

or clone this repo, build the package with `makepkg` and then install it

# After installation:
- append `bootsplash-bgrt` hook in the end of HOOKS string of `/etc/mkinitcpio.conf`
- add `bootsplash.bootfile=bootsplash-themes/bgrt/bootsplash` in kernel boot arguments
- run `sudo mkinitcpio -P`

