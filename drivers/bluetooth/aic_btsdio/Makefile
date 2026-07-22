MODULE_NAME=aic8800_btsdio

obj-$(CONFIG_AIC8800_BTSDIO_SUPPORT) = $(MODULE_NAME).o

# Directly include source objects (aic8800_btlpm.c removed, not needed on Rockchip)
$(MODULE_NAME)-y := \
	aic_bluetooth_main.o \
	rfkill.o

ccflags-y += -I$(srctree)/drivers/net/wireless/aicsemi/aic8800/sdio//bsp

CONFIG_AUTO_PM ?= n

ccflags-y += -DAIC_TRACE_INCLUDE_PATH=$(src)

ccflags-$(CONFIG_AUTO_PM) += -DCONFIG_AUTO_PM
