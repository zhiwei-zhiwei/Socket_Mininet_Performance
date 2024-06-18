## Project: Iperfer - Network Bandwidth Measurement Tool

### Overview

This project is a part of Lab 1 for CS640 Fall 2022 at the University of Wisconsin - Madison. The objective of this lab is to understand network performance by implementing a custom version of Iperf called Iperfer using Java sockets. The project involves measuring network bandwidth in both wired and wireless environments, as well as within virtual networks created using Mininet.

### Team Members
- **Name 1**: [CS Username 1]
- **Name 2**: [CS Username 2] (if applicable)

### Learning Outcomes

- Write applications that use sockets to transmit and receive data across a network.
- Describe how latency and throughput can be measured.
- Explain how latency and throughput are impacted by link characteristics and multiplexing.

### Project Structure

- **iperfer/**: Contains all the Java source files for Iperfer.
- **measurement/**: Contains measurement results and answers to questions from Part 3 of the lab.
- **README**: This file.

### Iperfer Usage

#### Client Mode

To run Iperfer in client mode, use the following command:
```
java Iperfer -c -h <server hostname> -p <server port> -t <time>
```
- `-c`: Indicates client mode.
- `<server hostname>`: Hostname or IP address of the Iperfer server.
- `<server port>`: Port on which the server is listening (1024 ≤ port ≤ 65535).
- `<time>`: Duration in seconds for which data should be generated.

Example:
```
java Iperfer -c -h 192.168.1.1 -p 5001 -t 10
```

#### Server Mode

To run Iperfer in server mode, use the following command:
```
java Iperfer -s -p <listen port>
```
- `-s`: Indicates server mode.
- `<listen port>`: Port on which the server will listen (1024 ≤ port ≤ 65535).

Example:
```
java Iperfer -s -p 5001
```

### Part 1: Write Iperfer

- Implement Iperfer to send and receive TCP packets between a pair of hosts.
- In client mode, Iperfer sends data for a specified time and calculates the bandwidth.
- In server mode, Iperfer receives data and calculates the bandwidth.

### Part 2: Mininet Tutorial

- Follow the Mininet tutorial to create virtual networks and run experiments.
- Download and set up the Mininet VM.

### Part 3: Measurements in Mininet

- Measure the RTT and bandwidth of links between switches in Mininet.
- Measure the latency and throughput between specific hosts.
- Investigate the effects of multiplexing and latency.

### Submission Instructions

- **Source Code**: Place all Java source files for Iperfer in the `iperfer` folder.
- **Measurement Results**: Place all measurement results and answers in the `measurement` folder.
- **README**: Include this file.

To create the submission tar file, use the following command:
```
tar czvf username1_username2.tgz iperfer measurement README
```
or
```
tar czvf username1.tgz iperfer measurement README
```

Upload the tar file on the Lab1 tab on the course's Canvas page.

### References

- [Iperf](https://iperf.fr)
- [Java Sockets Tutorial](http://docs.oracle.com/javase/tutorial/networking/sockets/index.html)
- [Mininet](http://mininet.org)
- [Mininet Walkthrough](http://mininet.org/walkthrough/)

### Assumptions
- Input values are validated as specified.
- Network environments are correctly set up as per the instructions.
- Mininet VM is configured according to the provided guidelines.
