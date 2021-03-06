#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2015 Alexander Pyhalov
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= libass
COMPONENT_VERSION= 0.13.4
COMPONENT_REVISION= 1
COMPONENT_FMRI = library/video/libass
COMPONENT_SUMMARY= Portable renderer for the ASS/SSA (Substation Alpha) subtitle format
COMPONENT_CLASSIFICATION = System/Multimedia Libraries
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= \
  sha256:6711469df5fcc47d06e92f7383dcebcf1282591002d2356057997e8936840792
COMPONENT_ARCHIVE_URL= \
  https://github.com/libass/libass/releases/download/$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_PROJECT_URL = https://github.com/libass/libass
COMPONENT_LICENSE = ISC
COMPONENT_LICENSE_FILE = COPYING

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

CONFIGURE_OPTIONS += --disable-asm
CONFIGURE_OPTIONS += --disable-static

build: $(BUILD_32_and_64)

install: $(INSTALL_32_and_64)

# Auto-generated dependencies
REQUIRED_PACKAGES += library/c++/harfbuzz
REQUIRED_PACKAGES += library/fribidi
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/fontconfig
REQUIRED_PACKAGES += system/library/freetype-2
REQUIRED_PACKAGES += system/library/math
