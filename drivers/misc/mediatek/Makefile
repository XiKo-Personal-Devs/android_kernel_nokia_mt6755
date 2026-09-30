#
# Copyright (C) 2015 MediaTek Inc.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#

#$(call all-subdir-src-or-makefile)
MTK_PLATFORM := $(subst ",,$(CONFIG_MTK_PLATFORM))
subdir-ccflags-y += -Werror
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat
subdir-ccflags-y += -I$(srctree)/drivers/mmc/host/mediatek/$(MTK_PLATFORM)

# ifdef  VENDOR_EDIT
# xiang.fei@Multimedia, 2015/10/16, Add for audio*/
# ifneq ($(filter "oppo6750_15127" "oppo6750_16011" "oppo6750_15129",$(CONFIG_ARCH_MTK_PROJECT)),)
KBUILD_CFLAGS +=   -DOPPO_MTK_MT6750_PROJECT
KBUILD_CPPFLAGS += -DOPPO_MTK_MT6750_PROJECT
CFLAGS_KERNEL +=  -DOPPO_MTK_MT6750_PROJECT
CFLAGS_MODULE +=  -DOPPO_MTK_MT6750_PROJECT
# endif
# endif  

# ifdef  VENDOR_EDIT
# yuanyan@Multimedia, 2016/02/23, add for 15131
# ifneq ($(filter "oppo6750_15131",$(CONFIG_ARCH_MTK_PROJECT)),)
KBUILD_CFLAGS +=   -DOPPO_MTK_15131_PROJECT
KBUILD_CPPFLAGS += -DOPPO_MTK_15131_PROJECT
CFLAGS_KERNEL +=  -DOPPO_MTK_15131_PROJECT
CFLAGS_MODULE +=  -DOPPO_MTK_15131_PROJECT
# endif
# endif

# ifdef  VENDOR_EDIT
# Jianfeng.Qiu@Swdp.Multimedia, 2016/04/18, Modify for 16021
# ifneq ($(filter "oppo6750_16021",$(CONFIG_ARCH_MTK_PROJECT)),)
KBUILD_CFLAGS +=   -DOPPO_MTK_16021_PROJECT
KBUILD_CPPFLAGS += -DOPPO_MTK_16021_PROJECT
CFLAGS_KERNEL +=  -DOPPO_MTK_16021_PROJECT
CFLAGS_MODULE +=  -DOPPO_MTK_16021_PROJECT
# endif

# ifdef VENDOR_EDIT//wanghao@BSP.TP
obj-y += oppo_devices_list/
# endif
# ifdef VENDOR_EDIT//yixue.ge@bsp.drv add for oppo project
obj-y += oppo_project/
obj-y += oppo_custom/
# endif

#i fdef VENDOR_EDIT
# //jie.cheng@swdh.sh, 2016/04/15, Add hypnus helper
obj-y     +=  oppo_hypnus/
# endif /* VENDOR_EDIT */

# ifdef VENDOR_EDIT
# Yixue.ge@BSP.drv, 2016/01/21, Add for support oppo dev info
obj-$(CONFIG_OPPO_DEVICE_IFNO) += oppo_devinfo/
# endif

# ifdef VENDOR_EDIT
# yongzhi.zhang@Multimedia, 2016/04/28, add for criticallog in kernel
obj-y     +=  oppo_criticallog/
#endif

# Haitao.Zhou@Prd.BaseDrv, 2015/10/28, Add for FPC normal world driver start
# ifeq ($(CONFIG_FINGERPRINT_SUPPORT),y)
obj-y += fpc/
# endif
# Haitao.Zhou@Prd.BaseDrv, 2015/10/28, Add for FPC normal world driver end


obj-$(CONFIG_MTK_EMI_MPU)	+= emi_mpu/
obj-$(CONFIG_MTK_DCS) += mtkdcs/
obj-$(CONFIG_MTK_BASE_POWER) += base/
obj-$(CONFIG_MTK_POWER_GS) += power_gs/
obj-$(CONFIG_MEDIATEK_SOLUTION)	+= sched/
obj-$(CONFIG_MEDIATEK_SOLUTION) += mach/
obj-$(CONFIG_MTK_GPT_COMMON) += gpt/
obj-$(CONFIG_MTK_SERIAL)	+= uart/
obj-$(CONFIG_MTK_IRQ) += irq/
obj-$(CONFIG_MTK_SYS_CIRQ) += cirq/
obj-$(CONFIG_MTK_GIC_EXT) += ext_gic/
obj-$(CONFIG_MTK_ICE_DEBUG) +=ice_debug/
obj-$(CONFIG_MTK_NFC) += nfc/
obj-$(CONFIG_ST_NFC) += nfc/

obj-$(CONFIG_MMPROFILE) += mmp/
obj-$(CONFIG_MTK_AUXADC)	+= auxadc/
obj-$(CONFIG_MTK_M4U)	+= m4u/
obj-$(CONFIG_MTK_GPT_SCHEME_SUPPORT)	+= partition/
obj-$(CONFIG_MTK_SYSENV)	+= sysenv/
obj-$(CONFIG_MTK_PWM)	    += pwm/
obj-$(CONFIG_MTK_CAM_CAL) += cam_cal/src/
obj-$(CONFIG_MTK_SENSORS_1_0) += sensors-1.0/
#obj-$(CONFIG_MTK_HALL_SWITCH) += hall-switch/
obj-$(CONFIG_MTK_HALL_SENSOR) += hallsensor/
obj-$(CONFIG_MTPROF)	+= mtprof/
ifeq ($(CONFIG_MTK_I2C_EXTENSION),y)
obj-$(CONFIG_MTK_I2C)  += i2c/
endif
obj-$(CONFIG_MTK_LEDS)	+= leds/
obj-$(CONFIG_CUSTOM_KERNEL_CHARGEPUMP) += chargepump/
obj-$(CONFIG_MTK_VIBRATOR)	+= vibrator/
obj-$(CONFIG_MTK_ACCDET)	+= accdet/
obj-$(CONFIG_MTK_ECCCI_C2K) += c2k_usb/
obj-y += irtx/
obj-$(CONFIG_MTK_IR_LEARNING_SUPPORT) += ir_learning/
obj-$(CONFIG_MTK_VIDEOCODEC_DRIVER) += videocodec/
obj-$(CONFIG_MTK_JPEG)	+= jpeg/
obj-$(CONFIG_MTK_RTC)	+= rtc/
obj-$(CONFIG_MTK_PMIC)	+= power/
obj-$(CONFIG_MTK_PMIC_NEW_ARCH)	+= pmic/
obj-$(CONFIG_MTK_PMIC_WRAP) += pmic_wrap/
obj-$(CONFIG_USB_MTK_HDRC) += usb20/
obj-$(CONFIG_MTK_USBFSH) += usb11/
obj-$(CONFIG_MU3_PHY)	+= mu3phy/
obj-$(CONFIG_USB_MU3D_DRV)	+= mu3d/
obj-$(CONFIG_SSUSB_DRV) += ssusb/
obj-$(CONFIG_USB_XHCI_MTK)	+= xhci/
obj-$(CONFIG_USB_C_SWITCH)	+= usb_c/
obj-$(CONFIG_MTK_GPIO) += gpio/
obj-$(CONFIG_SECURITY_SELINUX)	+= selinux_warning/
obj-$(CONFIG_MTK_MEM) += mem/
obj-$(CONFIG_MTK_MEMORY_LOWPOWER) += memory-lowpower/
obj-$(CONFIG_MTK_CMDQ) += cmdq/
obj-$(CONFIG_MTK_CMDQ) += mdp/
obj-$(CONFIG_MTK_BOOT) += boot/
obj-$(CONFIG_MTK_BOOT_REASON) += boot_reason/
obj-$(CONFIG_MTK_CHIP) += chip/
obj-$(CONFIG_MTK_DEVAPC_DRIVER) += devapc/
obj-$(CONFIG_MTK_DEVINFO_DRIVER) += devinfo/
obj-$(CONFIG_MTK_DEVINFO_DRIVER_V2) += devinfo/
obj-$(CONFIG_MTK_LCM) += lcm/
obj-$(CONFIG_MTK_LCM) += ext_disp/
obj-$(CONFIG_MTK_HDMI_SUPPORT) += hdmi/
obj-$(CONFIG_MTK_FB) += video/
obj-$(CONFIG_MTK_GPU_SUPPORT) += gpu/
obj-$(CONFIG_MTK_SMI_EXT)	+= smi/
obj-$(CONFIG_MTK_CQDMA) += cqdma/
obj-$(CONFIG_MTK_DRAMC) += dramc/
obj-$(CONFIG_MTK_SYNC) += sync/
obj-$(CONFIG_MTK_FREQ_HOPPING) += freqhopping/
obj-$(CONFIG_MTK_SECURITY_SW_SUPPORT) +=masp/
obj-$(CONFIG_MEDIATEK_SOLUTION)  += sched/
obj-y += cameraisp/src/
ifneq ($(CONFIG_MTK_IMGSENSOR),)
obj-y+= imgsensor/src/
endif
obj-$(CONFIG_MTK_LENS)   += lens/
obj-$(CONFIG_MTK_FLASHLIGHT)	+= flashlight/src/
obj-$(CONFIG_RT_FLASHLIGHT)	+= flashlight/richtek/
ifneq ($(wildcard $(srctree)/drivers/misc/mediatek/met_drv/),)
obj-y += met_drv/
endif
obj-$(CONFIG_MTK_CCCI_DEVICES)	+=  ccci_util/
obj-$(CONFIG_MTK_NET_CCMNI) +=  ccmni/
obj-$(CONFIG_MTK_CCCI_EXT)     +=  dual_ccci/
obj-$(CONFIG_MTK_ECCCI_DRIVER) += c2k_ccci/
obj-$(CONFIG_MTK_ECCCI_DRIVER) +=  eccci/

ifdef CONFIG_CUSTOM_KERNEL_SSW
ifneq ($(strip $(CONFIG_CUSTOM_KERNEL_SSW)),"")
obj-y	+= ssw/
endif
endif

obj-$(CONFIG_MTK_COMBO) += connectivity/
obj-$(CONFIG_MTK_BTIF) += btif/
obj-$(CONFIG_MTK_CONN_MD) += conn_md/

obj-$(CONFIG_MTK_IN_HOUSE_TEE_SUPPORT) += gcpu/
obj-$(CONFIG_TRUSTONIC_TEE_SUPPORT) += gcpu/
ifeq ($(CONFIG_HAVE_MTK_IN_HOUSE_TEE_SUPPORT),y)
obj-$(CONFIG_TRUSTY) += gcpu/
endif
obj-$(CONFIG_TRUSTONIC_TEE_SUPPORT) += gud/
obj-$(CONFIG_MTK_TRUSTED_MEMORY_SUBSYSTEM) += trusted_mem/
obj-$(CONFIG_MICROTRUST_TEE_SUPPORT) += teei/
obj-$(CONFIG_MTK_DEBUG_LATCH)	+= debug_latch/
obj-$(CONFIG_MTK_DEBUG_TRACER)	+= debug_tracer/
obj-$(CONFIG_MTK_WATCHPOINT) += watchpoint/
obj-$(CONFIG_MTK_SYSTRACKER)   += systracker/
obj-$(CONFIG_MTK_RAM_CONSOLE)	+= ram_console/
obj-$(CONFIG_MTK_DRAM_LOG_STORE)	+= log_store/
obj-$(CONFIG_MTK_USE_RESERVED_EXT_MEM) += exm/
obj-$(CONFIG_RT_REGMAP) += rt-regmap/

obj-$(CONFIG_MTK_SVP) += memory-ssvp/
obj-$(CONFIG_ZONE_MOVABLE_CMA) += zone_movable_cma/

obj-y += performance/

obj-$(CONFIG_MTK_IN_HOUSE_TEE_SUPPORT) += trustzone/
ifeq ($(CONFIG_HAVE_MTK_IN_HOUSE_TEE_SUPPORT),y)
obj-$(CONFIG_TRUSTY) += trustzone/
endif

obj-$(CONFIG_THERMAL)   += thermal/
obj-$(CONFIG_MTK_MULTIBRIDGE_SUPPORT) += multibridge/
obj-$(CONFIG_MEDIATEK_SOLUTION)	+= aee/
obj-$(CONFIG_MTK_ATF_LOGGER)	+= atf_log/
obj-$(CONFIG_MTK_MLOG) += mlog/
obj-$(CONFIG_MTK_EMI_BWL)	+= emi_bwl/
obj-$(CONFIG_MTK_MJC_DRIVER)	+= mjc/
obj-$(CONFIG_MD32_SUPPORT)     += md32/
obj-$(CONFIG_MTK_EMI_MBW) += emi_mbw/
obj-$(CONFIG_MTK_BTCVSD) += btcvsd/
obj-$(CONFIG_MTK_MTD_NAND) += nand/
obj-$(CONFIG_MTK_DUM_CHAR) += dum-char/
obj-$(CONFIG_MTK_DYNAMIC_BOOST) += dynamic_boost/


obj-$(CONFIG_MTK_USB2JTAG_SUPPORT) += usb2jtag/
# Crypto performance tools (disable by default)
obj-n += crypto/

#widevine drm
obj-$(CONFIG_TRUSTONIC_TEE_SUPPORT) += secwidevine/
obj-$(CONFIG_MTK_POWER_GS)      += power_gs/
obj-$(CONFIG_MTK_TINYSYS_SCP_SUPPORT) += scp/
obj-$(CONFIG_MTK_TINYSYS_SCP_SUPPORT) += audio_ipi/
obj-$(CONFIG_USB)	+= usb_boost/
obj-$(CONFIG_RT_REGMAP) += rt-regmap/
