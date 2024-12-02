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

### Backup


./odoo_backup
Follow the on-screen instructions to create a backup of your Odoo database and filestore.



