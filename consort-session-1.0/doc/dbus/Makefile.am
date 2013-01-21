SPEC_XML_FILES =					\
	consort-session.xml				\
	org.consort.SessionManager.ref.xml		\
	org.consort.SessionManager.Client.ref.xml		\
	org.consort.SessionManager.ClientPrivate.ref.xml	\
	org.consort.SessionManager.Inhibitor.ref.xml	\
	org.consort.SessionManager.Presence.ref.xml

if DOCBOOK_DOCS_ENABLED

htmldocdir = $(docdir)/dbus
htmldoc_DATA = consort-session.html

consort-session.html: $(SPEC_XML_FILES)
	$(AM_V_GEN)$(XMLTO) xhtml-nochunks -m $(top_srcdir)/doc/dbus/config.xsl consort-session.xml

endif # DOCBOOK_DOCS_ENABLED

org.consort.SessionManager.ref.xml: $(top_srcdir)/consort-session/org.consort.SessionManager.xml spec-to-docbook.xsl
	$(AM_V_GEN)$(XSLTPROC) $(top_srcdir)/doc/dbus/spec-to-docbook.xsl $< | tail -n +2 > $@
org.consort.SessionManager.Client.ref.xml: $(top_srcdir)/consort-session/org.consort.SessionManager.Client.xml spec-to-docbook.xsl
	$(AM_V_GEN)$(XSLTPROC) $(top_srcdir)/doc/dbus/spec-to-docbook.xsl $< | tail -n +2 > $@
org.consort.SessionManager.ClientPrivate.ref.xml: $(top_srcdir)/consort-session/org.consort.SessionManager.ClientPrivate.xml spec-to-docbook.xsl
	$(AM_V_GEN)$(XSLTPROC) $(top_srcdir)/doc/dbus/spec-to-docbook.xsl $< | tail -n +2 > $@
org.consort.SessionManager.Inhibitor.ref.xml: $(top_srcdir)/consort-session/org.consort.SessionManager.Inhibitor.xml spec-to-docbook.xsl
	$(AM_V_GEN)$(XSLTPROC) $(top_srcdir)/doc/dbus/spec-to-docbook.xsl $< | tail -n +2 > $@
org.consort.SessionManager.Presence.ref.xml: $(top_srcdir)/consort-session/org.consort.SessionManager.Presence.xml spec-to-docbook.xsl
	$(AM_V_GEN)$(XSLTPROC) $(top_srcdir)/doc/dbus/spec-to-docbook.xsl $< | tail -n +2 > $@

BUILT_SOURCES =	\
	org.consort.SessionManager.ref.xml \
	org.consort.SessionManager.Client.ref.xml \
	org.consort.SessionManager.ClientPrivate.ref.xml \
	org.consort.SessionManager.Inhibitor.ref.xml \
	org.consort.SessionManager.Presence.ref.xml

CLEANFILES =				\
	$(BUILT_SOURCES)		\
	$(htmldoc_DATA)

EXTRA_DIST =				\
	consort-session.xml.in		\
	config.xsl			\
	docbook.css			\
	dbus-introspect-docs.dtd	\
	spec-to-docbook.xsl

-include $(top_srcdir)/git.mk
