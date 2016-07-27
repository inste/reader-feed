#
# Copyright (C) 2010-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=reader
PKG_VERSION:=master
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_SOURCE_URL:=git@github.com:inste/reader.git

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=0

include $(INCLUDE_DIR)/package.mk

define Package/reader
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Serial temperature reader daemon
endef

define Package/reader/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/reader $(1)/usr/bin/reader
endef

$(eval $(call BuildPackage,reader))
