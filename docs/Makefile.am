NULL =
ASCIIDOC_FLAGS = -a icons -a toc

EXTRA_DIST =					\
	meson.build				\
	spice_style.html			\
	spice_style.txt				\
	spice_threading_model.html		\
	spice_threading_model.txt		\
	vd_interfaces.txt			\
	spice_protocol.txt			\
	spice_for_newbies.txt			\
	images/newbies/g_cmd_flow.png		\
	images/newbies/g_sub.png		\
	images/newbies/cli_bsc_stc.png		\
	images/newbies/srv_stc.png		\
	images/newbies/a_cmd_flow.png		\
	$(NULL)

HTML_FILES = \
	spice_style.html \
	spice_threading_model.html \
	vd_interfaces.html \
	spice_protocol.html \
	spice_for_newbies.html \
	$(NULL)

if BUILD_MANUAL
SUBDIRS = manual

all-local: $(HTML_FILES)

%.html: %.txt
	$(AM_V_GEN) $(ASCIIDOC) -n $(ASCIIDOC_FLAGS) -o $@ $<
endif

clean-local:
	rm -f $(HTML_FILES)
