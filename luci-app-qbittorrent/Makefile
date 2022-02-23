# Copyright (C) 2019 Openwrt.org
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-qbittorrent
PKG_VERSION=1.0
PKG_RELEASE:=23

LUCI_TITLE:=LuCI support for qBittorrent
LUCI_PKGARCH:=all
LUCI_DEPENDS:= \
	+PACKAGE_luci-app-qbittorrent_static:qBittorrent-static \
	+PACKAGE_luci-app-qbittorrent_dynamic:qbittorrent \
	+PACKAGE_luci-app-qbittorrentEE_dynamic:qBittorrent-Enhanced-Edition

<<<<<<< HEAD
define Package/luci-app-qbittorrent/config
=======
define Package/$(PKG_NAME)/config
>>>>>>> 847c67db61fd4d31c639f5b69ce0712b8024a91b
	choice
		prompt "Build Version Selection"
		default PACKAGE_luci-app-qbittorrent_static if arm||aarch64||x86_64
		default PACKAGE_luci-app-qbittorrent_dynamic if !(arm||aarch64||x86_64)

		config PACKAGE_luci-app-qbittorrent_static
			bool "Static Build"
			depends on arm||aarch64||x86_64

		config PACKAGE_luci-app-qbittorrent_dynamic
			bool "Dynamic Build"

		config PACKAGE_luci-app-qbittorrentEE_dynamic
			bool "QBEE Dynamic Build"
			
	endchoice
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
