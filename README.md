# Distributed Blockchain Network and Miner

## Overview

This project is a distributed blockchain network and mining system comprising a Python-based blockchain peer and two distinct mining clients: a Rust-based CPU miner and a CUDA-based GPU miner. The system is designed to simulate a simplified blockchain environment with capabilities such as synchronization, consensus, and state management, while exploring performance optimizations through multithreading and GPU acceleration.

**Code available upon request. [Contact Information](#contact-information)**

## Features

- **Blockchain Peer (Python):**
  - Event-driven, object-oriented architecture for efficient network communication and protocol handling.
  - Implements synchronization and consensus mechanisms to maintain blockchain integrity across the network.
  - Manages state and handles incoming and outgoing messages with other peers and miners.

- **Mining Clients:**
  - **Rust-based CPU Miner:**
    - Utilizes multithreading to optimize CPU usage for mining operations.
    - Communicates with the blockchain peer via custom TCP/IP protocols.
  - **CUDA-based GPU Miner:**
    - Leverages GPU acceleration to enhance hashing performance.
    - Implements parallel processing using CUDA for efficient mining.
    - Interacts with the blockchain peer using the same custom protocols.

## Architecture

### Components

1. **Blockchain Peer:**
   - Written in Python, it acts as a node in the blockchain network.
   - Listens for connections from mining clients and other network peers.
   - Manages the blockchain state, including adding new blocks and handling consensus.
   - Utilizes event-driven programming to handle asynchronous network events efficiently.

2. **Mining Clients:**
   - **CPU Miner (Rust):**
     - Exploits Rust's performance and safety features.
     - Uses multithreading to maximize CPU resource utilization.
   - **GPU Miner (CUDA with C++):**
     - Harnesses the power of NVIDIA GPUs for parallel computation.
     - Implements hashing algorithms optimized for GPU architecture.

### Communication Flow

1. **Initialization:**
   - Mining clients establish a connection with the blockchain peer.
   - The blockchain peer provides the latest block information and any pending transactions or messages.

2. **Mining Process:**
   - Mining clients perform hashing computations to find a valid nonce that satisfies the difficulty criteria.
   - The CPU miner distributes work across multiple threads.
   - The GPU miner dispatches work to the GPU cores using CUDA.

3. **Block Submission:**
   - Upon finding a valid block, miners submit it to the blockchain peer over the established TCP/IP connection.
   - The blockchain peer validates the block and, if valid, adds it to the blockchain.

4. **Network Update:**
   - The blockchain peer broadcasts the new block to other peers in the network.
   - Mining clients receive updates about new blocks and adjust their mining activities accordingly.

## Technologies Used

- **Python:**
  - Used for the blockchain peer implementation.
  - Employs event-driven programming and object-oriented principles.
  - Manages network communication using sockets and handles multiple connections concurrently.

- **Rust:**
  - Used for the CPU mining client.
  - Leverages Rust's performance, memory safety, and concurrency features.
  - Implements efficient multithreading for mining computations.

- **CUDA (Compute Unified Device Architecture):**
  - Used for the GPU mining client.
  - Enables parallel computation on NVIDIA GPUs.
  - Provides significant performance improvements for hashing operations.

- **Networking:**
  - Custom TCP/IP protocols facilitate communication between the blockchain peer and mining clients.
  - Ensures efficient data exchange and synchronization across the distributed system.

## Getting Started

### Prerequisites

- **Blockchain Peer:**
  - Python 3.x installed.
  - Required Python libraries (e.g., `socket`, `select`, etc.).

- **Rust CPU Miner:**
  - Rust toolchain installed (`rustc`, `cargo`).

- **CUDA GPU Miner:**
  - NVIDIA GPU with CUDA support.
  - CUDA Toolkit installed.
  - NVCC

### Installation

**Note:** Detailed installation instructions and code are available upon request.

1. **Blockchain Peer:**
   - Clone the repository.
   - Install any required Python dependencies.
   - Configure network settings as needed.

2. **Rust CPU Miner:**
   - Clone the repository.
   - Build the project using `cargo build`.

3. **CUDA GPU Miner:**
   - Clone the repository.
   - Ensure the CUDA environment is properly set up.
   - Build the project using `cargo build`.

### Running the System

1. **Start the Blockchain Peer:**
   - Run the Python script to start the blockchain peer.
   - It will begin listening for connections from mining clients and network peers.

2. **Start the Mining Clients:**
   - Run the Rust CPU miner and/or the CUDA GPU miner.
   - They will connect to the blockchain peer and commence mining operations.

3. **Monitoring:**
   - Logs and console outputs provide information about mining progress, block submissions, and network updates.

## Project Structure

- `blockchain_peer/`:
  - Contains the Python code for the blockchain peer.
  - Modules for network handling, event management, blockchain logic, and peer management.

- `cpu_miner/`:
  - Contains the Rust code for the CPU mining client.
  - Includes mining algorithms, network communication, and threading logic.

- `gpu_miner/`:
  - Contains the Rust code for the GPU mining client with CUDA support.
  - Includes CUDA kernels, mining algorithms, and networking components.

## Challenges and Learnings

- **Synchronization and Consensus:**
  - Implementing consensus algorithms to ensure blockchain integrity across a distributed network.
  - Handling scenarios where multiple miners submit valid blocks simultaneously.

- **Performance Optimization:**
  - Utilizing multithreading in Rust to maximize CPU efficiency.
  - Leveraging GPU acceleration with CUDA for substantial performance gains in mining.

- **Network Communication:**
  - Designing custom TCP/IP protocols for reliable and efficient data exchange between Peer and Miner clients.
  - Managing multiple concurrent connections and ensuring thread safety.

- **Event-Driven Architecture:**
  - Applying event-driven programming in Python to handle asynchronous events and improve responsiveness.
  - Structuring the system to scale effectively with increased network activity.


## Contact Information

For more information or to request access to the code, please contact:

- **Name:** Raman Bhandari
- **Email:** bhandar1@myumanitoba.ca or bhandari.raman14@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/raman-bhandari/
