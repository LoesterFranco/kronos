# Copyright (c) 2020 Sonal Pinto
# SPDX-License-Identifier: Apache-2.0

add_hdl_source(kronos_types.sv)

add_hdl_source(kronos_counter64.sv)

add_hdl_source(kronos_branch.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_alu.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_agu.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_hcu.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_csr.sv
  DEPENDS
    kronos_types
    kronos_counter64
)

add_hdl_source(kronos_lsu.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_RF.sv
  DEPENDS
    kronos_types
)

add_hdl_source(kronos_IF.sv
  DEPENDS
    kronos_types
    kronos_RF
)

add_hdl_source(kronos_ID.sv
  DEPENDS
    kronos_types
    kronos_branch
    kronos_agu
    kronos_hcu
)

add_hdl_source(kronos_EX.sv
  DEPENDS
    kronos_types
    kronos_alu
    kronos_lsu
    kronos_csr
)

add_hdl_source(kronos_core.sv
  DEPENDS
    kronos_types
    kronos_IF
    kronos_ID
    kronos_EX
)
