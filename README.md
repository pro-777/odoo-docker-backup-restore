# Odoo Docker Database Backup and Restore Tool

## Overview
The Odoo Docker Database Restore Tool is a Python script designed to automate the process of restoring Odoo databases from backup files. This tool is particularly useful for system administrators and developers who need to manage Odoo instances running in Docker containers. The script handles the entire restore process, including verifying backup integrity, stopping and starting containers, and restoring both the database and filestore.

## Features
- **Backup Verification**: Ensures the backup file is intact and contains the necessary database dump.
- **Container Management**: Automatically stops and starts Odoo and PostgreSQL containers as needed.
- **Database Restoration**: Drops the existing database (if it exists) and restores it from the backup.
- **Filestore Restoration**: Restores the filestore directory if it is present in the backup.
- **User Interaction**: Prompts the user for necessary inputs and confirms actions before proceeding.
- **Error Handling**: Provides clear error messages and handles common issues gracefully.

## Prerequisites
- Python 3.x
- Docker
- Odoo and PostgreSQL containers
- Backup files in `.tar.gz` format containing `database.sql` and optionally a `filestore` directory.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/pro-777/odoo-docker-backup-restore.git
   cd odoo-docker-backup-restore
   Ensure you have the necessary permissions to run Docker commands and access the backup directory.

## Usage

Place your backup files in the specified backup directory (default: /opt/odoo-backups).


## Run the script:
./odoo_backup
./odoo_restore

## Script Workflow
Print Banner: Displays system information and a welcome banner.
List Backups: Lists available backup files in the specified directory.
Select Backup: Prompts the user to select a backup file.
Verify Backup: Verifies the integrity of the selected backup file.
List Containers: Lists available PostgreSQL and Odoo containers.
Select Containers: Prompts the user to select the PostgreSQL and Odoo containers.
Database Credentials: Prompts the user to enter the database user and target database name.
Confirm Restore: Displays a summary of the restore process and prompts the user for confirmation.
Stop Odoo Container: Stops the Odoo container to prepare for the restore.
Restore Database: Drops the existing database (if it exists) and restores it from the backup.
Restore Filestore: Restores the filestore directory if it is present in the backup.
Start Odoo Container: Starts the Odoo container after the restore is complete.
Cleanup: Cleans up temporary files used during the restore process.
Display Logs: Displays recent Odoo logs to confirm the restore process.
Error Handling
Backup File Not Found: The script checks if the backup file exists and is readable.
Container Not Found: The script verifies that the specified containers are running.
Database.sql Not Found: The script searches recursively for the database.sql file within the backup.
Filestore Not Found: The script checks for the presence of the filestore directory in the backup.
Container Management: The script handles starting and stopping containers with multiple attempts.
Contributing
Contributions are welcome! Please open an issue or submit a pull request if you have any suggestions or improvements.

L## icense
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any questions or support, please contact Mostafa Elhavari.



