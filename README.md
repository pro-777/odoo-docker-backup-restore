# Odoo Docker Database Backup and Restore Tool

This tool provides scripts to backup and restore Odoo databases running in Docker containers. It also creates a folder inside  Host `/opt/` called `odoo-backups` to store the backup files. Additionally, the tool automatically adds and locates the Odoo filestore from the Odoo Docker container.

## Prerequisites

- Docker installed and running.
- Odoo Docker container set up and running.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/pro-777/odoo-docker-backup-restore.git
   cd odoo-docker-backup-restore
Verify the Binaries

Make sure the binaries execute correctly:


./odoo_backup.sh.x
./odoo_restore.sh.x
You should see the outputs:


This is the Odoo backup script.
This is the Odoo restore script.
Usage
Backup Odoo Database
To backup the Odoo database, run the backup script:


./odoo_backup.sh.x
This script will:

Connect to the Odoo Docker container.
Perform a database backup.
Automatically add and locate the Odoo filestore from the Odoo Docker container.
Save the backup file and filestore to the /opt/odoo-backups directory.
Restore Odoo Database
To restore the Odoo database, run the restore script:


./odoo_restore.sh.x
This script will:

Connect to the Odoo Docker container.
Restore the database from a specified backup file located in the /opt/odoo-backups directory.
Restore the filestore from the backup.
Verify the restoration process.
Configuration
You can customize the backup and restore processes by modifying the scripts. For example, you can specify the backup location, database credentials, and other parameters.

Contributing
Contributions are welcome! Please open an issue or submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any questions or support, please contact m@havari.me.

========================================

echo "# أداة نسخ احتياطي واستعادة قاعدة بيانات Odoo Docker
المتطلبات الأساسية

