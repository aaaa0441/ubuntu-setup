# ubuntu-setup

1. [Install Zsh](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH#user-content-ubuntu-debian--derivatives)
    * `apt install zsh`
    * `chsh -s $(which zsh)`
    * Re-log in
1. Install Git `sudo apt install git`
1. Install vim `sudo apt install vim`
1. Install Yakuake: `sudo apt install yakuake`
1. [Install 'Oh My Zsh'](https://github.com/robbyrussell/oh-my-zsh#user-content-getting-started)
    * `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`
1. [Install 'Material Shell'](https://github.com/carloscuesta/materialshell#user-content-download)
    * `git clone https://github.com/carloscuesta/materialshell.git`
    * `cp materialshell/zsh/materialshell.zsh-theme ~/.oh-my-zsh/themes/`
    * Modify .zshrc to enable the theme with ZSH_THEME="materialshell".
    * Restart terminal
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
    * Copy color-scheme files for Yakuake: `cp ubuntu-setup/colorscheme/* ~/.kde/share/apps/konsole/`
