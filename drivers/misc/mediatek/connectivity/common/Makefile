subdir-ccflags-y += -Werror -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include
subdir-ccflags-y += -Werror -I$(srctree)/drivers/misc/mediatek/include/mt-plat

ifeq ($(CONFIG_MTK_CONN_LTE_IDC_SUPPORT),y)
subdir-ccflags-y += -D WMT_IDC_SUPPORT=1
else
subdir-ccflags-y += -D WMT_IDC_SUPPORT=0
endif
subdir-ccflags-y += -D MTK_WCN_WMT_STP_EXP_SYMBOL_ABSTRACT
subdir-ccflags-y += -D MTK_WCN_REMOVE_KERNEL_MODULE
ifeq ($(CONFIG_ARM64), y)
subdir-ccflags-y += -D CONFIG_MTK_WCN_ARM64
endif

ifneq ($(filter "MT6620E3",$(CONFIG_MTK_COMBO_CHIP)),)
	obj-y   +=  combo/
endif
ifneq ($(filter "MT6628",$(CONFIG_MTK_COMBO_CHIP)),)
	subdir-ccflags-y += -D MT6628
	subdir-ccflags-y += -D MERGE_INTERFACE_SUPPORT
	obj-y   +=  combo/
endif
ifneq ($(filter "MT6630",$(CONFIG_MTK_COMBO_CHIP)),)
	subdir-ccflags-y += -D MT6630
ifneq ($(CONFIG_ARCH_MT2601),y)
	subdir-ccflags-y += -D MERGE_INTERFACE_SUPPORT
endif
	obj-y   +=  combo/
endif

obj-y   +=  common_detect/
