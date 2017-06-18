# ubuntu-setup

1. [Install Zsh](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH#user-content-ubuntu-debian--derivatives)
    * `apt install zsh`
    * `chsh -s $(which zsh)`
    * Re-log in
2. Install Git `sudo apt install git`
3. Install vim `sudo apt install vim`
4. [Install 'Oh My Zsh'](https://github.com/robbyrussell/oh-my-zsh#user-content-getting-started)
    * `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`
5. [Install 'Material Shell'](https://github.com/carloscuesta/materialshell#user-content-download)
    * `git clone https://github.com/carloscuesta/materialshell.git`
    * `cp materialshell/zsh/materialshell.zsh-theme ~/.oh-my-zsh/themes/`
    * Modify .zshrc to enable the theme with ZSH_THEME="materialshell".
    * Restart terminal
6. [Install Linuxbrew](https://github.com/Linuxbrew/brew#user-content-install-linuxbrew)
    * Install dependencies `sudo apt-get install build-essential curl file git python-setuptools ruby`
    * `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install)"`
    * `PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"`
    * `echo 'export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"' >>~/.bash_profile`
7. Install Yakuake: `sudo apt install yakuake`
8. Souce startup files correctly:
