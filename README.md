# polybar-powermenu
Powermenu module for Polybar. Provides shutdown, reboot and logout options.  

## Installation
Install ```polybar``` and [Material Icons](https://m2.material.io/)

Copy and paste this code into your ```polybar``` configuration file:

```
[module/powermenu]
type = custom/menu
expand-right = true
format-spacing = 1
label-open = %{F0198C5}%{T2}%{T-}%{F-}
label-close = %{F0198C5}%{T2}%{T-}%{F-}
label-separator = " "
label-separator-foreground = ${colors.foreground}
menu-0-0 = %{FA54242}%{T2}%{T-}%{F-}
menu-0-0-exec = menu-open-1
menu-0-1 =  %{FA54242}%{T2}%{T-}%{F-}
menu-0-1-exec = menu-open-2
menu-0-2 = %{FA54242}%{T2}%{T-}%{F-}
menu-0-2-exec = menu-open-3
menu-1-0 = "Cancel"
menu-1-0-exec = menu-open-0
menu-1-0-foreground = ${colors.foreground}
menu-1-1 = "Reboot"
menu-1-1-exec = systemctl reboot
menu-1-1-foreground = ${colors.alert}
menu-2-1 = "Power Off"
menu-2-1-exec = systemctl poweroff
menu-2-1-foreground = ${colors.alert}
menu-2-0 = "Cancel"
menu-2-0-exec = menu-open-0
menu-2-0-foreground = ${colors.foreground}
menu-3-0 = "Cancel"
menu-3-0-exec = menu-open-0
menu-3-0-foreground = ${colors.foreground}
menu-3-1 = "Logout"
menu-3-1-exec = i3-msg exit
menu-3-1-foreground = ${colors.alert}
```
Now, add the module in the ```bar``` section:
```
modules-left = powermenu #alternatively, right or center 
```
Customise the module to your needs!
