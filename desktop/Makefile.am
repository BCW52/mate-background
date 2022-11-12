backgrounddir = $(datadir)/backgrounds/mate/desktop

background_DATA = \
	Astronaut.jpg \
	Water-lilly.jpg \
	forest-moss.jpg \
	MATE-Stripes-Dark.png \
	forest-river-misty.jpg \
	gentoo.png \
	holy-arch.png \
	bamboo.jpg \
	linux-kernel-realistic.jpg \
	Minimal.png \
	minimal_squares.png \
	solarized-dark-sudo.jpg \
	solarized-dragon-kali.png

metadata_in_files = mate-desktop.xml.in
metadatadir = $(datadir)/mate-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)

$(metadata_DATA): $(metadata_in_files)
	$(AM_V_GEN) GETTEXTDATADIR=$(top_srcdir) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

noinst_DATA = mate-desktop.xml.in
CLEANFILES = mate-desktop.xml mate-desktop.xml.in

EXTRA_DIST = \
	$(background_DATA) \
	mate-desktop.xml.in.in \
	meson.build

mate-desktop.xml.in: mate-desktop.xml.in.in Makefile
	$(AM_V_GEN)sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/mate-desktop.xml.in.in > mate-desktop.xml.in.tmp \
	&& mv mate-desktop.xml.in.tmp mate-desktop.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in

-include $(top_srcdir)/git.mk
