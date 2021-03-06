PROJECT_NAME     := mbedtls_openthread_nrf52_library_armgcc
TARGETS          := mbedtls_openthread_lib
OUTPUT_DIRECTORY := _build

SDK_ROOT := ../../../../../..
PROJ_DIR := ../..


# Source files common to all targets
SRC_FILES += \
  $(SDK_ROOT)/external/mbedtls/library/aes.c \
  $(PROJ_DIR)/mbedtls/aes_alt_cc310.c \
  $(SDK_ROOT)/external/mbedtls/library/bignum.c \
  $(PROJ_DIR)/cc310_mbedtls.c \
  $(SDK_ROOT)/external/mbedtls/library/ccm.c \
  $(SDK_ROOT)/external/mbedtls/library/cipher.c \
  $(SDK_ROOT)/external/mbedtls/library/cipher_wrap.c \
  $(SDK_ROOT)/external/mbedtls/library/cmac.c \
  $(SDK_ROOT)/external/mbedtls/library/ctr_drbg.c \
  $(SDK_ROOT)/external/mbedtls/library/debug.c \
  $(SDK_ROOT)/external/mbedtls/library/ecjpake.c \
  $(PROJ_DIR)/mbedtls/ecp.c \
  $(SDK_ROOT)/external/mbedtls/library/ecp_curves.c \
  $(SDK_ROOT)/external/mbedtls/library/entropy.c \
  $(SDK_ROOT)/external/mbedtls/library/entropy_poll.c \
  $(PROJ_DIR)/hardware_entropy.c \
  $(SDK_ROOT)/external/mbedtls/library/md.c \
  $(SDK_ROOT)/external/mbedtls/library/md_wrap.c \
  $(SDK_ROOT)/external/mbedtls/library/memory_buffer_alloc.c \
  $(SDK_ROOT)/external/mbedtls/library/platform.c \
  $(SDK_ROOT)/external/mbedtls/library/sha256.c \
  $(PROJ_DIR)/mbedtls/sha256_alt_cc310.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_ciphersuites.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_cli.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_cookie.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_srv.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_ticket.c \
  $(SDK_ROOT)/external/mbedtls/library/ssl_tls.c \

# Include folders common to all targets
INC_FOLDERS += \
  $(SDK_ROOT)/external/openthread/include \
  $(SDK_ROOT)/external/nrf_cc310/include \
  $(PROJ_DIR)/../../../toolchain \
  $(SDK_ROOT)/external/mbedtls/include \
  $(PROJ_DIR)/../../../toolchain/gcc \
  $(PROJ_DIR)/../../../toolchain/cmsis/include \
  $(PROJ_DIR) \
  $(SDK_ROOT)/external/mbedtls/include/mbedtls \
  $(PROJ_DIR)/mbedtls \
  $(PROJ_DIR)/../../../device \

# Libraries common to all targets
LIB_FILES += \

# Optimization flags
OPT = -Os -g3
# Uncomment the line below to enable link time optimization
#OPT += -flto

# C flags common to all targets
CFLAGS += $(OPT)
CFLAGS += -DMBEDTLS_CONFIG_FILE="\"mbedtls-config.h\""
CFLAGS += -DNRF52840_XXAA
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
ASMFLAGS += -DMBEDTLS_CONFIG_FILE="\"mbedtls-config.h\""
ASMFLAGS += -DNRF52840_XXAA



# Add standard libraries at the very end of the linker input, after all objects
# that may need symbols provided by these libraries.
LIB_FILES += -lc -lnosys -lm


.PHONY: default help

# Default target - first one defined
default: mbedtls_openthread_lib

# Print all targets that can be built
help:
	@echo following targets are available:
	@echo		mbedtls_openthread_lib

TEMPLATE_PATH := $(PROJ_DIR)/../../../toolchain/gcc


include $(TEMPLATE_PATH)/Makefile.common

$(call define_library, $(TARGETS), $(PROJ_DIR)/nrf52_armgcc/armgcc/libmbedcrypto-cc310.a)

define create_library
@echo Creating library: $($@)
$(NO_ECHO)$(AR) $($@) $^
@echo Done
endef
mbedtls_openthread_lib:
	$(create_library)

SDK_CONFIG_FILE := ../config/sdk_config.h
CMSIS_CONFIG_TOOL := $(SDK_ROOT)/external_tools/cmsisconfig/CMSIS_Configuration_Wizard.jar
sdk_config:
	java -jar $(CMSIS_CONFIG_TOOL) $(SDK_CONFIG_FILE)
