# timeshift-config-arch
My Archlinux timeshift setup (Because snapper gives me headaches)

## Install timeshift and utilities from the AUR

```shell
yay -S timeshift timeshift-autosnap timeshift-systemd-timer
```

## Enable systemd services
```shell
sudo systemctl daemon-reload
sudo systemctl enable timeshift-boot.timer
sudo systemctl enable timeshift-hourly.timer
```
Done
