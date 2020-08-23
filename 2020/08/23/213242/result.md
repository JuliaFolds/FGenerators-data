# Benchmark result

* Pull request commit: [`28334bcb03f05fffd16658205f35adee0491e92c`](https://github.com/JuliaFolds/FGenerators.jl/commit/28334bcb03f05fffd16658205f35adee0491e92c)
* Pull request: <https://github.com/JuliaFolds/FGenerators.jl/pull/9> (Mention how to combine FGenerators with SplittablesBase)

# Judge result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Aug 2020 - 21:31
    - Baseline: 23 Aug 2020 - 21:32
* Package commits:
    - Target: f6d3a7
    - Baseline: 5373a3
* Julia commits:
    - Target: 96786e
    - Baseline: 96786e
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` | 1.24 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   | 1.13 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  | 1.13 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 1.10 (5%) :x: |   1.00 (1%)  |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       9044 s          0 s       1252 s       6486 s          0 s
       #2  2394 MHz       5533 s          0 s       1333 s       9913 s          0 s
       
  Memory: 6.7913818359375 GB (3302.7734375 MB free)
  Uptime: 184.0 sec
  Load Avg:  1.18408203125  0.8154296875  0.34716796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       9734 s          0 s       1269 s       9425 s          0 s
       #2  2394 MHz       8479 s          0 s       1380 s      10571 s          0 s
       
  Memory: 6.7913818359375 GB (3256.390625 MB free)
  Uptime: 221.0 sec
  Load Avg:  1.0927734375  0.84033203125  0.376953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 21:31
* Package commit: f6d3a7
* Julia commit: 96786e
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.733 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   6.060 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   8.500 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   6.000 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 895.455 ns (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.033 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   2.078 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.020 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 437.874 ns (5%) |         |                |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       9044 s          0 s       1252 s       6486 s          0 s
       #2  2394 MHz       5533 s          0 s       1333 s       9913 s          0 s
       
  Memory: 6.7913818359375 GB (3302.7734375 MB free)
  Uptime: 184.0 sec
  Load Avg:  1.18408203125  0.8154296875  0.34716796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 21:32
* Package commit: 5373a3
* Julia commit: 96786e
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.700 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   4.900 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   8.500 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   5.300 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 899.000 ns (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.000 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   2.099 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  | 900.000 ns (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 399.000 ns (5%) |         |                |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz       9734 s          0 s       1269 s       9425 s          0 s
       #2  2394 MHz       8479 s          0 s       1380 s      10571 s          0 s
       
  Memory: 6.7913818359375 GB (3256.390625 MB free)
  Uptime: 221.0 sec
  Load Avg:  1.0927734375  0.84033203125  0.376953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:               63
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:            2
    CPU MHz:             2394.455
    BogoMIPS:            4788.91
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            30720K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

