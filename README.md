# Odoo Docker Database Backup and Restore Tool

## Overview

The Odoo Docker Database Backup and Restore Tool is a Python script designed to simplify the process of backing up and restoring Odoo databases running in Docker containers. This tool ensures that your Odoo database and filestore are safely backed up and can be restored efficiently.

## Features

- **Backup Integrity Verification**: Ensures that the backup file is valid and contains the necessary database dump.
- **Container Management**: Automatically detects and manages PostgreSQL and Odoo containers.
- **Database Restoration**: Handles the restoration of the database and filestore, including dropping and recreating the database if necessary.
- **User Interaction**: Provides a user-friendly interface for selecting backups and confirming actions.
- **Error Handling**: Includes robust error handling to manage common issues during the backup and restore process.

## Prerequisites

- Python 3.x
- Docker
- PostgreSQL
- Odoo

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/odoo-backup-restore.git
    cd odoo-backup-backup-restore
 


## Usage

1. **Backup**:
    - Ensure that your Odoo and PostgreSQL containers are running.
    - Place the backup script in a directory of your choice.
    - Run the backup script:
        
        ./odoo_backup
      
    - Follow the on-screen instructions to create a backup of your Odoo database and filestore.

2. **Restore**:
    - Ensure that your Odoo and PostgreSQL containers are running.
    - Place the restore script in a directory of your choice.
    - Run the restore script:
       
        ./odoo_restore
    
    - Follow the on-screen instructions to select a backup and restore your Odoo database and filestore.

## Script Details

### Backup Script (`odoo_backup`)

The backup script performs the following steps:
1. **Detect Containers**: Identifies the running PostgreSQL and Odoo containers.
2. **Create Backup**: Creates a backup of the Odoo database and filestore.
3. **Save Backup**: Saves the backup file to a specified directory.

### Restore Script (`odoo_restore`)

The restore script performs the following steps:
1. **Detect Containers**: Identifies the running PostgreSQL and Odoo containers.
2. **Select Backup**: Lists available backups and allows the user to select one for restoration.
3. **Verify Backup**: Verifies the integrity of the selected backup file.
4. **Stop Odoo Container**: Stops the Odoo container to ensure a safe restoration process.
5. **Restore Database**: Drops the existing database (if it exists) and restores the database from the backup.
6. **Restore Filestore**: Restores the filestore from the backup.
7. **Start Odoo Container**: Starts the Odoo container after the restoration is complete.
8. **Cleanup**: Cleans up temporary files used during the restoration process.

## Example
================================
SYSTEM INFORMATION
================================
Time: 2024-11-30 14:59:38
IP Address: 192.168.1.100
OS: Ubuntu 20.04.1 LTS
================================

System Information:
• Hostname: your-hostname
• Date: 2024-11-30 14:59:38
• User: your-username

Available backups:
==================
1. odoo_full_backup_ok_20241130_145935.tar.gz (2.0M) - 2024-11-30 14:59:38
2. odoo_full_backup_ok_20241130_110320.tar.gz (1.2M) - 2024-11-30 11:03:27
3. odoo_full_backup_ok_20241130_152047.tar.gz (2.0M) - 2024-11-30 15:20:50

Select backup number [1-3]: 3
Verifying backup integrity...

Detecting Docker containers...

Available PostgreSQL containers:
================================
ID: 5d6aa362afce | Name: odoo-one-db-1

Enter PostgreSQL container ID or name: 5d6aa362afce

Available Odoo containers:
================================
ID: 7e2b4c8a1b3f | Name: odoo-one-web-1

Enter Odoo container ID or name: 7e2b4c8a1b3f
Enter database user [default: odoo]:
Extracted database name: ok
Enter target database name [default: ok]:
Warning: Database 'ok' already exists
Do you want to drop and recreate it? [y/n]: y

=== Restore Summary ===
Selected Backup: odoo_full_backup_ok_20241130_152047.tar.gz
Database Container: 5d6aa362afce
Odoo Container: 7e2b4c8a1b3f
Target Database: ok
Temporary Directory: /tmp/tmpabc123

WARNING: This will overwrite the database and filestore if they exist!
Do you want to proceed with the restore? [y/n]: y

Preparing for restore...
Stopping Odoo service...
Restoring database...
Dropping existing database if exists...
Creating new database...
Restoring database content...
Restoring filestore...
Creating filestore directory...
Copying filestore data...
Filestore restored successfully
Starting Odoo service...
Cleaning up temporary files...

=== Restore Completed Successfully ===
Timestamp: 2024-11-30 15:30:00
Restored From: odoo_full_backup_ok_20241130_152047.tar.gz
Target Database: ok

Waiting for Odoo to start...
Recent Odoo logs:
2024-11-30 15:30:00 INFO: Odoo server is starting...
...

Restore process completed!

### Backup


./odoo_backup
Follow the on-screen instructions to create a backup of your Odoo database and filestore.



