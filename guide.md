# Silly guide for Debian Regolith Install

## Step 1

```sh
apt install git sudo wget gpg lightdm
```

## Step 2

```sh
wget -qO - https://regolith-desktop.org/regolith.key | gpg --dearmor | sudo tee /usr/share/keyrings/regolith-archive-keyring.gpg > /dev/null
```

## Step 3

```sh
echo deb "[arch=amd64 signed-by=/usr/share/keyrings/regolith-archive-keyring.gpg] https://regolith-desktop.org/release-3_0-debian-bookworm-amd64 bookworm main" | \
sudo tee /etc/apt/sources.list.d/regolith.list
```

## Step 4

```sh
apt update
```

## Step 5

```sh
apt install regolith-desktop regolith-session-flashback regolith-look-lascaille
```
