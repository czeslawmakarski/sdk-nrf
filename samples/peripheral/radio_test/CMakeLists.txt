#
# Copyright (c) 2020 Nordic Semiconductor
#
# SPDX-License-Identifier: LicenseRef-BSD-5-Clause-Nordic
#

cmake_minimum_required(VERSION 3.13.1)

set(NRF_SUPPORTED_BOARDS
	nrf5340pdk_nrf5340_cpunet
	nrf52dk_nrf52832
	nrf52840dk_nrf52840
)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(NONE)

FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE
	${app_sources}
)
