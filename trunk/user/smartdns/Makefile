include $(ROOTDIR)/rules.mk

PKG_NAME:=smartdns
PKG_VERSION:=Release45

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://www.github.com/pymumu/smartdns.git
PKG_SOURCE_VERSION:=9ee27e7ba2d9789b7e007410e76c06a957f85e98
PKG_MIRROR_HASH:=skip

include $(INCLUDE_DIR)/package.mk

$(eval $(call BuildPackage,smartdns))

romfs:
	$(INSTALL_DIR) $(ROMFSDIR)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/smartdns $(ROMFSDIR)/usr/bin/smartdns
	$(INSTALL_BIN) ./smartdns.sh $(ROMFSDIR)/usr/bin/smartdns.sh
	$(INSTALL_DIR) $(ROMFSDIR)/etc_ro
	$(INSTALL_DATA) ./conf/*.conf $(ROMFSDIR)/etc_ro/
