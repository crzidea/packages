#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PECL_NAME:=xdebug
PECL_LONGNAME:=Xdebug extension

PKG_VERSION:=3.1.5
PKG_RELEASE:=1
PKG_HASH:=55f6ef381245da079b2fc5ce1cfbcb7961197d0c0e04f9d977613cf9aa969a79

PKG_NAME:=php8-pecl-xdebug
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Michael Heimpold <mhei@heimpold.de>

PKG_LICENSE:=Xdebug
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include ../php8/pecl.mk

CONFIGURE_ARGS+= \
	--disable-xdebug-dev \
	--without-xdebug-compression

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),,20,zend))
$(eval $(call BuildPackage,$(PKG_NAME)))
