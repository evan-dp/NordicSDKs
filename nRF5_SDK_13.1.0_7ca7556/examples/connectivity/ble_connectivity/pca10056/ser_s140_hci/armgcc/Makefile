PROJECT_NAME     := ble_connectivity_s140_hci_pca10056
TARGETS          := nrf52840_xxaa
OUTPUT_DIRECTORY := _build

SDK_ROOT := ../../../../../..
PROJ_DIR := ../../..

$(OUTPUT_DIRECTORY)/nrf52840_xxaa.out: \
  LINKER_SCRIPT  := ble_connectivity_gcc_nrf52.ld

# Source files common to all targets
SRC_FILES += \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_backend_serial.c \
  $(SDK_ROOT)/components/libraries/log/src/nrf_log_frontend.c \
  $(SDK_ROOT)/components/libraries/util/app_error.c \
  $(SDK_ROOT)/components/libraries/util/app_error_weak.c \
  $(SDK_ROOT)/components/libraries/scheduler/app_scheduler.c \
  $(SDK_ROOT)/components/libraries/timer/app_timer.c \
  $(SDK_ROOT)/components/libraries/util/app_util_platform.c \
  $(SDK_ROOT)/components/libraries/crc16/crc16.c \
  $(SDK_ROOT)/components/libraries/util/nrf_assert.c \
  $(SDK_ROOT)/components/libraries/queue/nrf_queue.c \
  $(SDK_ROOT)/components/libraries/strerror/nrf_strerror.c \
  $(SDK_ROOT)/components/boards/boards.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/common/ble_dtm_init.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_event_enc.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_evt_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gap_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gap_evt_conn.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/ble_gap_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/ble_gatt_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gattc_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gattc_evt_conn.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/ble_gattc_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gatts_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_gatts_evt_conn.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/ble_gatts_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_l2cap_conn.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/ble_l2cap_evt_conn.c \
  $(SDK_ROOT)/components/serialization/common/ble_serialization.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/ble_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/common/cond_field_serialization.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/conn_ble_gap_sec_keys.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/conn_ble_user_mem.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/common/conn_mw.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware/conn_mw_ble.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware/conn_mw_ble_gap.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware/conn_mw_ble_gattc.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware/conn_mw_ble_gatts.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware/conn_mw_ble_l2cap.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/common/conn_mw_nrf_soc.c \
  $(SDK_ROOT)/components/serialization/connectivity/hal/dtm_uart.c \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers/nrf_soc_conn.c \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble/nrf_soc_struct_serialization.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_cmd_decoder.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_dtm_cmd_decoder.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_error_handling.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_event_encoder.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_handlers.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_pkt_decoder.c \
  $(SDK_ROOT)/components/serialization/connectivity/ser_conn_reset_cmd_decoder.c \
  $(SDK_ROOT)/components/serialization/common/ser_dbg_sd_str.c \
  $(SDK_ROOT)/components/serialization/common/transport/ser_hal_transport.c \
  $(SDK_ROOT)/components/serialization/common/transport/ser_phy/ser_phy_hci.c \
  $(SDK_ROOT)/components/serialization/common/transport/ser_phy/ser_phy_hci_slip.c \
  $(SDK_ROOT)/components/drivers_nrf/clock/nrf_drv_clock.c \
  $(SDK_ROOT)/components/drivers_nrf/common/nrf_drv_common.c \
  $(SDK_ROOT)/components/drivers_nrf/uart/nrf_drv_uart.c \
  $(PROJ_DIR)/main.c \
  $(SDK_ROOT)/external/segger_rtt/RTT_Syscalls_GCC.c \
  $(SDK_ROOT)/external/segger_rtt/SEGGER_RTT.c \
  $(SDK_ROOT)/external/segger_rtt/SEGGER_RTT_printf.c \
  $(SDK_ROOT)/components/ble/common/ble_advdata.c \
  $(SDK_ROOT)/components/ble/common/ble_conn_params.c \
  $(SDK_ROOT)/components/ble/ble_dtm/ble_dtm.c \
  $(SDK_ROOT)/components/ble/ble_dtm/ble_dtm_hw_nrf52.c \
  $(SDK_ROOT)/components/ble/common/ble_srv_common.c \
  $(SDK_ROOT)/components/toolchain/gcc/gcc_startup_nrf52840.S \
  $(SDK_ROOT)/components/toolchain/system_nrf52840.c \
  $(SDK_ROOT)/components/softdevice/common/softdevice_handler/softdevice_handler.c \

# Include folders common to all targets
INC_FOLDERS += \
  $(SDK_ROOT)/components \
  $(SDK_ROOT)/components/serialization/connectivity/hal \
  $(SDK_ROOT)/components/libraries/scheduler \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/serializers \
  $(SDK_ROOT)/components/toolchain/cmsis/include \
  $(SDK_ROOT)/components/libraries/queue \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/common \
  $(SDK_ROOT)/components/serialization/connectivity \
  $(SDK_ROOT)/components/libraries/strerror \
  $(SDK_ROOT)/components/serialization/connectivity/codecs/ble/middleware \
  $(SDK_ROOT)/components/drivers_nrf/delay \
  $(SDK_ROOT)/components/serialization/common \
  $(SDK_ROOT)/components/ble/ble_dtm \
  $(SDK_ROOT)/components/libraries/crc16 \
  $(SDK_ROOT)/components/libraries/util \
  $(SDK_ROOT)/components/drivers_nrf/uart \
  $(SDK_ROOT)/components/ble/common \
  $(SDK_ROOT)/components/libraries/bsp \
  $(SDK_ROOT)/components/device \
  $(SDK_ROOT)/components/libraries/log \
  $(SDK_ROOT)/components/libraries/timer \
  $(SDK_ROOT)/components/softdevice/s140/headers \
  $(SDK_ROOT)/components/serialization/common/transport/ser_phy \
  $(SDK_ROOT)/components/toolchain/gcc \
  $(SDK_ROOT)/external/segger_rtt \
  ../config \
  $(SDK_ROOT)/components/boards \
  $(SDK_ROOT)/components/drivers_nrf/hal \
  $(SDK_ROOT)/components/serialization/common/struct_ser/ble \
  $(SDK_ROOT)/components/toolchain \
  $(SDK_ROOT)/components/drivers_nrf/common \
  $(SDK_ROOT)/components/serialization/common/transport \
  $(SDK_ROOT)/components/drivers_nrf/clock \
  $(SDK_ROOT)/components/serialization/common/transport/ser_phy/config \
  $(SDK_ROOT)/components/softdevice/s140/headers/nrf52 \
  $(SDK_ROOT)/components/softdevice/common/softdevice_handler \
  $(SDK_ROOT)/components/libraries/log/src \

# Libraries common to all targets
LIB_FILES += \

# C flags common to all targets
CFLAGS += -DBLE_STACK_SUPPORT_REQD
CFLAGS += -DBOARD_PCA10056
CFLAGS += -DBSP_DEFINES_ONLY
CFLAGS += -DCONFIG_GPIO_AS_PINRESET
CFLAGS += -DHCI_TIMER2
CFLAGS += -DNRF52840_XXAA
CFLAGS += -DNRF_SD_BLE_API_VERSION=5
CFLAGS += -DS140
CFLAGS += -DSER_CONNECTIVITY
CFLAGS += -DSOFTDEVICE_PRESENT
CFLAGS += -DSWI_DISABLE0
CFLAGS += -D__HEAP_SIZE=1024
CFLAGS += -D__STACK_SIZE=2048
CFLAGS += -mcpu=cortex-m4
CFLAGS += -mthumb -mabi=aapcs
CFLAGS +=  -Wall -Werror -O3 -g3
CFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
# keep every function in separate section, this allows linker to discard unused ones
CFLAGS += -ffunction-sections -fdata-sections -fno-strict-aliasing
CFLAGS += -fno-builtin --short-enums 

# C++ flags common to all targets
CXXFLAGS += \

# Assembler flags common to all targets
ASMFLAGS += -x assembler-with-cpp
ASMFLAGS += -DBLE_STACK_SUPPORT_REQD
ASMFLAGS += -DBOARD_PCA10056
ASMFLAGS += -DBSP_DEFINES_ONLY
ASMFLAGS += -DCONFIG_GPIO_AS_PINRESET
ASMFLAGS += -DHCI_TIMER2
ASMFLAGS += -DNRF52840_XXAA
ASMFLAGS += -DNRF_SD_BLE_API_VERSION=5
ASMFLAGS += -DS140
ASMFLAGS += -DSER_CONNECTIVITY
ASMFLAGS += -DSOFTDEVICE_PRESENT
ASMFLAGS += -DSWI_DISABLE0
ASMFLAGS += -D__HEAP_SIZE=1024
ASMFLAGS += -D__STACK_SIZE=2048

# Linker flags
LDFLAGS += -mthumb -mabi=aapcs -L $(TEMPLATE_PATH) -T$(LINKER_SCRIPT)
LDFLAGS += -mcpu=cortex-m4
LDFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
# let linker to dump unused sections
LDFLAGS += -Wl,--gc-sections
# use newlib in nano version
LDFLAGS += --specs=nano.specs -lc -lnosys


.PHONY: $(TARGETS) default all clean help flash flash_softdevice

# Default target - first one defined
default: nrf52840_xxaa

# Print all targets that can be built
help:
	@echo following targets are available:
	@echo 	nrf52840_xxaa

TEMPLATE_PATH := $(SDK_ROOT)/components/toolchain/gcc

include $(TEMPLATE_PATH)/Makefile.common

$(foreach target, $(TARGETS), $(call define_target, $(target)))

# Flash the program
flash: $(OUTPUT_DIRECTORY)/nrf52840_xxaa.hex
	@echo Flashing: $<
	nrfjprog --program $< -f nrf52 --sectorerase
	nrfjprog --reset -f nrf52

# Flash softdevice
flash_softdevice:
	@echo Flashing: s140_nrf52840_5.0.0-2.alpha_softdevice.hex
	nrfjprog --program $(SDK_ROOT)/components/softdevice/s140/hex/s140_nrf52840_5.0.0-2.alpha_softdevice.hex -f nrf52 --sectorerase 
	nrfjprog --reset -f nrf52

erase:
	nrfjprog --eraseall -f nrf52
