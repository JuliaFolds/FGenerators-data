# Benchmark result

* Pull request commit: [`be2c6eecfa43963974f35d86a1749fe37f607054`](https://github.com/JuliaFolds/FGenerators.jl/commit/be2c6eecfa43963974f35d86a1749fe37f607054)
* Pull request: <https://github.com/JuliaFolds/FGenerators.jl/pull/9> (Mention how to combine FGenerators with SplittablesBase)

# Judge result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Aug 2020 - 21:40
    - Baseline: 23 Aug 2020 - 21:40
* Package commits:
    - Target: 492685
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` | 1.14 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` | 1.18 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   | 1.17 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 1.13 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  | 1.07 (5%) :x: |   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10296 s          0 s       1459 s       8933 s          0 s
       #2  2095 MHz       5104 s          0 s       1460 s      14493 s          0 s
       
  Memory: 6.764881134033203 GB (3164.09765625 MB free)
  Uptime: 227.0 sec
  Load Avg:  1.1484375  0.64794921875  0.27392578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      13111 s          0 s       1496 s      10000 s          0 s
       #2  2095 MHz       6192 s          0 s       1499 s      17294 s          0 s
       
  Memory: 6.764881134033203 GB (3157.546875 MB free)
  Uptime: 266.0 sec
  Load Avg:  1.07470703125  0.693359375  0.30517578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 21:40
* Package commit: 492685
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.601 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   6.750 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.201 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   6.875 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.017 μs (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.567 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   1.840 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.280 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 608.580 ns (5%) |         |                |             |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10296 s          0 s       1459 s       8933 s          0 s
       #2  2095 MHz       5104 s          0 s       1460 s      14493 s          0 s
       
  Memory: 6.764881134033203 GB (3164.09765625 MB free)
  Uptime: 227.0 sec
  Load Avg:  1.1484375  0.64794921875  0.27392578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/FGenerators.jl/FGenerators.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 21:40
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.900 μs (5%) |         | 24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :fgen"]` |   5.700 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.101 μs (5%) |         | 26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :fgen"]`   |   5.901 μs (5%) |         | 32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 900.000 ns (5%) |         | 704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.500 μs (5%) |         | 880 bytes (1%) |          30 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :fgen"]`       |   1.800 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.200 μs (5%) |         |                |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :fgen"]`  | 600.000 ns (5%) |         |                |             |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      13111 s          0 s       1496 s      10000 s          0 s
       #2  2095 MHz       6192 s          0 s       1499 s      17294 s          0 s
       
  Memory: 6.764881134033203 GB (3157.546875 MB free)
  Uptime: 266.0 sec
  Load Avg:  1.07470703125  0.693359375  0.30517578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
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
    CPU MHz:             2095.229
    BogoMIPS:            4190.45
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

