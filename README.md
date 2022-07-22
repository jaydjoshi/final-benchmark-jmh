
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

## Output of this test for User Address

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
# Benchmark: com.dd.MyBenchmark.userWithFinalVariables

# Run progress: 0.00% complete, ETA 00:16:40
# Fork: 1 of 5
# Warmup Iteration   1: 13.756 ns/op
# Warmup Iteration   2: 15.136 ns/op
# Warmup Iteration   3: 29.090 ns/op
# Warmup Iteration   4: 12.428 ns/op
# Warmup Iteration   5: 11.391 ns/op
Iteration   1: 11.560 ns/op
Iteration   2: 11.732 ns/op
Iteration   3: 11.493 ns/op
Iteration   4: 11.367 ns/op
Iteration   5: 11.332 ns/op

# Run progress: 10.00% complete, ETA 00:15:07
# Fork: 2 of 5
# Warmup Iteration   1: 13.245 ns/op
# Warmup Iteration   2: 12.999 ns/op
# Warmup Iteration   3: 11.480 ns/op
# Warmup Iteration   4: 11.074 ns/op
# Warmup Iteration   5: 11.170 ns/op
Iteration   1: 10.905 ns/op
Iteration   2: 10.856 ns/op
Iteration   3: 10.781 ns/op
Iteration   4: 10.833 ns/op
Iteration   5: 11.251 ns/op

# Run progress: 20.00% complete, ETA 00:13:25
# Fork: 3 of 5
# Warmup Iteration   1: 14.786 ns/op
# Warmup Iteration   2: 12.587 ns/op
# Warmup Iteration   3: 10.933 ns/op
# Warmup Iteration   4: 11.167 ns/op
# Warmup Iteration   5: 11.018 ns/op
Iteration   1: 10.895 ns/op
Iteration   2: 11.013 ns/op
Iteration   3: 10.916 ns/op
Iteration   4: 11.206 ns/op
Iteration   5: 10.924 ns/op

# Run progress: 30.00% complete, ETA 00:11:44
# Fork: 4 of 5
# Warmup Iteration   1: 13.054 ns/op
# Warmup Iteration   2: 12.575 ns/op
# Warmup Iteration   3: 11.013 ns/op
# Warmup Iteration   4: 10.959 ns/op
# Warmup Iteration   5: 10.885 ns/op
Iteration   1: 10.891 ns/op
Iteration   2: 10.871 ns/op
Iteration   3: 10.820 ns/op
Iteration   4: 11.080 ns/op
Iteration   5: 10.880 ns/op

# Run progress: 40.00% complete, ETA 00:10:03
# Fork: 5 of 5
# Warmup Iteration   1: 13.136 ns/op
# Warmup Iteration   2: 12.485 ns/op
# Warmup Iteration   3: 10.848 ns/op
# Warmup Iteration   4: 10.826 ns/op
# Warmup Iteration   5: 11.014 ns/op
Iteration   1: 10.784 ns/op
Iteration   2: 10.978 ns/op
Iteration   3: 10.900 ns/op
Iteration   4: 11.036 ns/op
Iteration   5: 11.321 ns/op


Result "com.dd.MyBenchmark.userWithFinalVariables":
  11.065 ±(99.9%) 0.200 ns/op [Average]
  (min, avg, max) = (10.781, 11.065, 11.732), stdev = 0.267
  CI (99.9%): [10.865, 11.265] (assumes normal distribution)


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
# Benchmark: com.dd.MyBenchmark.userWithNonFinalVariables

# Run progress: 50.00% complete, ETA 00:08:23
# Fork: 1 of 5
# Warmup Iteration   1: 12.961 ns/op
# Warmup Iteration   2: 12.618 ns/op
# Warmup Iteration   3: 10.912 ns/op
# Warmup Iteration   4: 10.865 ns/op
# Warmup Iteration   5: 10.823 ns/op
Iteration   1: 10.940 ns/op
Iteration   2: 10.940 ns/op
Iteration   3: 11.009 ns/op
Iteration   4: 10.838 ns/op
Iteration   5: 10.849 ns/op

# Run progress: 60.00% complete, ETA 00:06:42
# Fork: 2 of 5
# Warmup Iteration   1: 13.095 ns/op
# Warmup Iteration   2: 12.814 ns/op
# Warmup Iteration   3: 10.921 ns/op
# Warmup Iteration   4: 11.232 ns/op
# Warmup Iteration   5: 10.919 ns/op
Iteration   1: 10.919 ns/op
Iteration   2: 10.968 ns/op
Iteration   3: 11.089 ns/op
Iteration   4: 10.954 ns/op
Iteration   5: 10.875 ns/op

# Run progress: 70.00% complete, ETA 00:05:01
# Fork: 3 of 5
# Warmup Iteration   1: 12.988 ns/op
# Warmup Iteration   2: 12.836 ns/op
# Warmup Iteration   3: 11.048 ns/op
# Warmup Iteration   4: 10.998 ns/op
# Warmup Iteration   5: 10.901 ns/op
Iteration   1: 10.857 ns/op
Iteration   2: 10.888 ns/op
Iteration   3: 10.875 ns/op
Iteration   4: 11.403 ns/op
Iteration   5: 12.337 ns/op

# Run progress: 80.00% complete, ETA 00:03:21
# Fork: 4 of 5
# Warmup Iteration   1: 13.453 ns/op
# Warmup Iteration   2: 12.464 ns/op
# Warmup Iteration   3: 10.855 ns/op
# Warmup Iteration   4: 10.863 ns/op
# Warmup Iteration   5: 10.836 ns/op
Iteration   1: 10.944 ns/op
Iteration   2: 10.855 ns/op
Iteration   3: 10.837 ns/op
Iteration   4: 10.842 ns/op
Iteration   5: 10.814 ns/op

# Run progress: 90.00% complete, ETA 00:01:40
# Fork: 5 of 5
# Warmup Iteration   1: 12.985 ns/op
# Warmup Iteration   2: 12.631 ns/op
# Warmup Iteration   3: 10.917 ns/op
# Warmup Iteration   4: 10.848 ns/op
# Warmup Iteration   5: 11.080 ns/op
Iteration   1: 10.814 ns/op
Iteration   2: 10.835 ns/op
Iteration   3: 10.853 ns/op
Iteration   4: 10.905 ns/op
Iteration   5: 10.819 ns/op


Result "com.dd.MyBenchmark.userWithNonFinalVariables":
  10.970 ±(99.9%) 0.232 ns/op [Average]
  (min, avg, max) = (10.814, 10.970, 12.337), stdev = 0.310
  CI (99.9%): [10.739, 11.202] (assumes normal distribution)


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

Benchmark                              Mode  Cnt   Score   Error  Units
MyBenchmark.userWithFinalVariables     avgt   25  11.065 ± 0.200  ns/op
MyBenchmark.userWithNonFinalVariables  avgt   25  10.970 ± 0.232  ns/op
```