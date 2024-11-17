Huffman Coding Compression
Description

This project implements Huffman Coding, a lossless compression algorithm that can compress and decompress text files. The program supports two main functions:

Encode: Compresses an input text file.

Decode: Decompresses a Huffman-coded file back to its original form.

Key Components

struct Node: Represents a node in the Huffman Tree, storing character data, frequency, Huffman code, and pointers to left and right child nodes.

Huffman Class: Contains methods to compress and decompress files. Initialize with:

Huffman h(inputFileName, outputFileName);

Compression (compress())

createMinHeap(): Reads the input file, calculates character frequencies, and builds a Min Heap using a priority queue.

createTree(): Constructs the Huffman Tree by combining nodes with the lowest frequencies until only one node remains in the heap.

createCodes(): Assigns binary codes to each character by traversing the Huffman Tree.

saveEncodedFile(): Saves the encoded data to the output file. Encoded file format includes Huffman codes and metadata, with padding added if necessary.
Decompression (decompress())

getTree(): Reconstructs the Huffman Tree from the Min Heap stored at the beginning of the encoded file.
saveDecodedFile(): Converts the encoded binary data back into characters using the reconstructed Huffman Tree and writes the output to a file.
Usage
Compressing: Use the compress() method to convert a text file to a Huffman-encoded file (.huf).
Decompressing: Use the decompress() method to revert a Huffman-encoded file back to its original text format.
Results
Example: Compressing inputFile.txt (2.2 MB) results in compressedFile.huf (1.1 MB). Decompressing compressedFile.huf returns outputFile.txt (2.2 MB).
