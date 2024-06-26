# The Blip

## Overview
Thanos is a Python script designed to terminate approximately half of the currently active processes on a system. It randomly selects processes to shut down and poofs them from existence!

## Warning
**Use with Caution:** This script can significantly affect system stability and should be used in a controlled environment. Running Thanos on a system is not recommended unless for testing or chaotic purposes. :)

## Requirements
- Python 3.x
- A custom `process` module capable of listing and killing processes. Ensure this module is securely implemented.

## Operation
Thanos operates by shuffling the list of active process IDs and then terminating a proportion of them. It achieves this through the following steps:
1. **Initialization**: It gathers all process IDs, ensuring no critical system processes are included.
2. **Random Selection**: The script randomly shuffles the list of process IDs to neutralize any bias in selection.
3. **Process Termination**: Thanos systematically terminates each selected process until half of the original list has been processed.

## Usage
To run Thanos, execute the following command in your terminal:
```bash

python thanos.py
