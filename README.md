
# Final vs Non-Final Variable JMH

## How to create JMH project?

Run below command,
```
mvn archetype:generate \
          -DinteractiveMode=false \
          -DarchetypeGroupId=org.openjdk.jmh \
          -DarchetypeArtifactId=jmh-java-benchmark-archetype \
          -DgroupId=com.dd \
          -DartifactId=final-benchmark-jmh \
          -Dversion=1.0

```
Add the tests to MyBenchmark.java

## Run the JMH 
1. Run `mvn clean install`
2. Run `java -jar ./target/benchmarks.jar`

## After adding intern()

```
Jays-MacBook-Air:final-benchmark-jmh jay$ java -jar ./target/benchmarks.jar
# JMH version: 1.35
# VM version: JDK 17, Java HotSpot(TM) 64-Bit Server VM, 17+35-LTS-2724
# VM invoker: /Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home/bin/java
# VM options: <none>
# Blackhole mode: compiler (auto-detected, use -Djmh.blackhole.autoDetect=false to disable)
# Warmup: 5 iterations, 10 s each
# Measurement: 5 iterations, 10 s each
# Timeout: 10 min per iteration
# Threads: 1 thread, will synchronize iterations
# Benchmark mode: Average time, time/op
# Benchmark: com.dd.MyBenchmark.concatFinalStrings

# Run progress: 0.00% complete, ETA 00:16:40
# Fork: 1 of 5
# Warmup Iteration   1: 21.446 ns/op
# Warmup Iteration   2: 16.709 ns/op
# Warmup Iteration   3: 9.476 ns/op
# Warmup Iteration   4: 11.335 ns/op
# Warmup Iteration   5: 9.318 ns/op
Iteration   1: 8.819 ns/op
Iteration   2: 9.026 ns/op
Iteration   3: 7.812 ns/op
Iteration   4: 7.245 ns/op
Iteration   5: 7.676 ns/op

# Run progress: 10.00% complete, ETA 00:15:08
# Fork: 2 of 5
# Warmup Iteration   1: 15.732 ns/op
# Warmup Iteration   2: 13.955 ns/op
# Warmup Iteration   3: 7.088 ns/op
# Warmup Iteration   4: 7.325 ns/op
# Warmup Iteration   5: 7.099 ns/op
Iteration   1: 6.932 ns/op
Iteration   2: 6.935 ns/op
Iteration   3: 6.942 ns/op
Iteration   4: 6.938 ns/op
Iteration   5: 7.166 ns/op

# Run progress: 20.00% complete, ETA 00:13:26
# Fork: 3 of 5
# Warmup Iteration   1: 13.920 ns/op
# Warmup Iteration   2: 12.612 ns/op
# Warmup Iteration   3: 6.869 ns/op
# Warmup Iteration   4: 6.809 ns/op
# Warmup Iteration   5: 6.862 ns/op
Iteration   1: 6.800 ns/op
Iteration   2: 7.127 ns/op
Iteration   3: 6.844 ns/op
Iteration   4: 6.775 ns/op
Iteration   5: 6.846 ns/op

# Run progress: 30.00% complete, ETA 00:11:44
# Fork: 4 of 5
# Warmup Iteration   1: 13.163 ns/op
# Warmup Iteration   2: 12.354 ns/op
# Warmup Iteration   3: 7.558 ns/op
# Warmup Iteration   4: 6.989 ns/op
# Warmup Iteration   5: 6.820 ns/op
Iteration   1: 6.944 ns/op
Iteration   2: 6.810 ns/op
Iteration   3: 6.905 ns/op
Iteration   4: 6.986 ns/op
Iteration   5: 6.844 ns/op

# Run progress: 40.00% complete, ETA 00:10:04
# Fork: 5 of 5
# Warmup Iteration   1: 13.223 ns/op
# Warmup Iteration   2: 12.570 ns/op
# Warmup Iteration   3: 6.856 ns/op
# Warmup Iteration   4: 6.837 ns/op
# Warmup Iteration   5: 6.880 ns/op
Iteration   1: 6.924 ns/op
Iteration   2: 7.145 ns/op
Iteration   3: 6.843 ns/op
Iteration   4: 6.823 ns/op
Iteration   5: 6.975 ns/op


Result "com.dd.MyBenchmark.concatFinalStrings":
  7.163 ±(99.9%) 0.440 ns/op [Average]
  (min, avg, max) = (6.775, 7.163, 9.026), stdev = 0.587
  CI (99.9%): [6.723, 7.603] (assumes normal distribution)


# JMH version: 1.35
# VM version: JDK 17, Java HotSpot(TM) 64-Bit Server VM, 17+35-LTS-2724
# VM invoker: /Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home/bin/java
# VM options: <none>
# Blackhole mode: compiler (auto-detected, use -Djmh.blackhole.autoDetect=false to disable)
# Warmup: 5 iterations, 10 s each
# Measurement: 5 iterations, 10 s each
# Timeout: 10 min per iteration
# Threads: 1 thread, will synchronize iterations
# Benchmark mode: Average time, time/op
# Benchmark: com.dd.MyBenchmark.concatNonFinalStringsUsingIntern

# Run progress: 50.00% complete, ETA 00:08:23
# Fork: 1 of 5
# Warmup Iteration   1: 236.001 ns/op
# Warmup Iteration   2: 217.817 ns/op
# Warmup Iteration   3: 231.010 ns/op
# Warmup Iteration   4: 231.629 ns/op
# Warmup Iteration   5: 237.042 ns/op
Iteration   1: 230.813 ns/op
Iteration   2: 233.684 ns/op
Iteration   3: 230.935 ns/op
Iteration   4: 230.791 ns/op
Iteration   5: 231.211 ns/op

# Run progress: 60.00% complete, ETA 00:06:42
# Fork: 2 of 5
# Warmup Iteration   1: 218.750 ns/op
# Warmup Iteration   2: 217.742 ns/op
# Warmup Iteration   3: 221.644 ns/op
# Warmup Iteration   4: 218.704 ns/op
# Warmup Iteration   5: 218.485 ns/op
Iteration   1: 222.500 ns/op
Iteration   2: 239.664 ns/op
Iteration   3: 239.326 ns/op
Iteration   4: 221.922 ns/op
Iteration   5: 219.518 ns/op

# Run progress: 70.00% complete, ETA 00:05:01
# Fork: 3 of 5
# Warmup Iteration   1: 215.285 ns/op
# Warmup Iteration   2: 217.464 ns/op
# Warmup Iteration   3: 217.375 ns/op
# Warmup Iteration   4: 216.848 ns/op
# Warmup Iteration   5: 229.450 ns/op
Iteration   1: 217.920 ns/op
Iteration   2: 220.256 ns/op
Iteration   3: 218.378 ns/op
Iteration   4: 216.847 ns/op
Iteration   5: 217.577 ns/op

# Run progress: 80.00% complete, ETA 00:03:21
# Fork: 4 of 5
# Warmup Iteration   1: 269.264 ns/op
# Warmup Iteration   2: 310.259 ns/op
# Warmup Iteration   3: 319.541 ns/op
# Warmup Iteration   4: 313.489 ns/op
# Warmup Iteration   5: 288.727 ns/op
Iteration   1: 276.781 ns/op
Iteration   2: 305.343 ns/op
Iteration   3: 259.341 ns/op
Iteration   4: 260.816 ns/op
Iteration   5: 283.004 ns/op

# Run progress: 90.00% complete, ETA 00:01:40
# Fork: 5 of 5
# Warmup Iteration   1: 285.002 ns/op
# Warmup Iteration   2: 257.080 ns/op
# Warmup Iteration   3: 285.492 ns/op
# Warmup Iteration   4: 263.258 ns/op
# Warmup Iteration   5: 259.848 ns/op
Iteration   1: 265.146 ns/op
Iteration   2: 362.576 ns/op
Iteration   3: 721.649 ns/op
Iteration   4: 306.731 ns/op
Iteration   5: 228.831 ns/op


Result "com.dd.MyBenchmark.concatNonFinalStringsUsingIntern":
  266.462 ±(99.9%) 75.962 ns/op [Average]
  (min, avg, max) = (216.847, 266.462, 721.649), stdev = 101.407
  CI (99.9%): [190.501, 342.424] (assumes normal distribution)


# Run complete. Total time: 00:16:45

REMEMBER: The numbers below are just data. To gain reusable insights, you need to follow up on
why the numbers are the way they are. Use profilers (see -prof, -lprof), design factorial
experiments, perform baseline and negative tests that provide experimental control, make sure
the benchmarking environment is safe on JVM/OS/HW level, ask for reviews from the domain experts.
Do not assume the numbers tell you what you want them to tell.

NOTE: Current JVM experimentally supports Compiler Blackholes, and they are in use. Please exercise
extra caution when trusting the results, look into the generated code to check the benchmark still
works, and factor in a small probability of new VM bugs. Additionally, while comparisons between
different JVMs are already problematic, the performance difference caused by different Blackhole
modes can be very significant. Please make sure you use the consistent Blackhole mode for comparisons.

Benchmark                                     Mode  Cnt    Score    Error  Units
MyBenchmark.concatFinalStrings                avgt   25    7.163 ±  0.440  ns/op
MyBenchmark.concatNonFinalStringsUsingIntern  avgt   25  266.462 ± 75.962  ns/op
```