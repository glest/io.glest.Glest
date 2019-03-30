Glest Flatpak Repo Creator.
=================================

Generate all the files to create a Flatpak release of Glest.

More about flatpak: https://flatpak.org/
Flatpak project: https://github.com/flatpak

## Install Glest Using Flatpak

1. Install Flatpak for your linux distribution: https://flatpak.org/setup/ (with flathub).
2. Download **Glest.flatpak** from https://drive.google.com/file/d/1cJ1sqFeZqyWHSXkmZrjXYMvn4rFYX9Hj/view?usp=sharing
3. Install by double-clicking on **Glest.flatpak** to install using your graphical package manager, or run `flatpak install Glest.flatpak` in the terminal.
4. Run Glest from your menu, or in the terminal run `flatpak run io.glest.Glest`

Note: amd64/x86_64 linux required.

## Build Glest Using Flatpak

1. Install Flatpak for your Linux distribution: https://flatpak.org/setup/
2. Install the freedesktop tools: `flatpak install flathub org.freedesktop.Platform//18.08 org.freedesktop.Sdk//18.08`.
3. Clone this git repo: `git clone --recursive https://github.com/glest/io.glest.Glest.git`. It is important to use the `--recursive` flag when cloning.
4. Inside the repo, run this command `flatpak-builder --repo=Glest --force-clean Glest-build io.glest.Glest.json`. This will build the repo and save it into the folder `Glest`.
5. Build the Glest package by running `flatpak build-bundle Glest Glest.flatpak io.glest.Glest`. This will create the package Glest.flatpak.
6. Install Glest using the instructions above.
