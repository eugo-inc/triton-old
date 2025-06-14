add_triton_library(TritonGPUToLLVM
    DotOpToLLVM/FMA.cpp
    DotOpToLLVM/FMADotUtility.cpp
    AllocateSharedMemory.cpp
    AllocateWarpGroups.cpp
    AssertOpToLLVM.cpp
    ControlFlowOpToLLVM.cpp
    ConvertLayoutOpToLLVM.cpp
    ElementwiseOpToLLVM.cpp
    FuncOpToLLVM.cpp
    GatherOpToLLVM.cpp
    GlobalScratchMemoryAllocation.cpp
    HistogramOpToLLVM.cpp
    MakeRangeOpToLLVM.cpp
    MemoryOpToLLVM.cpp
    PrintOpToLLVM.cpp
    ReduceOpToLLVM.cpp
    ScanOpToLLVM.cpp
    SPMDOpToLLVM.cpp
    TypeConverter.cpp
    Utility.cpp
    ViewOpToLLVM.cpp

    DEPENDS
    TritonGPUConversionPassIncGen

    LINK_LIBS PUBLIC
    MLIRIR
    MLIRPass
    MLIRGPUDialect
    MLIRGPUToNVVMTransforms
    # MLIRGPUToROCDLTransforms // @EUGO_CHANGE - no ROCM support
    MLIRGPUTransforms
    TritonAnalysis
    TritonIR
    TritonGPUIR
    TritonGPUTransforms
    TritonNvidiaGPUTransforms
)
