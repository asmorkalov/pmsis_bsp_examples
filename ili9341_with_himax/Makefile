APP = test
APP_SRCS += test.c
APP_CFLAGS += -O3 -g
USE_PMSIS_BSP=1

RUNNER_CONFIG = $(CURDIR)/config.ini

BOARD ?= gapuino

ifeq '$(BOARD_NAME)' 'gapuino'
APP_CFLAGS = -DGAPUINO -DHIMAX
endif

ifeq '$(BOARD_NAME)' 'gapoc_a'
PLPBRIDGE_FLAGS += -ftdi
APP_CFLAGS = -DGAPOC_A
# -DUSE_BRIDGE
endif

include $(RULES_DIR)/pmsis_rules.mk
