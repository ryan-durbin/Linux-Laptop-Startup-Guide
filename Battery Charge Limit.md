To set the battery charge limit and enable this charging limit on boot:

1: Open the battery service file

```sudo nano /etc/systemd/system/set-battery-limit.service```

2: save this code inside the file you just opened
```
[Unit]
Description=Set ASUS Battery Charge Limit to 80%
After=multi-user.target
StartLimitBurst=0

[Service]
Type=oneshot
Restart=on-failure
ExecStart=/bin/bash -c 'echo 80 > /sys/class/power_supply/BAT0/charge_control_end_threshold'

[Install]
WantedBy=multi-user.target
```

3: run this commend to enable the new service on boot

```sudo systemctl enable --now set-battery-limit.service```
