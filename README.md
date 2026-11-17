# dupe-finder

`dupe-finder` reports duplicate files with matching SHA-256 content hashes.
It compares files within each directory that has no subdirectories.
It does not compare files across different directories.

## Current status

This prototype has a scan path set directly in `src/main.rs`.
It does not accept command-line arguments.
The Cargo package and executable are named `sample_organizer`.

## Use

1. Install Rust and Cargo.
2. Set `root_directory` in [src/main.rs](src/main.rs) to the directory you want to scan.
3. Run this command from the repository root:

   ```bash
   cargo run --locked --release
   ```

The tool prints duplicate groups and writes `scan_log.txt` in the current directory.
Each run replaces that log file.
The tool does not delete or move the scanned files.
