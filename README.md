cmdpp
=====

## ABOUT

`cmdpp` is a command line preprocessor. It preprocesses arguments
of other command line tools.

Patches to `cmdpp.conf` are very welcome.

## USAGE

* Copy `cmdpp.conf` to `/etc/cmdpp.conf` or `~/.cmdpp`
* Install `cmdpp` to `/usr/bin`
* Add the following line to your `.bashrc`: `alias find="cmdpp find"`
* Run `find /var/www -static` to find all static files in you web site directory.

Use `cmdpp -n` to see what actually happens:

	$ cmdpp -n find /var/www/ -static -ls
	find '/var/www/' '(' '(' -iname '*.jpg' -or -iname '*.jpeg' -or -iname '*.png' ')' -or '(' -iname '*.htm' -or -iname '*.html' ')' -or -iname '*.css' ')' -ls
