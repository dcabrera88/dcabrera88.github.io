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
6. Get LastPass to manage your passwords.

Note that the install locations for Emacs and Gnu Global are personal preference. They can be installed anywhere, just make sure you keep track of where things are installed.


# Configuring Environment Variables
1. Add to your PATH variable the following locations:
   1. `C:\Program Files\PuTTY\`
   2. `C:\Program Files\Git\bin\`
   3. `C:\Program Files\GnuGlobal\glo663wb\bin\`
2. Add the following environment variable `GIT_SSH` and set it to `C:\Program Files\PuTTY\plink.exe`

# Configuring Git and Github
On a git terminal configure the follwing:
1. Configure your user name like so `git config --global user.name "Your Name"`
2. Configure your email like so `git config --global user.email your@email.com`
3. Configure the editor. In this case I'm using emacs but you can use whatever you want. `git config --global core.editor "emacs -nw"`
4. Open PuTTYGen and create a public and private key. Save the private key in `C:\Users\YourUserName\.ssh\`. Add the Public Key in github under Settings->SSH and GPG keys.
5. Open Pageant and add the newly created key. You will need to open Pageant and add the key every time you start windows. (Unless you set up a script. TODO?)
6. Open PuTTY. Select an SSH connection and the option `Never` under `Close window on exit`. Try to open an SSH connection to `git@github.com`
7. You should see a message like this one:
```
Using username "git".
Authenticating with public key "Home-Github-Key-rsa-key-20190804" from agent
Server refused to allocate pty
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```
8. Done! You should now be able to push and pull from git without needing to type your username and password every time. 

# Configuring Emacs
If you aren't using emacs as your text editor you can skip this section.
Download your `.emacs` file and put it in your user folder. In windows 10 it is usually `C:\Users\<Username>\AppData\Roaming\`. If you don't have one you can either download one from [here](https://github.com/dcabrera88/emacs), you can create your own by following the instructions in [here](https://dcabrera88.github.io/emacs/) or following many of the other resources online.

# Installing jekyll and stuff
On a git terminal run the following commands:
1. gem install jekyll bundle
2. You should be able to run `jekyll -v` and have this set up.
TODO. Expand this section and setup.

Done! At least for now. Will probably need a section on each of the different tools i.e. GCC, Vivado, Python, Unreal Engine, etc that I will work on.
