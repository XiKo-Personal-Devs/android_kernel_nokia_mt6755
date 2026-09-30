# In case the platform does NOT support this type of sensors
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sensors-1.0/hwmon/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sensors-1.0/accelerometer/inc
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sensors-1.0/magnetometer/inc
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sensors-1.0/include
obj-y   +=  mag.o
obj-y   +=  mag_factory.o

obj-$(CONFIG_MTK_MAGHUB)        +=  maghub/
obj-$(CONFIG_MTK_AKM09911)         +=  akm09911/
obj-$(CONFIG_MTK_AKM8963)	+=  akm8963/
obj-$(CONFIG_MTK_BMC156_MAG)	+=  bmc156_mag/
obj-$(CONFIG_MTK_MMC3416X_NEW)	+=  mmc3416x-new/
obj-$(CONFIG_MTK_AKM8963_NEW_OPPO)	+= akm8963-new_oppo/