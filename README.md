# Estimation
This project is for the cardinality estimation pruning for top-down logic rule mining.

## 1. Compilation

There are two versions of implementation:
- `src.7z` contains Java impelementation. Maven build files are included.
- `c++.7z` contains C++ implementation. CMake configuration files are included.
The runtime options for the executables are slightly different due to the dependend libraries and can be viewed with the option `-help` or `--help`.
The system *Est* is to run with the observation ratio option and set an observation ratio no less than 1.0.

E.g. (suppose `est.jar` is the JAR package compiled from the Java source code) 
```sh
$ java -jar est.jar -I dataset Fm -o 2.5
```
The original version of *SInC* is to run without the estimation option.

E.g.
```sh
$ java -jar est.jar -I dataset Fm
```

## 2. Dataset

All datasets used in this project is included in `dataset.7z`.
The specificaitons of the binary KB format is included in the `src/main/java/sinc2/util/kb/NumeratedKb.java` file (Java source) and the `src/kb/SimpleKb.h` file (C++ source).
