dotfiles
========

[Bork](https://github.com/mattly/bork)-based dotfile setup for Mac and Linux systems which is really simple and easy to understand.

### Features

* Dotfile wrapper based on [Bork](https://github.com/mattly/bork)
* Brew and Cask package check
* Mac App Store app check
* `npm` (Node Package Manager) package check
* `apt-get` package check
* Commented configuration options, so you know what is actually going on
* Lightweight Atom package installer which uses a bundle [Atomfile](opt/Atomfile) (and `apm` of course)
* Dotfiles per hostname

### Installation

1. Fork this repository
2. `git clone https://github.com/<GitHub-user>/dotfiles $HOME/.dotfiles`
3. `cd $HOME/.dotfiles`
4. `./dotfiles`

### Available commands

```sh
# Install/update the dotfiles
$ dotfiles

# Install/update one specific borkfile, located in borkfiles/
$ dotfiles <borkfile>
```

### Informations

Explanation of the directories:

```
./bork
└── This folder includes the bork git repository which gets updated as
    soon as you update the the dotfiles

./borkfiles
└── Includes the actual bork files, seperated to allow a condition based
    installation (system architecture, OS type)

./borkfiles/bootstrap.bork
└── This is the bootstrapping one, which applies the other Borkfiles in
    the same folder

./configs
└── Contains all of your configuration files which gets symlinked into $HOME
    as ".$FILE". So basically, your actual dotfiles (vimrc, gitconfig, etc)
```

### Credits

* [Kasperisager](https://github.com/kasperisager), for the idea with Bork
* [FRDMN](https://github.com/frdmn), for making me do this! <3

### License

[WTFPL](LICENSE)
