# PHP version switcher for OSX

If you're on OSX with PHP installed via Brew, you may be looking for an easy way to switch between PHP versions (5.3, 5.4, 5.5, etc). Well, this package is it.

Installation:
```
git clone git@github.com:conradkleinespel/sphp-osx.git
```

Usage:
```
./sphp-osx/sphp 53
./sphp-osx/sphp 54
./sphp-osx/sphp 55
```

For command line path, you should update the `$PATH` variable in either your `.profile`, `.zshrc`, `.bashrc` or `.bash_profile`:

```sh
# Comment out the original one
# export PATH="$(brew --prefix homebrew/php/php54)/bin:$PATH"
export PATH="/usr/local/opt/php5/bin:$PATH"
```
