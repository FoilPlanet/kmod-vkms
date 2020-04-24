#
# virtual kms driver
#
# SPDX-License-Identifier: GPL-2.0-only
#
vkms-y := vkms_drv.o vkms_plane.o vkms_output.o vkms_crtc.o vkms_gem.o vkms_composer.o

obj-m += vkms.o

KERNEL_SRC ?= /lib/modules/$(shell uname -r)/build

all:
	$(MAKE) -C $(KERNEL_SRC) V=0 M=$$PWD

install:
	cp vkms.ko $(DESTDIR)/

clean:
	@rm -rf deps.h *.o *.ko *.mod.c *.symvers *.order .*.cmd
	@rm -rf .tmp_versions .cache.mk *.o.ur-safe
