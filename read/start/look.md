---
title: Look
nav_order: 30
has_children: false
parent: 入門
---


# Look

## 參考連結

* Documentation / Getting Started / Configuration / [Looks](https://regolith-linux.org/docs/getting-started/configuration/#looks)
* Documentation / Customize / [Look](https://regolith-linux.org/docs/customize/look/)
* Documentation / Reference / [Regolith Looks](https://regolith-linux.org/docs/reference/looks/)

## 操作步驟

### 查詢指令

執行

``` sh
apt search ^regolith-look-
```

顯示

```
Sorting... Done
Full Text Search... Done
regolith-look-ayu/focal 2.9.7-1 amd64
  Ayu look

regolith-look-ayu-dark/focal 2.9.7-1 amd64
  Ayu Dark look

regolith-look-ayu-mirage/focal 2.9.7-1 amd64
  Ayu Mirage look

regolith-look-cahuella/focal 2.9.7-1 amd64
  Regolith R1.3 look

regolith-look-dracula/focal 2.9.7-1 amd64
  User contributed Dracula theme

regolith-look-gruvbox/focal,now 2.9.7-1 amd64 [installed]
  User contributed gruvbox theme

regolith-look-lascaille/focal,now 2.9.7-1 amd64 [installed,automatic]
  Default R1.4 look based on Ayu Mirage and JetBrains Mono

regolith-look-midnight/focal 2.9.7-1 amd64
  User contributed theme based on the midnight theme (https://github.com/i-mint/midnight) and qogir icons (https://github.com/vinceliuice/Qogir-icon-theme/).

regolith-look-nord/focal 2.9.7-1 amd64
  Regolith R1.2 look

regolith-look-pop-os/focal 2.9.7-1 amd64
  User contributed Pop!_OS theme

regolith-look-solarized-dark/focal 2.9.7-1 amd64
  Solarized Dark look

regolith-look-solarized-light/focal 2.9.7-1 amd64
  Solarized Light look

regolith-look-ubuntu/focal 2.9.7-1 amd64
  Ubuntu look for Ubuntu style

```

執行

``` sh
apt-cache search regolith-look
```

顯示

```
regolith-look-ayu - Ayu look
regolith-look-ayu-dark - Ayu Dark look
regolith-look-ayu-mirage - Ayu Mirage look
regolith-look-cahuella - Regolith R1.3 look
regolith-look-dracula - User contributed Dracula theme
regolith-look-gruvbox - User contributed gruvbox theme
regolith-look-lascaille - Default R1.4 look based on Ayu Mirage and JetBrains Mono
regolith-look-midnight - User contributed theme based on the midnight theme (https://github.com/i-mint/midnight) and qogir icons (https://github.com/vinceliuice/Qogir-icon-theme/).
regolith-look-nord - Regolith R1.2 look
regolith-look-pop-os - User contributed Pop!_OS theme
regolith-look-solarized-dark - Solarized Dark look
regolith-look-solarized-light - Solarized Light look
regolith-look-ubuntu - Ubuntu look for Ubuntu style
```

## 安裝

執行下面指令，安裝「[regolith-look-gruvbox](https://regolith-linux.org/docs/reference/looks/#gruvbox)」

``` sh
sudo apt-get install regolith-look-gruvbox
```

執行

``` sh
regolith-look
```

顯示

```
Usage: regolith-look <command>
Actions:
    refresh - Update the current session look based on Xresources values
    list - Display currently installed looks in the /etc/regolith/styles directory
    stage - Copy Xresource and i3 config files in the user directory
    set <look> - Write a global override file in the user dir to specify the desired look
```

執行

``` sh
regolith-look list
```

顯示

```
gruvbox
lascaille
```

執行

``` sh
regolith-look set gruvbox
```

顯示

```
Note: Regolith Xresources file /home/sam/.Xresources-regolith already exists, moved previous copy to /tmp/Xresources-regolith-1647941197.
Created /home/sam/.Xresources-regolith pointing to gruvbox.
```

執行

``` sh
regolith-look refresh
```

顯示

```
> Updating already existing 'Regolith' profile
[SUCCESS] Reinstalled Regolith GNOME Terminal version 0.1.0 for the 'Regolith' profile!
```
