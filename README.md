# File Statistics Scanner

[Click to watch Demo: ![Demo](https://img.youtube.com/vi/I9h9QZ44rgo/hqdefault.jpg)](https://www.youtube.com/watch?v=I9h9QZ44rgo)
<!-- <video src="demo.mp4" controls autoplay loop muted width="100%"></video> -->

A Python script to scan a directory for files with specified extensions, ignoring selected folders, and count:
-	Number of matching files
-	Total lines across all matching files
-	Total characters across all matching files

## How It Works
1. Prompts the user to enter file extensions (e.g., py, js, txt).
2. Prompts for directory names to ignore (e.g., node_modules, venv).
3. Recursively scans the current working directory using simple BFS traversal.
4. Displays statistics for each extension provided.

## Installation

### Using pipx
```sh
pipx install adityas-fsscan
```

## Example Run

```bash
$ fsscan
Current working directory: /Users/attaditya/projects/code-analyzer
Enter file extensions to scan: 
Please avoid leading dots (e.g., write 'py' instead of '.py').
> py
> js
> 

Enter directories to ignore (optional): 
Please avoid leading slashes (e.g., write 'node_modules' instead of '/node_modules').
> node_modules
> 

Data for py:
  Files: 12
  Lines: 1893
  Chars: 55120
Data for js:
  Files: 8
  Lines: 1104
  Chars: 30792
```

## Project Structure

```
.
├── main.py                # Entry point
├── count_data.py          # Contains CountData dataclass
├── file_scanner.py        # scan_files() implementation
```

## Requirements
- `Python 3.8+`

(No external dependencies required)

