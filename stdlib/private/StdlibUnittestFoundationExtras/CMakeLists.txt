add_swift_library(swiftStdlibUnittestFoundationExtras SHARED IS_STDLIB
  # This file should be listed the first.  Module name is inferred from the
  # filename.
  StdlibUnittestFoundationExtras.swift

  # Cannot serialize StdlibUnittestFoundationExtras because of:
  # <rdar://problem/18917405> Compiling StdlibUnittest with -sil-serialize-all
  # crashes in SIL serializer
  #
  # SWIFT_COMPILE_FLAGS ${STDLIB_SIL_SERIALIZE_ALL}

  SWIFT_MODULE_DEPENDS Foundation
  INSTALL_IN_COMPONENT stdlib-experimental)

