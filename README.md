# Scripts

## Script to disable auto-mounting usb drives in ubuntu

```bash
#!/bin/bash

# Create the 99-no-auto-mount.rules file
echo 'ENV{UDISKS_AUTO}="0"' | sudo tee /etc/udev/rules.d/99-no-auto-mount.rules

# Reload the udev rules
sudo udevadm control --reload-rules
```
