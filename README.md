MacOS Setup
======

A fork of Thoughtbot's laptop script, personalized for different development goals. 

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Requirements
------------

Support:

* macOS Ventura (13.x) on Apple Silicon and Intel
* macOS Monterey (12.x) on Apple Silicon and Intel

Older versions may work but aren't regularly tested.
Bug reports for older versions are welcome.

Install
-------

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/thoughtbot/laptop/main/mac
```

Review the script (avoid running scripts you haven't read!):

```sh
less mac
```

Execute the downloaded script:

```sh
sh mac 2>&1 | tee ~/laptop.log
```

Optionally, review the log:

```sh
less ~/laptop.log
```

Debugging
---------

Your last run will be saved to `~/laptop.log`.
Read through it to see if you can debug the issue yourself.

What it sets up
---------------

macOS tools:

* [Homebrew] for managing operating system libraries.

[Homebrew]: http://brew.sh/

Dev tools:

* [Universal Ctags] for indexing files for vim tab completion
* [Git] for version control
* [OpenSSL] for Transport Layer Security (TLS)
* [The Silver Searcher] for finding things in files
* [Tmux] for saving project state and switching between projects
* [Zsh] as your shell
* [neovim] for terminal textx-editing/general development
* [openssh] for secure shell protocol
* [wget] for file download and easier syntax than curl
* [htop] as a loightweight terminal based task manager
* [gcc] as an alternative compiler to clang. Can be invoked with appending '-' plus the version number. Calling just 'gcc' on MacOS will use the clang compiler by default. 
* [wireshark]: for packet analysis
* [ngrok] for easy tunnelling from localhost
* [raspberry-pi-imager] for flashing sd cards and installing pi images

[Universal Ctags]: https://ctags.io/
[Git]: https://git-scm.com/
[OpenSSL]: https://www.openssl.org/
[The Silver Searcher]: https://github.com/ggreer/the_silver_searcher
[Tmux]: http://tmux.github.io/
[Zsh]: http://www.zsh.org/
[neovim]: https://github.com/neovim/neovim
[openssh]: https://github.com/openssh/openssh-portable
[wget]: https://www.gnu.org/software/wget/
[htop]: https://github.com/htop-dev/htop
[gcc]: https://gcc.gnu.org/
[wireshark]: https://gitlab.com/wireshark/wireshark
[ngrok]: https://ngrok.com/docs
[raspberry-pi-imager]: https://www.raspberrypi.com/software/

Browsing:

* [Firefox] for general browsing
* [Brave] for a (mostly) degoogled Chromium browser

[Firefox]: https://developer.mozilla.org/en-US/docs/Mozilla/Firefox
[Brave]: https://github.com/brave/brave-browser

GitHub tools:

* [GitHub CLI] for interacting with the GitHub API

[GitHub CLI]: https://cli.github.com/

Image tools:

* [ImageMagick] for cropping and resizing images

[ImageMagick]: https://github.com/ImageMagick/ImageMagick

Programming languages, package managers, and configuration:

* [asdf-vm] for managing programming language versions
* [Node.js] and [npm], for running apps and installing JavaScript packages
* [Yarn] for managing JavaScript packages
* [Rosetta 2] for running tools that are not supported in Apple silicon processors

[ImageMagick]: http://www.imagemagick.org/
[Node.js]: http://nodejs.org/
[npm]: https://www.npmjs.org/
[asdf-vm]: https://github.com/asdf-vm/asdf
[Yarn]: https://yarnpkg.com/en/
[Rosetta 2]: https://developer.apple.com/documentation/apple-silicon/about-the-rosetta-translation-environment

Databases:

* ~~[Postgres] for storing relational data~~
* ~~[Redis] for storing key-value data~~

[Postgres]: http://www.postgresql.org/
[Redis]: http://redis.io/

It should take less than 15 minutes to install (depends on your machine).

### Testing your changes

Test your changes by running the script on a fresh install of macOS.
You can use the free and open source emulator [UTM].

Tip: Make a fresh virtual machine with the installation of macOS completed and
your user created and first launch complete. Then duplicate that machine to test
the script each time on a fresh install thats ready to go.

[UTM]: https://mac.getutm.app

License
-------

Laptop is © 2011-2022 thoughtbot, inc.
It is free software,
and may be redistributed under the terms specified in the [LICENSE] file.

[LICENSE]: LICENSE