# PHP version switcher for OSX

If you're on OSX with PHP installed via Brew, you may be looking for an easy way to switch between PHP versions (5.3, 5.4, 5.5, 5.6, etc). Well, this package is it.

Installation:
```
curl https://raw.githubusercontent.com/sgotre/sphp-osx/master/sphp > /usr/local/bin/sphp
chmod +x /usr/local/bin/sphp
```

Add `/usr/local/bin` to your `$PATH`. If you use the Bash shell, you can do this by running this command:
```
echo 'export PATH="/usr/local/bin:$PATH"' >> $HOME/.bashrc
```
You may need to restart your shell for this to take effect.

Usage:

- `-s|-s=*` Skips apache & valet config switch for i.e

```sh
# skip apache only
sphp 5.6 -s

# skip valet only
sphp 5.6 -s=valet

# skip valet & apache
sphp 5.6 -s=valet,apache
```
- `-c=*` switch a specific config for i.e

```sh
# switch valet config only
sphp 5.6 -c=valet

# switch valet & apache config only
sphp 5.6 -c=valet,apache

# switch apache config only
sphp 5.6 -c=apache
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
* [@@biplobice](https://github.com/biplobice)