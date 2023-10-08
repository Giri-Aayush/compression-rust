# Simple Rust File Compression Utility using flate2

## Overview
This Rust project is a straightforward utility for compressing files using the Gzip compression algorithm. It leverages the `flate2` library to perform the compression. The utility is designed to be used from the command line, and it measures the time taken to complete the compression process, providing a simple performance metric.

## Dependencies
- Rust Programming Language (latest stable version recommended)
- `flate2` crate

## Usage
1. Ensure you have the latest stable version of Rust installed on your machine. You can download it from the [official website](https://www.rust-lang.org/).
2. Clone or download this repository to your local machine.
3. Navigate to the project directory in your terminal.
4. Run the program with the following command, replacing `source` and `target` with the path to the source file you want to compress and the path where you want to save the compressed file, respectively:
```bash
cargo run --release source target
```
## How It Works
1. The program starts by checking the number of arguments provided in the command line to ensure the source and target file paths are specified.
2. It then opens the source file and prepares a target file for writing.
3. A Gzip encoder is created using the GzEncoder struct from the flate2 crate, with the default compression level.
4. The std::io::copy function is used to read from the source file and write to the Gzip encoder, which in turn writes the compressed data to the target file.
5. Once the compression is complete, the program prints out the size of the source file, the size of the compressed file, and the time taken to complete the compression.

## Performance Metrics
After the compression process, the program outputs three pieces of information:

- The size of the source file in bytes.
- The size of the compressed file in bytes.
- The time taken to complete the compression

## Error Handling
Basic error handling is implemented to manage potential issues that might arise during file operations, such as file not found or permission denied errors. For instance, if the program encounters an error while opening the source file or creating the target file, it will terminate and output an error message.

## Future Improvements
- Better error handling and user feedback.
- Adding support for different compression algorithms.
- Adding options for specifying compression level.
- Adding decompression functionality.
$Error Handling
Basic error handling is implemented to manage potential issues that might arise during file operations, such as file not found or permission denied errors. For instance, if the program encounters an error while opening the source file or creating the target file, it will terminate and output an error message.

## Future Improvements
- Better error handling and user feedback.
- Adding support for different compression algorithms.
- Adding options for specifying compression level.
- Adding decompression functionality.

## License
This project is open-source and available under the MIT License. See the LICENSE file for more details.
