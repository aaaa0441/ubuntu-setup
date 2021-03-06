# ubuntu-setup

1. Install Git `sudo apt install git`
1. Install vim `sudo apt install vim`
1. [Install Zsh](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH#user-content-ubuntu-debian--derivatives)
    * `apt install zsh`
    * `chsh -s $(which zsh)`
    * Re-log in
1. [Install 'Oh My Zsh'](https://github.com/robbyrussell/oh-my-zsh#user-content-getting-started)
    * `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`
1. [Install 'Material Shell'](https://github.com/carloscuesta/materialshell#user-content-download)
    * `git clone https://github.com/carloscuesta/materialshell.git`
    * `cp materialshell/zsh/materialshell.zsh-theme ~/.oh-my-zsh/themes/`
    * Modify .zshrc to enable the theme with ZSH_THEME="materialshell".
    * Restart terminal
1. Install Yakuake: `sudo apt install yakuake`
    * Copy color-scheme files for Yakuake: `cp ubuntu-setup/colorscheme/* ~/.kde/share/apps/konsole/`
1. [Install Linuxbrew](https://github.com/Linuxbrew/brew#user-content-install-linuxbrew)
    * Install dependencies `sudo apt-get install build-essential curl file git python-setuptools ruby`
    * `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install)"`
    * `PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"`
1. Souce startup files correctly:
    * Add '.env_vars'
    ```
    # Linuxbrew
    export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"
    export MANPATH="/home/linuxbrew/.linuxbrew/share/man:$MANPATH"
    export INFOPATH="/home/linuxbrew/.linuxbrew/share/info:$INFOPATH"
    ```
    * Add to end of '~/.profile':
    ```
    # Set additional environment variables
    # Ref: http://dghubble.com/blog/posts/.bashprofile-.profile-and-.bashrc-conventions/
    source $HOME/.env_vars
    ```

### Optional Steps

1. Install graphic card driver: http://www.webupd8.org/2016/06/how-to-install-latest-nvidia-drivers-in.html
    * PPA: `https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa/`
1. Install ASUS WIFI adapter driver: [rtl8812AU_8821AU_linux](https://github.com/abperiasamy/rtl8812AU_8821AU_linux)
1. Disable specific WIFI adapter (Ref: [Ask Ubuntu](https://askubuntu.com/questions/116309/how-can-i-permanently-disable-the-internal-wifi-adapter))
    * Find out driver name: `lspci -nnk | grep -iA2 net`
    * Add `blacklist <driver-name>` to '/etc/modprobe.d/blacklist.conf'
1. [Remove guest session](http://ubuntuhandbook.org/index.php/2016/04/remove-guest-session-ubuntu-16-04/)
1. [Install Chinese input method](https://apps.ubuntu.com/cat/applications/precise/fcitx-googlepinyin/)

