
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

## Output of this test

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
# Warmup Iteration   1: 0.524 ns/op
# Warmup Iteration   2: 0.522 ns/op
# Warmup Iteration   3: 0.536 ns/op
# Warmup Iteration   4: 0.522 ns/op
# Warmup Iteration   5: 0.523 ns/op
Iteration   1: 0.524 ns/op
Iteration   2: 0.523 ns/op
Iteration   3: 0.522 ns/op
Iteration   4: 0.533 ns/op
Iteration   5: 0.525 ns/op

# Run progress: 10.00% complete, ETA 00:15:06
# Fork: 2 of 5
# Warmup Iteration   1: 0.522 ns/op
# Warmup Iteration   2: 0.528 ns/op
# Warmup Iteration   3: 0.528 ns/op
# Warmup Iteration   4: 0.522 ns/op
# Warmup Iteration   5: 0.525 ns/op
Iteration   1: 0.610 ns/op
Iteration   2: 0.681 ns/op
Iteration   3: 0.596 ns/op
Iteration   4: 0.582 ns/op
Iteration   5: 0.565 ns/op

# Run progress: 20.00% complete, ETA 00:13:24
# Fork: 3 of 5
# Warmup Iteration   1: 0.566 ns/op
# Warmup Iteration   2: 0.593 ns/op
# Warmup Iteration   3: 0.553 ns/op
# Warmup Iteration   4: 0.546 ns/op
# Warmup Iteration   5: 0.534 ns/op
Iteration   1: 0.532 ns/op
Iteration   2: 0.561 ns/op
Iteration   3: 0.562 ns/op
Iteration   4: 0.534 ns/op
Iteration   5: 0.558 ns/op

# Run progress: 30.00% complete, ETA 00:11:44
# Fork: 4 of 5
# Warmup Iteration   1: 0.572 ns/op
# Warmup Iteration   2: 0.551 ns/op
# Warmup Iteration   3: 0.721 ns/op
# Warmup Iteration   4: 0.637 ns/op
# Warmup Iteration   5: 0.638 ns/op
Iteration   1: 0.651 ns/op
Iteration   2: 0.590 ns/op
Iteration   3: 0.613 ns/op
Iteration   4: 0.748 ns/op
Iteration   5: 0.709 ns/op

# Run progress: 40.00% complete, ETA 00:10:03
# Fork: 5 of 5
# Warmup Iteration   1: 0.578 ns/op
# Warmup Iteration   2: 0.630 ns/op
# Warmup Iteration   3: 0.559 ns/op
# Warmup Iteration   4: 0.581 ns/op
# Warmup Iteration   5: 0.586 ns/op
Iteration   1: 0.556 ns/op
Iteration   2: 0.571 ns/op
Iteration   3: 0.570 ns/op
Iteration   4: 0.561 ns/op
Iteration   5: 0.540 ns/op


Result "com.dd.MyBenchmark.concatFinalStrings":
  0.581 ±(99.9%) 0.045 ns/op [Average]
  (min, avg, max) = (0.522, 0.581, 0.748), stdev = 0.060
  CI (99.9%): [0.536, 0.626] (assumes normal distribution)


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
# Benchmark: com.dd.MyBenchmark.concatNonFinalStrings

# Run progress: 50.00% complete, ETA 00:08:22
# Fork: 1 of 5
# Warmup Iteration   1: 9.142 ns/op
# Warmup Iteration   2: 9.041 ns/op
# Warmup Iteration   3: 7.883 ns/op
# Warmup Iteration   4: 8.673 ns/op
# Warmup Iteration   5: 8.072 ns/op
Iteration   1: 7.019 ns/op
Iteration   2: 7.158 ns/op
Iteration   3: 7.442 ns/op
Iteration   4: 7.126 ns/op
Iteration   5: 7.017 ns/op

# Run progress: 60.00% complete, ETA 00:06:42
# Fork: 2 of 5
# Warmup Iteration   1: 7.600 ns/op
# Warmup Iteration   2: 7.105 ns/op
# Warmup Iteration   3: 6.846 ns/op
# Warmup Iteration   4: 6.897 ns/op
# Warmup Iteration   5: 6.901 ns/op
Iteration   1: 6.957 ns/op
Iteration   2: 6.891 ns/op
Iteration   3: 6.843 ns/op
Iteration   4: 6.830 ns/op
Iteration   5: 6.870 ns/op

# Run progress: 70.00% complete, ETA 00:05:01
# Fork: 3 of 5
# Warmup Iteration   1: 7.465 ns/op
# Warmup Iteration   2: 7.140 ns/op
# Warmup Iteration   3: 6.877 ns/op
# Warmup Iteration   4: 6.860 ns/op
# Warmup Iteration   5: 6.833 ns/op
Iteration   1: 6.960 ns/op
Iteration   2: 6.849 ns/op
Iteration   3: 6.892 ns/op
Iteration   4: 6.871 ns/op
Iteration   5: 6.979 ns/op

# Run progress: 80.00% complete, ETA 00:03:21
# Fork: 4 of 5
# Warmup Iteration   1: 7.844 ns/op
# Warmup Iteration   2: 7.558 ns/op
# Warmup Iteration   3: 7.102 ns/op
# Warmup Iteration   4: 6.887 ns/op
# Warmup Iteration   5: 6.866 ns/op
Iteration   1: 6.873 ns/op
Iteration   2: 6.876 ns/op
Iteration   3: 6.830 ns/op
Iteration   4: 6.869 ns/op
Iteration   5: 6.836 ns/op

# Run progress: 90.00% complete, ETA 00:01:40
# Fork: 5 of 5
# Warmup Iteration   1: 7.439 ns/op
# Warmup Iteration   2: 7.124 ns/op
# Warmup Iteration   3: 7.696 ns/op
# Warmup Iteration   4: 8.285 ns/op
# Warmup Iteration   5: 7.222 ns/op
Iteration   1: 6.978 ns/op
Iteration   2: 6.963 ns/op
Iteration   3: 6.966 ns/op
Iteration   4: 6.934 ns/op
Iteration   5: 6.916 ns/op


Result "com.dd.MyBenchmark.concatNonFinalStrings":
  6.950 ±(99.9%) 0.100 ns/op [Average]
  (min, avg, max) = (6.830, 6.950, 7.442), stdev = 0.134
  CI (99.9%): [6.850, 7.050] (assumes normal distribution)


# Run complete. Total time: 00:16:46

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

Benchmark                          Mode  Cnt  Score   Error  Units
MyBenchmark.concatFinalStrings     avgt   25  0.581 ± 0.045  ns/op
MyBenchmark.concatNonFinalStrings  avgt   25  6.950 ± 0.100  ns/op
```