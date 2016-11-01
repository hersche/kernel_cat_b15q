# PLATFORM := $(subst ",,$(CONFIG_MTK_PLATFORM))
PLATFORM="common"

ifneq ($(wildcard $(srctree)/drivers/misc/mediatek/ext_disp/$(PLATFORM)/),)
obj-y += $(PLATFORM)/
obj-y += common/
else
obj-y += dummy/
endif
