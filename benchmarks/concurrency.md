# Granian benchmarks

## Concurrency

Run at: Tue 19 Mar 2024, 15:08    
Environment: Apple Silicon M2 Pro (CPUs: 10)    
Python version: 3.11    
Granian version: 1.2.0    

### ASGI

| Mode | Processes | Threads | Blocking Threads | Total requests | RPS | avg latency | max latency |
| --- | --- | --- | --- | --- | --- | --- | --- |
| workers (c80) | 1 | 1 | 1 | 1472105 | 97482 | 0.809ms | 3.893ms |
| runtime (c80) | 1 | 1 | 1 | 929318 | 61534 | 1.284ms | 5.248ms |
| workers (c80) | 1 | 2 | 1 | 1400457 | 92736 | 0.851ms | 4.812ms |
| runtime (c80) | 1 | 2 | 1 | 925279 | 61272 | 1.289ms | 6.294ms |
| workers (c80) | 1 | 4 | 1 | 1290774 | 85475 | 0.94ms | 4.845ms |
| runtime (c80) | 1 | 4 | 1 | 858927 | 57254 | 1.386ms | 6.501ms |
| workers (c320) | 2 | 1 | 1 | 2226178 | 147378 | 2.11ms | 19.675ms |
| runtime (c160) | 2 | 1 | 1 | 1229094 | 81383 | 1.917ms | 9.647ms |
| workers (c640) | 2 | 2 | 1 | 2232483 | 148632 | 3.994ms | 25.4ms |
| runtime (c80) | 2 | 2 | 1 | 1294997 | 85754 | 0.91ms | 7.112ms |
| workers (c640) | 2 | 4 | 1 | 2034157 | 135182 | 4.537ms | 77.928ms |
| runtime (c80) | 2 | 4 | 1 | 1184470 | 78441 | 0.995ms | 9.285ms |
| **workers (c640)** | **4** | **1** | **1** | **2248614** | **149510** | **3.882ms** | **27.427ms** |
| runtime (c160) | 4 | 1 | 1 | 1764747 | 116853 | 1.326ms | 8.362ms |
| workers (c640) | 4 | 2 | 1 | 2241413 | 148522 | 4.233ms | 79.033ms |
| runtime (c160) | 4 | 2 | 1 | 1826775 | 121757 | 1.264ms | 16.418ms |
| workers (c640) | 4 | 4 | 1 | 2080516 | 138148 | 4.197ms | 128.194ms |
| runtime (c640) | 4 | 4 | 1 | 2131702 | 141252 | 3.736ms | 63.085ms |
| workers (c640) | 5 | 1 | 1 | 2231262 | 148035 | 3.86ms | 25.37ms |
| runtime (c320) | 5 | 1 | 1 | 1883522 | 125521 | 2.463ms | 17.453ms |
| workers (c640) | 5 | 2 | 1 | 2186091 | 144838 | 4.32ms | 96.888ms |
| runtime (c640) | 5 | 2 | 1 | 2111729 | 139929 | 3.968ms | 48.927ms |
| workers (c80) | 5 | 4 | 1 | 1483865 | 98288 | 3.024ms | 208.876ms |
| **runtime (c640)** | **5** | **4** | **1** | **2136709** | **141488** | **3.623ms** | **47.921ms** |
| workers (c640) | 10 | 1 | 1 | 2148887 | 143017 | 4.803ms | 112.821ms |
| runtime (c640) | 10 | 1 | 1 | 2020660 | 134116 | 6.486ms | 159.138ms |
| workers (c80) | 10 | 2 | 1 | 1306685 | 86531 | 13.676ms | 254.613ms |
| runtime (c640) | 10 | 2 | 1 | 2068880 | 137170 | 4.371ms | 134.885ms |
| workers (c160) | 10 | 4 | 1 | 1462070 | 96981 | 7.947ms | 375.369ms |
| runtime (c640) | 10 | 4 | 1 | 2071664 | 137285 | 3.948ms | 136.938ms |

### RSGI

| Mode | Processes | Threads | Blocking Threads | Total requests | RPS | avg latency | max latency |
| --- | --- | --- | --- | --- | --- | --- | --- |
| workers (c80) | 1 | 1 | 1 | 1411999 | 93504 | 0.842ms | 4.028ms |
| runtime (c80) | 1 | 1 | 1 | 1117334 | 73994 | 1.063ms | 5.188ms |
| workers (c320) | 1 | 2 | 1 | 2181023 | 145355 | 2.154ms | 18.989ms |
| runtime (c80) | 1 | 2 | 1 | 1422249 | 94181 | 0.833ms | 5.471ms |
| workers (c640) | 1 | 4 | 1 | 1956799 | 130351 | 4.823ms | 22.841ms |
| runtime (c160) | 1 | 4 | 1 | 949719 | 63295 | 2.524ms | 10.488ms |
| workers (c320) | 2 | 1 | 1 | 2157642 | 143791 | 2.177ms | 15.951ms |
| runtime (c80) | 2 | 1 | 1 | 1419978 | 94658 | 0.823ms | 4.059ms |
| **workers (c640)** | **2** | **2** | **1** | **2267309** | **151004** | **3.955ms** | **26.224ms** |
| runtime (c80) | 2 | 2 | 1 | 1341545 | 88836 | 0.877ms | 5.79ms |
| workers (c640) | 2 | 4 | 1 | 2274646 | 150934 | 3.648ms | 23.543ms |
| runtime (c320) | 2 | 4 | 1 | 1348524 | 89862 | 3.539ms | 16.592ms |
| workers (c640) | 4 | 1 | 1 | 2228900 | 148432 | 4.03ms | 22.629ms |
| runtime (c320) | 4 | 1 | 1 | 1837278 | 122439 | 2.532ms | 17.346ms |
| workers (c640) | 4 | 2 | 1 | 2268179 | 150527 | 4.008ms | 73.672ms |
| runtime (c160) | 4 | 2 | 1 | 1961918 | 130743 | 1.156ms | 9.574ms |
| workers (c640) | 4 | 4 | 1 | 2173476 | 144207 | 3.662ms | 87.553ms |
| **runtime (c640)** | **4** | **4** | **1** | **2183501** | **144934** | **3.671ms** | **62.258ms** |
| workers (c320) | 5 | 1 | 1 | 2215795 | 147456 | 1.981ms | 28.612ms |
| runtime (c160) | 5 | 1 | 1 | 1995860 | 133013 | 1.153ms | 10.997ms |
| workers (c640) | 5 | 2 | 1 | 2209641 | 146340 | 5.068ms | 186.313ms |
| runtime (c640) | 5 | 2 | 1 | 2137135 | 141609 | 4.052ms | 54.876ms |
| workers (c640) | 5 | 4 | 1 | 2126848 | 140957 | 3.799ms | 130.24ms |
| runtime (c640) | 5 | 4 | 1 | 2162262 | 143413 | 3.78ms | 98.119ms |
| workers (c640) | 10 | 1 | 1 | 2179120 | 144416 | 4.315ms | 82.551ms |
| runtime (c640) | 10 | 1 | 1 | 2096533 | 138856 | 6.003ms | 125.325ms |
| workers (c80) | 10 | 2 | 1 | 1411899 | 93526 | 9.769ms | 250.795ms |
| runtime (c640) | 10 | 2 | 1 | 2127853 | 141027 | 4.507ms | 143.035ms |
| workers (c160) | 10 | 4 | 1 | 1492358 | 98902 | 7.561ms | 374.871ms |
| runtime (c640) | 10 | 4 | 1 | 2107436 | 139785 | 3.807ms | 68.263ms |

### WSGI

| Mode | Processes | Threads | Blocking Threads | Total requests | RPS | avg latency | max latency |
| --- | --- | --- | --- | --- | --- | --- | --- |
| workers (c80) | 1 | 1 | 1 | 1531035 | 101384 | 0.781ms | 5.844ms |
| runtime (c160) | 1 | 1 | 1 | 1538601 | 101879 | 1.562ms | 8.726ms |
| workers (c640) | 1 | 1 | 2 | 1331197 | 88103 | 7.19ms | 25.729ms |
| runtime (c640) | 1 | 1 | 2 | 1420760 | 94034 | 6.762ms | 23.653ms |
| workers (c160) | 1 | 1 | 4 | 1173581 | 77714 | 2.044ms | 11.113ms |
| runtime (c160) | 1 | 1 | 4 | 1185259 | 78482 | 2.032ms | 9.908ms |
| workers (c640) | 1 | 2 | 1 | 1190184 | 79284 | 8.027ms | 24.066ms |
| runtime (c160) | 1 | 2 | 1 | 2122357 | 140535 | 1.103ms | 8.09ms |
| workers (c640) | 1 | 2 | 2 | 1265033 | 84268 | 7.548ms | 26.557ms |
| runtime (c80) | 1 | 2 | 2 | 1366693 | 90505 | 0.88ms | 4.658ms |
| workers (c320) | 1 | 2 | 4 | 1099795 | 72813 | 4.382ms | 17.27ms |
| runtime (c80) | 1 | 2 | 4 | 1201405 | 79555 | 1.002ms | 5.655ms |
| workers (c80) | 1 | 4 | 1 | 1224406 | 81083 | 1.021ms | 7.549ms |
| runtime (c80) | 1 | 4 | 1 | 1795258 | 118888 | 0.652ms | 5.828ms |
| workers (c80) | 1 | 4 | 2 | 1077639 | 71363 | 1.157ms | 6.695ms |
| runtime (c320) | 1 | 4 | 2 | 1255215 | 83099 | 3.831ms | 19.019ms |
| workers (c160) | 1 | 4 | 4 | 1113421 | 73724 | 2.191ms | 10.89ms |
| runtime (c640) | 1 | 4 | 4 | 1149282 | 76560 | 8.308ms | 24.442ms |
| workers (c80) | 2 | 1 | 1 | 2172513 | 143867 | 0.513ms | 3.766ms |
| runtime (c640) | 2 | 1 | 1 | 2171779 | 143727 | 4.327ms | 22.913ms |
| workers (c640) | 2 | 1 | 2 | 2223326 | 147178 | 4.264ms | 22.327ms |
| runtime (c320) | 2 | 1 | 2 | 2201404 | 145736 | 2.112ms | 17.839ms |
| workers (c320) | 2 | 1 | 4 | 1768073 | 117057 | 2.686ms | 19.285ms |
| runtime (c320) | 2 | 1 | 4 | 1764833 | 117585 | 2.688ms | 15.706ms |
| workers (c640) | 2 | 2 | 1 | 2230845 | 148442 | 3.948ms | 22.191ms |
| runtime (c320) | 2 | 2 | 1 | 2253571 | 149183 | 1.927ms | 19.215ms |
| workers (c640) | 2 | 2 | 2 | 2001567 | 133233 | 4.518ms | 27.879ms |
| runtime (c640) | 2 | 2 | 2 | 2237970 | 148899 | 3.875ms | 24.096ms |
| workers (c160) | 2 | 2 | 4 | 1459247 | 96620 | 1.67ms | 11.944ms |
| runtime (c640) | 2 | 2 | 4 | 2196268 | 146073 | 3.954ms | 24.819ms |
| workers (c640) | 2 | 4 | 1 | 1767834 | 117570 | 5.433ms | 75.389ms |
| runtime (c320) | 2 | 4 | 1 | 2233091 | 148568 | 1.768ms | 19.332ms |
| workers (c320) | 2 | 4 | 2 | 1490862 | 99355 | 3.218ms | 23.559ms |
| runtime (c640) | 2 | 4 | 2 | 2233460 | 147870 | 3.392ms | 32.852ms |
| workers (c160) | 2 | 4 | 4 | 1440232 | 95349 | 1.878ms | 88.268ms |
| runtime (c640) | 2 | 4 | 4 | 1979403 | 131128 | 4.175ms | 25.368ms |
| workers (c320) | 4 | 1 | 1 | 2289337 | 151557 | 1.904ms | 17.528ms |
| runtime (c160) | 4 | 1 | 1 | 2292997 | 151826 | 0.942ms | 11.375ms |
| workers (c640) | 4 | 1 | 2 | 2264994 | 150704 | 3.79ms | 22.417ms |
| runtime (c640) | 4 | 1 | 2 | 2276127 | 151380 | 3.768ms | 24.604ms |
| workers (c640) | 4 | 1 | 4 | 2221442 | 147599 | 3.791ms | 22.506ms |
| runtime (c640) | 4 | 1 | 4 | 2242754 | 148910 | 3.821ms | 26.634ms |
| workers (c640) | 4 | 2 | 1 | 2278037 | 151358 | 3.834ms | 54.723ms |
| runtime (c320) | 4 | 2 | 1 | 2284117 | 151531 | 1.906ms | 48.789ms |
| workers (c640) | 4 | 2 | 2 | 2216991 | 146917 | 4.546ms | 85.882ms |
| runtime (c640) | 4 | 2 | 2 | 2276864 | 150961 | 3.627ms | 38.945ms |
| workers (c640) | 4 | 2 | 4 | 2034538 | 135153 | 4.742ms | 99.635ms |
| runtime (c640) | 4 | 2 | 4 | 2170743 | 143723 | 3.681ms | 59.116ms |
| workers (c80) | 4 | 4 | 1 | 1499563 | 99297 | 13.849ms | 258.47ms |
| runtime (c640) | 4 | 4 | 1 | 2255686 | 149478 | 3.519ms | 39.328ms |
| workers (c80) | 4 | 4 | 2 | 1334184 | 88409 | 10.222ms | 282.733ms |
| runtime (c640) | 4 | 4 | 2 | 2206503 | 146332 | 3.416ms | 70.791ms |
| workers (c160) | 4 | 4 | 4 | 1414347 | 93849 | 8.378ms | 339.89ms |
| runtime (c640) | 4 | 4 | 4 | 2095334 | 138736 | 3.575ms | 51.54ms |
| **workers (c160)** | **5** | **1** | **1** | **2299404** | **152246** | **0.935ms** | **9.328ms** |
| runtime (c320) | 5 | 1 | 1 | 2283078 | 151921 | 1.915ms | 17.687ms |
| workers (c640) | 5 | 1 | 2 | 2277170 | 151155 | 3.777ms | 26.321ms |
| runtime (c640) | 5 | 1 | 2 | 2283252 | 151467 | 3.837ms | 31.866ms |
| workers (c640) | 5 | 1 | 4 | 2230754 | 147775 | 3.996ms | 47.481ms |
| runtime (c640) | 5 | 1 | 4 | 2237231 | 148159 | 4.049ms | 41.956ms |
| workers (c640) | 5 | 2 | 1 | 2263438 | 150183 | 3.832ms | 48.856ms |
| runtime (c640) | 5 | 2 | 1 | 2286014 | 151344 | 3.67ms | 41.313ms |
| workers (c640) | 5 | 2 | 2 | 2125966 | 140932 | 4.76ms | 113.512ms |
| runtime (c640) | 5 | 2 | 2 | 2248842 | 149439 | 3.588ms | 52.371ms |
| workers (c80) | 5 | 2 | 4 | 1434767 | 94984 | 9.639ms | 250.261ms |
| runtime (c640) | 5 | 2 | 4 | 2108567 | 139671 | 3.769ms | 50.505ms |
| workers (c80) | 5 | 4 | 1 | 1503811 | 99552 | 7.747ms | 375.127ms |
| runtime (c640) | 5 | 4 | 1 | 2250059 | 149019 | 3.473ms | 39.089ms |
| workers (c80) | 5 | 4 | 2 | 1361092 | 90112 | 10.666ms | 374.913ms |
| runtime (c640) | 5 | 4 | 2 | 2176351 | 144173 | 3.509ms | 71.264ms |
| workers (c160) | 5 | 4 | 4 | 1469777 | 97288 | 4.499ms | 249.513ms |
| runtime (c640) | 5 | 4 | 4 | 2052086 | 136093 | 3.693ms | 51.207ms |
| workers (c640) | 10 | 1 | 1 | 2287452 | 151760 | 4.493ms | 59.651ms |
| **runtime (c640)** | **10** | **1** | **1** | **2302335** | **152476** | **4.18ms** | **53.213ms** |
| workers (c640) | 10 | 1 | 2 | 2235166 | 147962 | 4.179ms | 75.248ms |
| runtime (c640) | 10 | 1 | 2 | 2216916 | 146880 | 4.312ms | 96.285ms |
| workers (c640) | 10 | 1 | 4 | 2063897 | 136797 | 4.413ms | 73.977ms |
| runtime (c640) | 10 | 1 | 4 | 2067111 | 137054 | 4.612ms | 107.718ms |
| workers (c640) | 10 | 2 | 1 | 2171946 | 143875 | 4.066ms | 86.412ms |
| runtime (c640) | 10 | 2 | 1 | 2204148 | 146054 | 3.561ms | 72.654ms |
| workers (c640) | 10 | 2 | 2 | 2018679 | 133761 | 4.646ms | 119.943ms |
| runtime (c640) | 10 | 2 | 2 | 2106616 | 139680 | 3.79ms | 87.341ms |
| workers (c80) | 10 | 2 | 4 | 1502379 | 99545 | 3.565ms | 250.65ms |
| runtime (c80) | 10 | 2 | 4 | 1434102 | 95160 | 5.538ms | 250.904ms |
| workers (c640) | 10 | 4 | 1 | 1997207 | 132329 | 4.341ms | 103.345ms |
| runtime (c640) | 10 | 4 | 1 | 2154127 | 142812 | 3.593ms | 77.126ms |
| workers (c80) | 10 | 4 | 2 | 1377866 | 91340 | 6.694ms | 374.844ms |
| runtime (c640) | 10 | 4 | 2 | 2041386 | 135175 | 3.782ms | 68.789ms |
| workers (c160) | 10 | 4 | 4 | 1475546 | 97821 | 1.951ms | 75.6ms |
| runtime (c80) | 10 | 4 | 4 | 1424839 | 94454 | 4.106ms | 180.078ms |
