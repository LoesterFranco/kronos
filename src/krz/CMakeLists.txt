# Copyright (c) 2020 Sonal Pinto
# SPDX-License-Identifier: Apache-2.0

add_riscv_executable(krz_bootloader.c
    LINKER_SCRIPT
        bootloader.ld
)

add_riscv_executable(krz_test_boot.S
    LINKER_SCRIPT
        bootloader.ld
)

add_riscv_executable(krz_blinky.c
    SOURCES
        mini-printf.c
    KRZ_APP TRUE    
)
