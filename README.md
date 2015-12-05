Updated version of Amit Singh's CPUID modified to print SGX enclave related information. I've replaced inline assembly with clang/Visual Studio provided cpuid macros to minimize dependency on compiler versions.

Following is a sample output from my chepeo Core i3 machine:

<pre>
# Identification
Vendor                    : GenuineIntel
Brand String              : Intel(R) Core(TM) i3-6100U CPU @ 2.30GHz
Model Number              : 78
Family Code               : 6
Extended Model            : 4
Extended Family           : 0
Stepping ID               : 3
Signature                 : 263907

# Address Bits
Physical Addressing       : 39
Virtual Addressing        : 48

# Multi-Core Information
Logical Processors (Threads) per Physical Processor : 16
Cores per Physical Package                          : 8

# Caches
## L1 Instruction Cache
Size                      : 32K
Line Size                 : 64B
Sharing                   : shared between 2 processor threads
Sets                      : 64
Partitions                : 1
Associativity             : 8

## L1 Data Cache
Size                      : 32K
Line Size                 : 64B
Sharing                   : shared between 2 processor threads
Sets                      : 64
Partitions                : 1
Associativity             : 8

## L2 Unified Cache
Size                      : 256K
Line Size                 : 64B
Sharing                   : shared between 2 processor threads
Sets                      : 1024
Partitions                : 1
Associativity             : 4

## L3 Unified Cache
Size                      : 3M
Line Size                 : 64B
Sharing                   : shared between 16 processor threads
Sets                      : 4096
Partitions                : 1
Associativity             : 12

# Translation Lookaside Buffers
Instruction TLBs          : 0 large, 0 small
Data TLBs                 : 0 large, 64 small

# Features
ACPI                      : Thermal Monitor and Software Controlled Clock
APIC                      : On-Chip APIC Hardware
CLFSH                     : CLFLUSH Instruction
CMOV                      : Conditional Move Instruction
CX16                      : CMPXCHG16B Instruction
CX8                       : CMPXCHG8 Instruction
DE                        : Debugging Extension
DS                        : Debug Store
DS-CPL                    : CPL Qualified Debug Store
DTES64                    : 64-Bit Debug Store
EST                       : Enhanced Intel SpeedStep Technology
FPU                       : Floating-Point Unit On-Chip
FXSR                      : FXSAVE and FXSTOR Instructions
HTT                       : HyperThreading
MCA                       : Machine-Check Architecture
MCE                       : Machine-Check Exception
MMX                       : MMX Technology
MONITOR                   : MONITOR/MWAIT Instructions
MOVBE                     : MOVBE Instruction
MSR                       : Model Specific Registers
MTRR                      : Memory Type Range Registers
OSXSAVE                   : XSETBV/XGETBV Instructions Enabled
PAE                       : Physical Address Extension
PAT                       : Page Attribute Table
PBE                       : Pending Break Enable
PDCM                      : Perfmon and Debug Capability
PGE                       : Page Global Enable
POPCNT                    : POPCNT Instruction
PSE                       : Page Size Extension
PSE-36                    : 36-Bit Page Size Extension
SEP                       : Fast System Call
SS                        : Self-Snoop
SSE                       : Streaming SIMD Extensions
SSE2                      : Streaming SIMD Extensions 2
SSE3                      : Streaming SIMD Extensions 3
SSSE3                     : Supplemental Streaming SIMD Extensions 3
SSE4.1                    : Streaming SIMD Extensions 4.1
SSE4.2                    : Streaming SIMD Extensions 4.2
TM                        : Thermal Monitor
TM2                       : Thermal Monitor 2
TSC                       : Time Stamp Counter
VME                       : Virtual Mode Extension
VMX                       : Virtual Machine Extensions
XSAVE                     : XSAVE/XSTOR States
x2APIC                    : Extended xAPIC Support
xTPR                      : xTPR Update Control

# Extended Features
EM64T                     : Intel Extended Memory 64 Technology
XD                        : Execution Disable


# SGX Information
SGX1 Supported            : True
SGX2 Supported            : False
Max 32-bit enclave size   : 2^31
Max 64-bit enclave size   : 2^36
MISCSECS                  : 0x00000000
## SECS Attributes
  Initialized             : 0
  Debugged                : 0
  Mode64                  : 0
  PROVISIONKEY Available  : 0
  EINITTOKENKEY Available : 0
  
</pre>
