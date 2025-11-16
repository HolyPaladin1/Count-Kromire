# This is just a helper file for convenience, have a look at Translation-HOWTO.txt instead.
# (Typing "make" in the terminal while beeing in this directory performs miracles.)

# The rules (below) define how the language files are created.
# Left of the ":" is the file to be created.
# It will only be created if there was a change in one of the files listed right of it.

*/LC_MESSAGES/wesnoth-Kromire.po: wesnoth-Kromire.pot
	msgmerge $@ $< > tempfile.po && mv tempfile.po $@

wesnoth-Kromire.pot: ../utils/*.cfg ../scenarios/*.cfg ../_main.cfg
	wmlxgettext $+ --directory=. --domain=wesnoth-Kromire > $@

# Explanation:
# $@ means the stuff left of the ":"
# $< means the first Element after the ":"
# $+ means all Elements after the ":"
# > has nothing to do with it, after it comes the output file  
