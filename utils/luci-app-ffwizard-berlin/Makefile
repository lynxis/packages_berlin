# $Id: Makefile 2010-02-04 23:25:21Z pg $

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-ffwizard-berlin
PKG_VERSION:=0.0.3
PKG_RELEASE:=4

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/luci-app-ffwizard-berlin
  SECTION:=luci
  CATEGORY:=LuCI
  SUBMENU:=3. Applications
  TITLE:=Freifunk Berlin configuration wizard
  URL:=http://pberg.freifunk.net
  DEPENDS+= +luci-base +luci-mod-admin-full +community-profiles
endef

define Package/luci-app-ffwizard-berlin/description
  Freifunk Wizard for Berlin
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/luci-app-ffwizard-berlin/install
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/controller
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/model
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/tools
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/view
	$(CP) ./luasrc/controller/* $(1)/usr/lib/lua/luci/controller
	$(CP) ./luasrc/model/* $(1)/usr/lib/lua/luci/model
	$(CP) ./luasrc/tools/* $(1)/usr/lib/lua/luci/tools
	$(CP) ./luasrc/view/* $(1)/usr/lib/lua/luci/view
	$(INSTALL_DIR) $(1)/www
	$(CP) ./htdocs/* $(1)/www
endef

$(eval $(call BuildPackage,luci-app-ffwizard-berlin))
