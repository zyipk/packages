# Copyright (C) 2019 Openwrt.org
#
# This is a free software, use it under Apache Licene 2.0 & GNU General Public License v3.0.
#

include $(TOPDIR)/rules.mk

LUCI_TITLE:=qbittorrent-nox for LuCI
LUCI_DEPENDS:=+qBittorrent-Enhanced-Edition
LUCI_PKGARCH:=all

PKG_NAME:=luci-app-qbittorrent
PKG_RELEASE:=$(AUTORELEASE)

define Package/luci-app-qbittorrent/conffiles
/etc/qBittorrent/
endef

define Package/luci-app-qbittorrent/install
  chmod 0755 $(1)/etc/init.d/qBittorrent
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
