###########################################################################
##
## File:        ext/Makefile.am
## Versions:    $Id: 5904800a48603e33ef5aea73b962890cc16666e5 $
## Created:     2002/06/14
##
###########################################################################


AUTOMAKE_OPTIONS=foreign dejagnu no-installinfo

EXTRA_scripts = add.ext mkroot

install-data-local : $(EXTRA_scripts)
	$(mkinstalldirs) $(DESTDIR)$(prefix)/bin
	@list='$(EXTRA_scripts)'; for p in $$list; do \
	  if test -f $$p \
	  ; then \
	   echo " $(INSTALL_PROGRAM_ENV) $(INSTALL_PROGRAM) $$p $(DESTDIR)$(prefix)/bin/$$p"; \
	   $(INSTALL_PROGRAM_ENV) $(INSTALL_PROGRAM) $$p $(DESTDIR)$(prefix)/bin/$$p; \
	  else :; fi; \
	done

uninstall-local :
	@list='$(EXTRA_scripts)'; for p in $$list; do \
	  echo " rm -f $(DESTDIR)$(prefix)/bin/$$p"; \
	  rm -f $(DESTDIR)$(prefix)/bin/$$p; \
	done

check :

clean :
