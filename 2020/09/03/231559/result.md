# Benchmark result

* Pull request commit: [`43bb185afc2f8a3310550df343b1415e27ef5ea9`](https://github.com/JuliaFolds/FGenerators.jl/commit/43bb185afc2f8a3310550df343b1415e27ef5ea9)
* Pull request: <https://github.com/JuliaFolds/FGenerators.jl/pull/7> (FLoops.jl integration)

# Judge result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Sep 2020 - 23:14
    - Baseline: 3 Sep 2020 - 23:15
* Package commits:
    - Target: 53a003
    - Baseline: 3871d1
* Julia commits:
    - Target: 697e78
    - Baseline: 697e78
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: None
    - Baseline: None

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                                      | time ratio    | memory ratio |
|-------------------------------------------------------------------------|---------------|--------------|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` | 1.11 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` | 1.10 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   | 1.09 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 1.05 (5%) :x: |   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo

### Target
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5980 s          0 s       1396 s      22992 s          0 s
       #2  2095 MHz      10375 s          0 s       1559 s      18804 s          0 s
       
  Memory: 6.764881134033203 GB (3218.94921875 MB free)
  Uptime: 324.0 sec
  Load Avg:  1.046875  0.70361328125  0.32568359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9346 s          0 s       1444 s      23681 s          0 s
       #2  2095 MHz      11089 s          0 s       1587 s      22179 s          0 s
       
  Memory: 6.764881134033203 GB (3233.73046875 MB free)
  Uptime: 365.0 sec
  Load Avg:  1.0751953125  0.75732421875  0.3623046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 3 Sep 2020 - 23:14
* Package commit: 53a003
* Julia commit: 697e78
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                      | time            | GC time | memory         | allocations |
|-------------------------------------------------------------------------|----------------:|--------:|---------------:|------------:|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.760 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   7.067 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |  10.001 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   7.600 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.160 μs (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.600 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   1.930 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.340 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 679.784 ns (5%) |         |                |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5980 s          0 s       1396 s      22992 s          0 s
       #2  2095 MHz      10375 s          0 s       1559 s      18804 s          0 s
       
  Memory: 6.764881134033203 GB (3218.94921875 MB free)
  Uptime: 324.0 sec
  Load Avg:  1.046875  0.70361328125  0.32568359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 3 Sep 2020 - 23:15
* Package commit: 3871d1
* Julia commit: 697e78
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                      | time            | GC time | memory         | allocations |
|-------------------------------------------------------------------------|----------------:|--------:|---------------:|------------:|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.200 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   6.400 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |  10.100 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   7.000 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.100 μs (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.600 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   1.900 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.300 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 700.000 ns (5%) |         |                |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       9346 s          0 s       1444 s      23681 s          0 s
       #2  2095 MHz      11089 s          0 s       1587 s      22179 s          0 s
       
  Memory: 6.764881134033203 GB (3233.73046875 MB free)
  Uptime: 365.0 sec
  Load Avg:  1.0751953125  0.75732421875  0.3623046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.246
    BogoMIPS:            4190.49
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

