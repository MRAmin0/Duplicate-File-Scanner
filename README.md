# Duplicate File Finder

This project helps users find duplicate files in a specified directory and its subdirectories. It scans files based on their SHA-256 hash and provides a detailed report of duplicate files. The tool also allows users to ignore specific directories from the scan process.

## Features

- Search for duplicate files by hashing the content of the files.
- Option to ignore specific directories during the scan.
- Save the results of the scan in a JSON file.
- Display duplicate file paths in the console.

## Requirements

- Python 3.x
- `tqdm` library for progress bar (can be installed via `pip`)

## Installation

### Clone the repository

```bash
git clone https://github.com/MRAmin0/Duplicate-File-Scanner.git
cd Duplicate-File-Scanner
```

Install dependencies
This project requires the tqdm package for showing a progress bar during the scan. Install the required dependencies using pip:

```python
pip install -r requirements.txt
```


Or you can simply install tqdm manually:

```python
pip install tqdm
```

## Usage
1. Run the script by executing the following command:

```python
python duplicate_finder.py
```

2. Enter the target directory you want to scan when prompted.

3. Choose whether to ignore specific directories:

- If you don't want to scan certain directories, enter their paths when prompted (one per line). Type done when you're finished entering directories to ignore.

- If you don't need to ignore any directories, simply respond with no.

4. Wait for the scan to finish. The script will calculate the hash of each file and check for duplicates.

5. View the results:

- The results will be displayed in the console.

- A JSON file (duplicates.json) will be created, containing the list of duplicate files.

## Output

- Console Output: Duplicate files are listed in the console along with a separator line for each hash group.

- JSON Output: A file named duplicates.json will be generated, containing a JSON object where each key is a file hash and each value is a list of file paths that share that hash.

- Example of duplicates.json:
```json
{
    "e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855": [
        "/path/to/duplicate/file1.txt",
        "/path/to/duplicate/file2.txt"
    ],
    "7a5a28c3798ed929fd9cc9adcf517771bcf26a4014899e6b8a5777f70bc1cc71": [
        "/path/to/duplicate/file3.jpg"
    ]
}
```

## License

This project is licensed under the MIT License - see the [MIT License](https://opensource.org/licenses/MIT) for details.
