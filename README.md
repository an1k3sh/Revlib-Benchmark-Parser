# Revlib-Benchmark-Parser

This reporsitory contains two Python scripts, which convert Revlib Benchmarks in the `.real` format into Qiskit Qauntum Circuits and QASM (Quantum Assembly Language) code respectively.

## Requirements

The following dependencies are required to use these converters:
- Python 3.x
- Qiskit

## Files

The repository consists of the following files:

1. `revlibparser.py`: This file provides a parser for the .real benchmark format. It defines functions to read and parse the benchmark file, and convert it into a Qiskit `QuantumCircuit` object. The `read_circuit` function takes a file path as input and returns a `QuantumCircuit` representing the benchmark.
2. `QASM_converter.py`: This script utilizes the  `revlibparser.py` module to convert benchmarks in the `.real` format into QASM code. It locates the benchmark files in a directory named "reals" and generates corresponding QASM files in a directory named "qasm_files". The QASM files can be used with other tools or simulators that support the QASM format.

## Usage

1. Converting the benchmark files to Qiskit `QuantumCircuit` object:
   - Import the `revlibparser` module
     ``` python
     import revlibparser
     ```
   - Call the `read_circuit` function
     ``` python
     qc = revlibparser.read_circuit("./real/benchmark_name.real")
     ```
2. Converting the benchmark files to QASM files:
   - Place the benchmark files into a folder named real `real` in the same directory as `QASM_converter.py`
   - Execute the `QASM_converter.py` file
