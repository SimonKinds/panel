The custom panel I use when running [bspwm](https://github.com/baskerville/bspwm).
Initially based on the examples from the bspwm found [here](https://github.com/baskerville/bspwm/tree/master/examples/panel) 

It's using [lemonbar](https://github.com/LemonBoy/bar) for displaying the panel.

# Getting it working
Add the directory in which the repository is located to your `$PATH` and then you may execute `panel` and you're off to the races.
The vpn script requires the user to be allowed to execute sudo commands.
I solved it by creating a vpn group, adding my user to it and then specifically enabling the systemd commands required to start and stop the vpn.
The commands will depend on your `$DEFAULT_VPN_CONFIG` set in panel_config.
In my case the lines added to the /etc/sudoers file were the following
```
%vpn ALL=NOPASSWD: /usr/bin/systemctl start openvpn-client@mullvad_singapore
%vpn ALL=NOPASSWD: /usr/bin/systemctl stop openvpn-client@mullvad_singapore
```

# Custom additions
- Dots representing workspaces
  - Green = active
  - Red = urgent
- Battery percentage via `acpi`
- Show VPN status
  - Gets toggled when clicked
