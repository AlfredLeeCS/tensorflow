add_llvm_executable(mlir-cpu-runner
  mlir-cpu-runner.cpp
)
llvm_update_compile_flags(mlir-cpu-runner)
whole_archive_link(mlir-cpu-runner
  MLIRAffineOps
  MLIRLLVMIR
  MLIRTargetLLVMIR
  MLIRTranslation
)
target_link_libraries(mlir-cpu-runner PRIVATE
  MLIRAnalysis
  MLIREDSC
  MLIRExecutionEngine
  MLIRIR
  MLIRJitRunner
  MLIRLLVMIR
  MLIRParser
  MLIRTargetLLVMIR
  MLIRSupport
  LLVMCore
  LLVMSupport
)
