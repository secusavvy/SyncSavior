# SyncSavior

SyncSavior is a bash script designed to streamline the process of creating incremental backups using `rsync`. It efficiently manages backup directories, incorporates timestamping, and logs operations to ensure your data is always synchronized and secure.

### Features
- **Incremental Backups:** Uses `rsync` to perform efficient and incremental backups, reducing the need for redundant data transfers.
- **Timestamped Directories:** Automatically organizes backups with date-stamped directories for easy tracking and management.
- **Comprehensive Logging:** Captures detailed logs of the backup process, aiding in troubleshooting and verification.
- **Simple Operation:** Easily run the script with minimal parameters to handle your backup needs.

### Technologies Used
- Bash scripting
- `rsync` for file synchronization and backup
- `date` command for generating timestamps

### Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/secusavvy/SyncSavior.git
   cd SyncSavior
   ```

2. Make the script executable:
   ```bash
   chmod +x backup.sh
   ```

3. Run the script:
   ```bash
   ./backup.sh <source_directory> <target_directory>
   ```

   Replace `<source_directory>` with the path of the directory you want to back up and `<target_directory>` with the path where the backup should be stored.

### How It Works
- The script begins by validating the input arguments to ensure that both source and target directories are provided.
- It checks for the presence of `rsync` to ensure that the backup process can proceed.
- It creates a timestamped backup directory within the target location and performs the backup operation.
- All actions, including errors and progress, are logged to a file named `backup_<current_date>.log`.
