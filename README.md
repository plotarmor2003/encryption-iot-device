# Lightweight Encryption for IoT Devices

This project implements a lightweight encryption algorithm designed for IoT devices. The encryption is based on a simplified version of the Advanced Encryption Standard (AES), optimized for resource-constrained environments typical of IoT devices.

## Features

- **S-Box Implementation:** Utilizes a substitution box (S-Box) for byte substitution, a key component in encryption algorithms like AES.
- **Field Multiplication:** Performs finite field multiplication essential for the MixColumns transformation in AES.
- **AddRoundKey Function:** XORs the state with a portion of the round key, another core function in AES encryption.
- **SubCell and ShiftRow Operations:** Implements byte substitution and row shifting, contributing to the diffusion properties of the cipher.
- **MixColumn Transformation:** Applies the MixColumns transformation to the state matrix, ensuring diffusion across the block.

## Project Structure

- **light_weight.py:** The main implementation file containing all encryption-related functions.
- **README.md:** This file provides an overview of the project and instructions for use.

## How It Works

1. **SubBytes (SubCell):** Each byte of the state is replaced with its corresponding value from the S-Box.
2. **ShiftRows:** Each row of the state is cyclically shifted by a certain number of bytes.
3. **MixColumns:** Each column of the state is mixed by multiplying it with a constant matrix in the finite field.
4. **AddRoundKey:** The state is XORed with the round key derived from the original encryption key.

## Requirements

- Python 3.x

## Usage

To use the encryption algorithm, simply include the `light_weight.py` file in your project and call the provided functions with your input data.

```python

