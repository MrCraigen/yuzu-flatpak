# yuzu-flatpak

This is an unofficial Yuzu flatpak package.

## Setup
First you need the base org.kde.Sdk and org.kde.Platform from flathub.org.
   ```
   flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
   flatpak install flathub org.kde.Sdk//5.14
   flatpak install flathub org.kde.Platform//5.14
   ```
   
## Build / Install
1. Add buid.sh script file first
   ```
   sh buid.sh
   ```
   This will generate a new Flaptak local repo called yuzu-repo.
2. Then in other to install and run Yuzu, run the run.sh script.
   ```
   sh run.sh
   ```
   This will add the new local repo (yuzu-repo) in to flatpak and install Yuzu for you.
   
## Update
As the Flatpak json file gets the files from the Yuzu master branch you can just simply run the build.sh and run.sh again. When you run the run.sh again it will remove the old Yuzu application and install it again. 

I will keep the master branch until Yuzu team makes a stable branch to choose form.

## After build and install Yuzu flatpak
Follow the instruction on the Yuzu webbpage.
   ```
   https://yuzu-emu.org/help/quickstart/
   ```

## Note
If you get this error:

   ```
   Error: module telepathy-glib: Failed to execute child process "eu-strip" (No such file or directory)
   ```
Then you are missing elfutils on your system. So you need to install it before continue

Debian based distro (Debian, Ubuntu, Linux Mint, PopOS)
   ```
   sudo apt install elfutils
   ```
Arch based distro (Arch, Manjaro)
   ```
   sudo pacman -S elfutils
   ```
Fedora based distro
   ```
   sudo yum install elfutils
   ```
   
