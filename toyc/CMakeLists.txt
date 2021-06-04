set(LIBS
        MLIROptLib
        MLIRToy
        )
add_llvm_executable(toyc main.cpp)

llvm_update_compile_flags(toyc)
target_link_libraries(toyc PRIVATE ${LIBS})

mlir_check_all_link_libraries(toyc)

install(TARGETS toyc DESTINATION bin)