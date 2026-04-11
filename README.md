# PHP version switcher for OSX

If you're on OSX with PHP installed via Brew, you may be looking for an easy way to switch between PHP versions (5.6, 7.0, 7.1, 7.2 etc). Well, this package is it.

Quick install:
```
curl -sL https://raw.githubusercontent.com/jschaedl/sphp-osx/main/sphp -o /usr/local/bin/sphp && chmod 755 /usr/local/bin/sphp
```

Or clone the repository:
```
git clone git@github.com:jschaedl/sphp-osx.git
```

Make sure `/usr/local/bin` is in your `$PATH`. If you use the Bash shell, you can do this by running:
```
echo 'export PATH="/usr/local/bin:$PATH"' >> $HOME/.bashrc
```
You may need to restart your shell for this to take effect.

Usage:
```
sphp 8.1
sphp 8.5
```

## Troubleshooting

### PHP doesn't work anymore when I switch versions in Bash

Bash has an executable path cache. It saves the paths of executables it has previously run. If Brew changes the path to the `php` executable, you may encounter
this error. You have 2 options:
- Add `set +h` in your `~/.bashrc` or `~/.profile` file. This will disable the executable path cache in Bash. However, this might slow down your Bash.
- After you use `sphp`, enter the command `hash -r` in your shell. This will clear the executable path cache only once.

## Contributors

* [@alefi87](https://github.com/alefi87)
* [@conradkleinespel](https://github.com/conradkleinespel)
* [@michaelburtonray](https://github.com/michaelburtonray)
* [@sebastienbarre](https://github.com/sebastienbarre)
* [@uzyn](https://github.com/uzyn)
* [@w00fz](https://github.com/w00fz)
* [@markcarver](https://github.com/markcarver)
* [@maztch](https://github.com/maztch)
* [@@sgotre](https://github.com/sgotre)
* [@anararo](https://github.com/anararo)
