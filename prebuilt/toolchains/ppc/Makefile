# Makefile

CCORI ?= bootlin
CCORI_LIST ?= internal bootlin
TOOLCHAIN  ?= $(PREBUILT_TOOLCHAINS)/$(XARCH)

ifeq ($(CCORI), internal)
  CCPRE   ?= powerpc-linux-gnu-
  CCPATH  ?= $(dir $(shell which $(CCPRE)gcc))
endif

ifeq ($(CCORI), bootlin)
  CCPRE  ?= powerpc-linux-
  CCVER  ?= 2018.11-1
  CCBASE := powerpc-e500mc--uclibc--stable-$(CCVER)
  CCPATH ?= $(TOOLCHAIN)/$(CCBASE)/bin
  CCURL  := https://toolchains.bootlin.com/downloads/releases/toolchains/powerpc-e500mc/tarballs/$(CCBASE).tar.bz2
endif
