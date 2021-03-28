# NAS Parallel Benchmarks 3.0 Fork

## Why?

Java code is identical to the code provided by [NASA for NPB 3.0](https://www.nas.nasa.gov/assets/npb/NPB3.0.tar.gz)
I made a fork with only a few small improvements:

* Use [gradle](https://gradle.org/) (tested with 6.8) instead of Make for the compilation
* Changed the testAllS and testAllW scripts to use jar file instead of classes

Also tested the benchmark using Oracle Java Development Kit version 11:

## Environment

```
java version "11.0.10" 2021-01-19 LTS
Java(TM) SE Runtime Environment 18.9 (build 11.0.10+8-LTS-162)
Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.10+8-LTS-162, mixed mode)

 josevnz  dmaf5  ~/NPB3.0/NPB3.0-JAV  lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   43 bits physical, 48 bits virtual
CPU(s):                          8
On-line CPU(s) list:             0-7
Thread(s) per core:              2
Core(s) per socket:              4
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       AuthenticAMD
CPU family:                      23
Model:                           24
Model name:                      AMD Ryzen 5 3550H with Radeon Vega Mobile Gfx
Stepping:                        1
Frequency boost:                 enabled
CPU MHz:                         1400.000
CPU max MHz:                     2100.0000
CPU min MHz:                     1400.0000
BogoMIPS:                        4192.15
Virtualization:                  AMD-V
L1d cache:                       128 KiB
L1i cache:                       256 KiB
L2 cache:                        2 MiB
L3 cache:                        4 MiB
NUMA node0 CPU(s):               0-7
Vulnerability Itlb multihit:     Not affected
Vulnerability L1tf:              Not affected
Vulnerability Mds:               Not affected
Vulnerability Meltdown:          Not affected
Vulnerability Spec store bypass: Mitigation; Speculative Store Bypass disabled via prctl and seccomp
Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
Vulnerability Spectre v2:        Mitigation; Full AMD retpoline, IBPB conditional, STIBP disabled, RSB filling
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm 
                                 constant_tsc rep_good nopl nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq monitor ssse3 fma cx16 sse4_1 sse4_2 movbe popcnt aes xsave avx 
                                 f16c rdrand lahf_lm cmp_legacy svm extapic cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw skinit wdt tce topoext perfctr_core perfctr_nb bpex
                                 t perfctr_llc mwaitx cpb hw_pstate sme ssbd sev ibpb vmmcall sev_es fsgsbase bmi1 avx2 smep bmi2 rdseed adx smap clflushopt sha_ni xsaveopt xsavec
                                  xgetbv1 xsaves clzero irperf xsaveerptr arat npt lbrv svm_lock nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold a
                                 vic v_vmsave_vmload vgif overflow_recov succor smca
```

Added the samples directory, so you can get an idea of the output of this benchmarks