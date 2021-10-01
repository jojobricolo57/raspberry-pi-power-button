
# Raspberry Pi Power Button - Wake/Power Off/Restart(Double Press)

## Information

When Raspberry Pi is powered off, shortening GPIO3 (Pin 5) to ground will wake the Raspberry Pi.

This script will use pin GPIO3(5), Ground(6) with momentary button.

![gpio layout](https://github.com/fire1ce/raspberry-pi-power-button/raw/main/gpio_layout.jpg)

## Requirements

* python3-gpiozero

Can be install via apt

```bash
sudo apt install python3-gpiozero
```

## Install

This will install the script as `service` and it will run at boot

```bash
curl https://raw.githubusercontent.com/fire1ce/raspberry-pi-power-button/main/install.sh | bash
```

## Uninstall

```bash
curl https://raw.githubusercontent.com/fire1ce/raspberry-pi-power-button/main/uninstall.sh | bash
```

## Default Behavior

| __Button Press When Pi is On__      | __Description__ |
| ----------------------------------- | --------------- |
| Single                              | Nothing         |
| Double                              | Reboot          |
| Long and releases (Above 3 seconds) | Power off       |

| __Button Press When Pi is off__ | __Description__            |
| ------------------------------- | -------------------------- |
| Single                          | Powers on the Raspberry Pi |

## Check if service is running

```bash
sudo systemctl status power_button.service
```
