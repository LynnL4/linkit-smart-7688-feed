#
# Copyright (C) 2015 John Crispin <blogic@openwrt.org>
#
# This is free software, licensed under the GPL 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mtk-linkit-webui
PKG_VERSION:=2015-07-07
PKG_RELEASE=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/MediaTek-Labs/linkit-smart-7688-webUI.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=3676d579f7fc56dd9b07f2f75233acfbced7f032
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/mtk-linkit-webui
  TITLE:=LinkIt Smart 76x8 Webui
  DEPENDS:=@(TARGET_ramips_mt7688_LinkIt7688||TARGET_ramips_mt7628_Seeed-MT7628)
endef

define Build/Configure
	true
endef

define Build/Compile
	true
endef

define Package/mtk-linkit-webui/install
	$(INSTALL_DIR) $(1)/www/build
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/build/* $(1)/www/build/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/zh-*.html $(1)/www/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/index.html $(1)/www/index_76x8.html
endef

$(eval $(call BuildPackage,mtk-linkit-webui))
