add_mlir_dialect_library(MLIRToy
        AST.cpp

        ADDITIONAL_HEADER_DIRS
        ${PROJECT_SOURCE_DIR}/include/toy

        DEPENDS

	LINK_LIBS PUBLIC
	MLIRIR
	)
