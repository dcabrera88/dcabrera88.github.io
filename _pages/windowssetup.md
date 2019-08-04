---
permalink: /windowssetup/
title: "Windows Setup"
excerpt: "Setting up in windows"
last_modified_at: 2019-07-13T11:57:09-06:00
---

# Intalling necessary software

This setup assumes a clean Windows install.

1. Go to [ninite.com](https://git-scm.com) and install Chrome, 7-Zip, Foxit Reader, WinDirStat, WinSCP, Putty, Notepad++ and whatever else you might need.
2. Go to [git-scm.com](https://git-scm.com) and download Git for Windows.
3. Download emacs from [here](https://www.gnu.org/software/emacs/download.html) and install it in `C:\Program Files\Emacs\emacs-xx.x\`
4. Get GnuGlobal from [here](https://www.gnu.org/software/global/download.html) and install it in `C:\Program Files\GnuGlobal\gloXXXwb\`
5. Get the ruby dev kit from [here](https://rubyinstaller.org/downloads/).

Note that the install locations for Emacs and Gnu Global are personal preference. They can be installed anywhere, just make sure you keep track of where things are installed.


# Configuring Environment Variables
1. Add to your PATH variable the following locations:
   1. `C:\Program Files\PuTTY\`
   2. `C:\Git\bin\`
   3. `C:\Program Files\GnuGlobal\glo663wb\bin\`
2. Add the following environment variable `GIT_SSH` and set it to `C:\Program Files\PuTTY\plink.exe`

# Configuring Git
On a git terminal configure the follwing:
1. Configure your user name like so `git config --global user.name "Your Name"`
2. Configure your email like so `git config --global user.email your@email.com`
3. Configure the editor. In this case I'm using emacs but you can use whatever you want. `git config --global core.editor "emacs -nw"`

# Configuring Emacs
Download your .emacs file and put it in your user folder. TBD TODO

# Installing jekyll and stuff
TODO
