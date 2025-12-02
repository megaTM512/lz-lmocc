# LZ-LMOCC

LZ-MAXOCC takes a lempel-ziv compressed file as input and changes the referenced position for each phrase to the substring with the minimal average reference height.

## Usage

```bash
make
./lz-lmocc -i <input_file> -o <output_file> # Output file without file extension
```

## Output

The output file will contain the modified LZ77 compressed data. Additionally, a CSV file named `lz-lmocc_results.csv` will be created (or appended to) in the current directory, containing performance metrics for each run.

The CSV file will have the following columns:

- Timestamp
- Algorithm used (LZ-MAXOCC)
- Input File
- Number of Phrases
- Average Height Before
- Max Height Before
- Variance Height Before
- Average Height After
- Max Height After
- Variance Height After
- Time Taken (seconds)
