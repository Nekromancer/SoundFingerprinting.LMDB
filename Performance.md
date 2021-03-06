``` ini

BenchmarkDotNet=v0.12.0, OS=Windows 10.0.18363
Intel Core i5-9600K CPU 3.70GHz (Coffee Lake), 1 CPU, 6 logical and 6 physical cores
.NET Core SDK=3.1.101
  [Host]     : .NET Core 3.1.1 (CoreCLR 4.700.19.60701, CoreFX 4.700.19.60801), X64 RyuJIT
  Job-CAKGWO : .NET Core 3.1.1 (CoreCLR 4.700.19.60701, CoreFX 4.700.19.60801), X64 RyuJIT
  Job-HMKIWF : .NET Framework 4.8 (4.8.4121.0), X64 RyuJIT

Platform=X64  

```
|               Method |     Toolchain |  audioFile |       Mean |    Error |   StdDev | Ratio | RatioSD |       Gen 0 |       Gen 1 |      Gen 2 |  Allocated |
|--------------------- |-------------- |----------- |-----------:|---------:|---------:|------:|--------:|------------:|------------:|-----------:|-----------:|
| **InMemoryRecognitions** | **.NET Core 3.1** | **151041.wav** |   **990.5 ms** | **16.64 ms** | **15.56 ms** |  **1.00** |    **0.00** |  **17000.0000** |   **8000.0000** |  **3000.0000** |  **469.14 MB** |
|     LMDBRecognitions | .NET Core 3.1 | 151041.wav | 1,199.1 ms | 12.41 ms | 11.00 ms |  1.21 |    0.02 | 143000.0000 |  61000.0000 |  3000.0000 | 1147.32 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 | 151041.wav |   939.3 ms |  6.96 ms |  6.51 ms |  1.00 |    0.00 |  18000.0000 |   8000.0000 |  3000.0000 |   472.2 MB |
|     LMDBRecognitions |         net48 | 151041.wav | 1,369.3 ms | 21.74 ms | 20.34 ms |  1.46 |    0.02 | 166000.0000 |  57000.0000 |  4000.0000 | 1328.26 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| **InMemoryRecognitions** | **.NET Core 3.1** | **153201.wav** |   **910.0 ms** | **17.89 ms** | **16.74 ms** |  **1.00** |    **0.00** |  **16000.0000** |   **8000.0000** |  **3000.0000** |  **432.29 MB** |
|     LMDBRecognitions | .NET Core 3.1 | 153201.wav | 1,046.0 ms | 10.57 ms |  9.89 ms |  1.15 |    0.02 |  87000.0000 |  28000.0000 |  3000.0000 |  786.78 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 | 153201.wav |   864.4 ms | 12.59 ms | 11.78 ms |  1.00 |    0.00 |  16000.0000 |   6000.0000 |  3000.0000 |  434.45 MB |
|     LMDBRecognitions |         net48 | 153201.wav | 1,139.9 ms | 13.53 ms | 12.66 ms |  1.32 |    0.03 | 109000.0000 |  33000.0000 |  3000.0000 |  954.13 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| **InMemoryRecognitions** | **.NET Core 3.1** | **157095.wav** | **1,002.5 ms** | **13.67 ms** | **12.78 ms** |  **1.00** |    **0.00** |  **18000.0000** |   **8000.0000** |  **3000.0000** |  **475.84 MB** |
|     LMDBRecognitions | .NET Core 3.1 | 157095.wav | 1,281.8 ms | 23.18 ms | 21.68 ms |  1.28 |    0.03 | 160000.0000 |  72000.0000 |  3000.0000 | 1269.87 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 | 157095.wav |   956.9 ms | 11.17 ms | 10.45 ms |  1.00 |    0.00 |  18000.0000 |   8000.0000 |  3000.0000 |  478.18 MB |
|     LMDBRecognitions |         net48 | 157095.wav | 1,498.4 ms | 29.54 ms | 38.42 ms |  1.55 |    0.04 | 213000.0000 |  92000.0000 |  4000.0000 | 1612.19 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| **InMemoryRecognitions** | **.NET Core 3.1** | **161344.wav** |   **786.5 ms** |  **8.01 ms** |  **7.49 ms** |  **1.00** |    **0.00** |  **13000.0000** |   **5000.0000** |  **2000.0000** |  **383.23 MB** |
|     LMDBRecognitions | .NET Core 3.1 | 161344.wav |   935.4 ms |  9.93 ms |  9.28 ms |  1.19 |    0.01 |  74000.0000 |  23000.0000 |  3000.0000 |  691.53 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 | 161344.wav |   747.1 ms |  4.37 ms |  4.09 ms |  1.00 |    0.00 |  13000.0000 |   5000.0000 |  2000.0000 |   385.1 MB |
|     LMDBRecognitions |         net48 | 161344.wav | 1,050.4 ms | 20.78 ms | 26.28 ms |  1.41 |    0.03 |  95000.0000 |  19000.0000 |  3000.0000 |  846.81 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| **InMemoryRecognitions** | **.NET Core 3.1** |  **50996.wav** | **1,032.9 ms** | **14.84 ms** | **13.88 ms** |  **1.00** |    **0.00** |  **17000.0000** |   **9000.0000** |  **3000.0000** |  **481.04 MB** |
|     LMDBRecognitions | .NET Core 3.1 |  50996.wav | 1,234.1 ms | 17.01 ms | 15.92 ms |  1.19 |    0.02 | 139000.0000 |  55000.0000 |  4000.0000 |  1121.3 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 |  50996.wav |   959.4 ms |  9.56 ms |  7.98 ms |  1.00 |    0.00 |  18000.0000 |   8000.0000 |  3000.0000 |  484.33 MB |
|     LMDBRecognitions |         net48 |  50996.wav | 1,388.0 ms | 26.81 ms | 26.33 ms |  1.45 |    0.03 | 163000.0000 |  45000.0000 |  4000.0000 | 1329.88 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| **InMemoryRecognitions** | **.NET Core 3.1** |  **52158.wav** | **3,465.7 ms** | **28.81 ms** | **24.06 ms** |  **1.00** |    **0.00** |  **50000.0000** |  **16000.0000** |  **4000.0000** | **1490.59 MB** |
|     LMDBRecognitions | .NET Core 3.1 |  52158.wav | 5,127.7 ms | 56.82 ms | 53.15 ms |  1.48 |    0.01 | 620000.0000 | 263000.0000 |  5000.0000 | 6527.39 MB |
|                      |               |            |            |          |          |       |         |             |             |            |            |
| InMemoryRecognitions |         net48 |  52158.wav | 3,242.3 ms | 35.68 ms | 33.38 ms |  1.00 |    0.00 |  51000.0000 |  17000.0000 |  4000.0000 | 1497.76 MB |
|     LMDBRecognitions |         net48 |  52158.wav | 7,217.5 ms | 89.75 ms | 74.94 ms |  2.22 |    0.03 | 911000.0000 | 319000.0000 | 23000.0000 |    8510 MB |

