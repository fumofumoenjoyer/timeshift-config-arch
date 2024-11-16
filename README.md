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
## Timeshift-autosnap.conf

```shell
#
# /etc/timeshift-autosnap.conf
#

# skipAutosnap defines if timeshift-autosnap execution should be skipped.
# Default value is false.
skipAutosnap=false

# deleteSnapshots defines if old snapshots should be deleted.
# Default value is true.
deleteSnapshots=true

# maxSnapshots defines how much old snapshots script should left.
# Only positive whole numbers can be used.
# Default value is 3.
maxSnapshots=30

# updateGrub defines if grub entries should be auto-generated.
# If grub-btrfs package is not installed grub won't be generated.
# Default value is true.
updateGrub=true

# snapshotDescription defines value used to distinguish snapshots created using timeshift-autosnap
# Default value is "{timeshift-autosnap} {created before upgrade}".
snapshotDescription={timeshift-autosnap} {created before upgrade}

```

Done
