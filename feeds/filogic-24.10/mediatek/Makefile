# Copyright (c) 2015 OpenWrt.org
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=mediatek
BOARDNAME:=MediaTek ARM
SUBTARGETS:=filogic mt7622 mt7623 mt7629
FEATURES:=dt-overlay emmc fpu gpio nand pci pcie rootfs-part separate_ramdisk squashfs usb

KERNEL_PATCHVER:=6.6

# DEVICE_TYPE:=fw3

GENERIC_BACKPORT_DIR := ${CURDIR}/backport-$(KERNEL_PATCHVER)
GENERIC_PATCH_DIR := ${CURDIR}/pending-$(KERNEL_PATCHVER)
GENERIC_HACK_DIR := ${CURDIR}/hack-$(KERNEL_PATCHVER)
GENERIC_FILES_DIR := 
GENERIC_LINUX_CONFIG:=${CURDIR}/config-$(KERNEL_PATCHVER)-mediatek

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += \
	kmod-leds-gpio kmod-gpio-button-hotplug

$(eval $(call BuildTarget))
