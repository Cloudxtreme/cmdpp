cmdpp
=====

## ABOUT

`cmdpp` is a command line preprocessor. It preprocesses arguments
of other command line tools.

## EXAMPLE

* copy `cmdpp.conf` to `/etc/cmdpp.conf` or `~/.cmdpp`
* install `cmdpp` to `/usr/bin`
* add the following line to your `.bashrc`: `alias find="cmdpp find"`
* run `find /var/www -static` to find all static files in you site directory

To see what actually happens, use `cmdpp -n`:

	$ cmdpp -n find /var/www/ -static -ls
	find '/var/www/' '(' '(' -iname '*.jpg' -or -iname '*.jpeg' -or -iname '*.png' ')' -or '(' -iname '*.htm' -or -iname '*.html' ')' -or -iname '*.css' ')' -ls

Patches to `cmdpp.conf` are very welcome.
