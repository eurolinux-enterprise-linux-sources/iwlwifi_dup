# common
CONFIG_IWLWIFI_DEBUG=n
CONFIG_IWLWIFI_DEBUGFS=n
obj-m	+= iwlwifi_dup.o
iwlwifi_dup-objs		+= iwl-io.o
iwlwifi_dup-objs		+= iwl-drv.o
iwlwifi_dup-objs		+= iwl-debug.o
iwlwifi_dup-objs		+= iwl-notif-wait.o
iwlwifi_dup-objs		+= iwl-eeprom-read.o iwl-eeprom-parse.o
iwlwifi_dup-objs		+= iwl-phy-db.o iwl-nvm-parse.o
iwlwifi_dup-objs		+= pcie/drv.o pcie/rx.o pcie/tx.o pcie/trans.o
iwlwifi_dup-objs		+= iwl-7000.o iwl-8000.o 

iwlwifi_dup-objs += $(iwlwifi-m)

ccflags-y += -D__CHECK_ENDIAN__ -I$(src)

obj-m	+= mvm/iwlmvm_dup.o

mvm/iwlmvm_dup-objs := mvm/fw.o mvm/mac80211.o mvm/nvm.o mvm/ops.o \
		mvm/phy-ctxt.o mvm/mac-ctxt.o mvm/utils.o mvm/rx.o \
		mvm/tx.o mvm/binding.o mvm/quota.o mvm/sta.o mvm/sf.o \
		mvm/scan.o mvm/time-event.o mvm/rs.o mvm/power.o \
		mvm/coex.o mvm/coex_legacy.o mvm/tt.o mvm/offloading.o \
		mvm/tdls.o mvm/d3.o

CFLAGS_iwl-devtrace.o := -I$(src)

