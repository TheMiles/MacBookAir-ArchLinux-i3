[Previous Page](/Install-p1.md) - [Next Page](/Install-p3.md)

# Part II - Post Base System Install - GUI Setup</h1>

1. Install Wayland 

    ```Shell
    $ sudo pacman -Syu gnome gnome-extra wayland wayland-utils xorg-xwayland libinput xf86-input-libinput gdm
    $ sudo systemctl enable gdm
    $ sudo systemctl start gdm
    ```

2. Install a few extas

    ```Shell
    $ sudo pacman -Syu cpio firefox vlc htop fzf zoxide less neovim mesa tmux zsh zsh-completions zsh-autosuggestions zsh-syntax-highlighting code playerctl dmidecode  pacman-contrib eza bat ripgrep btop
    ```

3.  WM & system customization

    ```Shell
    $ mkdir Projects

    $ cd Projects
    
    $ git clone https://aur.archlinux.org/paru.git
    
    $ cd paru 
    
    $ makepkg -si PKGBUILD 
    
    $ paru -S noto-fonts ttf-material-icons-git termsyn-powerline-font-git ttf-font-awesome zramd
    
    $ sudo systemctl enable --now zramd.service 
    ```
    
4.  Console customization

    ```shell
    $ chsh -s /bin/zsh
    
    $ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    
    $ curl -Lks https://raw.github.com/themiles/dotfiles/master/update.sh | bash
    ```


[Previous Page](//Install-p1.md) - [Next Page](/Install-p3.md)