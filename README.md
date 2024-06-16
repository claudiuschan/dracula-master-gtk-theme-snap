Dracula snap port.

Git repo:\
[Dracula gtk theme](https://github.com/dracula/gtk) 

To connect the theme to all apps which have available plugs to gtk-common-themes you can run:

`for i in $(snap connections | grep gtk-common-themes:gtk-3-themes | awk '{print $2}'); do sudo snap connect $i dracula-gtk-theme:gtk-3-themes; done`

`for i in $(snap connections | grep gtk-common-themes:icon-themes | awk '{print $2}'); do sudo snap connect $i dracula-gtk-theme:icon-themes; done`


Based on the theme port from:\
https://gitlab.com/spider623/whitesur-snap \
https://gitlab.com/sundbp/dracula-theme-snap
