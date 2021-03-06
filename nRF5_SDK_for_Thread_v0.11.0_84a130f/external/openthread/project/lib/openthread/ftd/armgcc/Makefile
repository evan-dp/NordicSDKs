PROJECT_NAME     := openthread_lib_libopenthread_ftd
TARGETS          := libopenthread_ftd
OUTPUT_DIRECTORY := _build

SDK_ROOT := ../../../../../../..
PROJ_DIR := ../../../..


# Source files common to all targets
SRC_FILES += \
  $(PROJ_DIR)/openthread/src/core/thread/address_resolver.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/aes_ccm.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/aes_ecb.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/announce_begin_client.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/announce_begin_server.cpp \
  $(PROJ_DIR)/openthread/src/core/api/border_router_api.cpp \
  $(PROJ_DIR)/openthread/src/core/utils/child_supervision.cpp \
  $(PROJ_DIR)/openthread/src/core/api/child_supervision_api.cpp \
  $(PROJ_DIR)/openthread/src/core/coap/coap.cpp \
  $(PROJ_DIR)/openthread/src/core/api/coap_api.cpp \
  $(PROJ_DIR)/openthread/src/core/coap/coap_header.cpp \
  $(PROJ_DIR)/openthread/src/core/coap/coap_secure.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/commissioner.cpp \
  $(PROJ_DIR)/openthread/src/core/api/commissioner_api.cpp \
  $(PROJ_DIR)/openthread/src/core/common/crc16.cpp \
  $(PROJ_DIR)/openthread/src/core/api/crypto_api.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/data_poll_manager.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/dataset.cpp \
  $(PROJ_DIR)/openthread/src/core/api/dataset_api.cpp \
  $(PROJ_DIR)/openthread/src/core/api/dataset_ftd_api.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/dataset_local.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/dataset_manager.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/dataset_manager_ftd.cpp \
  $(PROJ_DIR)/openthread/src/core/api/dhcp6_api.cpp \
  $(PROJ_DIR)/openthread/src/core/net/dhcp6_client.cpp \
  $(PROJ_DIR)/openthread/src/core/net/dhcp6_server.cpp \
  $(PROJ_DIR)/openthread/src/core/api/dns_api.cpp \
  $(PROJ_DIR)/openthread/src/core/net/dns_client.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/dtls.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/energy_scan_client.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/energy_scan_server.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/heap.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/hmac_sha256.cpp \
  $(PROJ_DIR)/openthread/src/core/net/icmp6.cpp \
  $(PROJ_DIR)/openthread/src/core/api/icmp6_api.cpp \
  $(PROJ_DIR)/openthread/src/core/common/instance.cpp \
  $(PROJ_DIR)/openthread/src/core/api/instance_api.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6_address.cpp \
  $(PROJ_DIR)/openthread/src/core/api/ip6_api.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6_filter.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6_headers.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6_mpl.cpp \
  $(PROJ_DIR)/openthread/src/core/net/ip6_routes.cpp \
  $(PROJ_DIR)/openthread/src/core/api/jam_detection_api.cpp \
  $(PROJ_DIR)/openthread/src/core/utils/jam_detector.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/joiner.cpp \
  $(PROJ_DIR)/openthread/src/core/api/joiner_api.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/joiner_router.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/key_manager.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/leader.cpp \
  $(PROJ_DIR)/openthread/src/core/api/link_api.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/link_quality.cpp \
  $(PROJ_DIR)/openthread/src/core/api/link_raw_api.cpp \
  $(PROJ_DIR)/openthread/src/core/common/locator.cpp \
  $(PROJ_DIR)/openthread/src/core/common/logging.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/lowpan.cpp \
  $(PROJ_DIR)/openthread/src/core/mac/mac.cpp \
  $(PROJ_DIR)/openthread/src/core/mac/mac_filter.cpp \
  $(PROJ_DIR)/openthread/src/core/mac/mac_frame.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/mbedtls.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/mesh_forwarder.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/meshcop.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/meshcop_tlvs.cpp \
  $(PROJ_DIR)/openthread/src/core/common/message.cpp \
  $(PROJ_DIR)/openthread/src/core/api/message_api.cpp \
  $(PROJ_DIR)/openthread/src/core/utils/missing_strlcat.c \
  $(PROJ_DIR)/openthread/src/core/utils/missing_strlcpy.c \
  $(PROJ_DIR)/openthread/src/core/utils/missing_strnlen.c \
  $(PROJ_DIR)/openthread/src/core/thread/mle.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/mle_router.cpp \
  $(PROJ_DIR)/openthread/src/core/api/netdata_api.cpp \
  $(PROJ_DIR)/openthread/src/core/net/netif.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/network_data.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/network_data_leader.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/network_data_leader_ftd.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/network_data_local.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/network_diagnostic.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/panid_query_client.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/panid_query_server.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/pbkdf2_cmac.cpp \
  $(PROJ_DIR)/openthread/src/core/api/server_api.cpp \
  $(PROJ_DIR)/openthread/src/core/crypto/sha256.cpp \
  $(PROJ_DIR)/openthread/src/core/utils/slaac_address.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/src_match_controller.cpp \
  $(PROJ_DIR)/openthread/src/core/common/tasklet.cpp \
  $(PROJ_DIR)/openthread/src/core/api/tasklet_api.cpp \
  $(PROJ_DIR)/openthread/src/core/api/thread_api.cpp \
  $(PROJ_DIR)/openthread/src/core/api/thread_ftd_api.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/thread_netif.cpp \
  $(PROJ_DIR)/openthread/src/core/common/timer.cpp \
  $(PROJ_DIR)/openthread/src/core/meshcop/timestamp.cpp \
  $(PROJ_DIR)/openthread/src/core/common/tlvs.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/tmf_proxy.cpp \
  $(PROJ_DIR)/openthread/src/core/api/tmf_proxy_api.cpp \
  $(PROJ_DIR)/openthread/src/core/thread/topology.cpp \
  $(PROJ_DIR)/openthread/src/core/common/trickle_timer.cpp \
  $(PROJ_DIR)/openthread/src/core/net/udp6.cpp \
  $(PROJ_DIR)/openthread/src/core/api/udp_api.cpp \

# Include folders common to all targets
INC_FOLDERS += \
  $(PROJ_DIR)/openthread/examples/platforms/nrf52840 \
  $(PROJ_DIR)/openthread/third_party/mbedtls/repo.patched/include/mbedtls \
  $(PROJ_DIR)/openthread/third_party/mbedtls \
  $(PROJ_DIR)/openthread/examples/platforms/nrf52840/crypto \
  $(PROJ_DIR)/openthread/third_party/mbedtls/repo.patched/include \
  $(PROJ_DIR)/openthread/src/core \
  $(PROJ_DIR)/openthread/include \
  $(PROJ_DIR) \

# Libraries common to all targets
LIB_FILES += \

# Optimization flags
OPT = -Os -g3
# Uncomment the line below to enable link time optimization
#OPT += -flto

# C flags common to all targets
CFLAGS += $(OPT)
CFLAGS += -DHAVE_CONFIG_H
CFLAGS += -DMBEDTLS_CONFIG_FILE="\"mbedtls-config.h\""
CFLAGS += -DMBEDTLS_USER_CONFIG_FILE="\"nrf52840-mbedtls-config.h\""
CFLAGS += -DOPENTHREAD_CONFIG_LOG_OUTPUT=OPENTHREAD_CONFIG_LOG_OUTPUT_PLATFORM_DEFINED
CFLAGS += -DOPENTHREAD_FTD=1
CFLAGS += -DOPENTHREAD_PROJECT_CORE_CONFIG_FILE="\"openthread-core-nrf52840-config.h\""
CFLAGS += -D_BSD_SOURCE=1
CFLAGS += -D_DEFAULT_SOURCE=1
CFLAGS += -mcpu=cortex-m4
CFLAGS += -mthumb -mabi=aapcs
CFLAGS +=  -Wall -Werror
CFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
# keep every function in a separate section, this allows linker to discard unused ones
CFLAGS += -ffunction-sections -fdata-sections -fno-strict-aliasing
CFLAGS += -fno-builtin -fshort-enums 

# C++ flags common to all targets
CXXFLAGS += $(OPT)

# Assembler flags common to all targets
ASMFLAGS += -g3
ASMFLAGS += -mcpu=cortex-m4
ASMFLAGS += -mthumb -mabi=aapcs
ASMFLAGS += -mfloat-abi=hard -mfpu=fpv4-sp-d16
ASMFLAGS += -DHAVE_CONFIG_H
ASMFLAGS += -DMBEDTLS_CONFIG_FILE="\"mbedtls-config.h\""
ASMFLAGS += -DMBEDTLS_USER_CONFIG_FILE="\"nrf52840-mbedtls-config.h\""
ASMFLAGS += -DOPENTHREAD_CONFIG_LOG_OUTPUT=OPENTHREAD_CONFIG_LOG_OUTPUT_PLATFORM_DEFINED
ASMFLAGS += -DOPENTHREAD_FTD=1
ASMFLAGS += -DOPENTHREAD_PROJECT_CORE_CONFIG_FILE="\"openthread-core-nrf52840-config.h\""
ASMFLAGS += -D_BSD_SOURCE=1
ASMFLAGS += -D_DEFAULT_SOURCE=1



# Add standard libraries at the very end of the linker input, after all objects
# that may need symbols provided by these libraries.
LIB_FILES += -lc -lnosys -lm


.PHONY: default help

# Default target - first one defined
default: libopenthread_ftd

# Print all targets that can be built
help:
	@echo following targets are available:
	@echo		libopenthread_ftd

TEMPLATE_PATH := $(SDK_ROOT)/components/toolchain/gcc


include $(TEMPLATE_PATH)/Makefile.common

$(call define_library, $(TARGETS), $(PROJ_DIR)/lib/openthread/ftd/armgcc/libopenthread-ftd.a)

define create_library
@echo Creating library: $($@)
$(NO_ECHO)$(AR) $($@) $^
@echo Done
endef
libopenthread_ftd:
	$(create_library)

SDK_CONFIG_FILE := ../config/sdk_config.h
CMSIS_CONFIG_TOOL := $(SDK_ROOT)/external_tools/cmsisconfig/CMSIS_Configuration_Wizard.jar
sdk_config:
	java -jar $(CMSIS_CONFIG_TOOL) $(SDK_CONFIG_FILE)
