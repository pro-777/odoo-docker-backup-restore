# Odoo Docker Database Backup and Restore Tool


This tool provides scripts to backup and restore Odoo databases running in Docker containers. It also creates a folder inside Host `/opt/` called `odoo-backups` to store the backup files. Additionally, the tool automatically adds and locates the Odoo filestore from the Odoo Docker container.


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



==================================================
أداة النسخ الاحتياطي والاستعادة لقاعدة بيانات # Odoo Docker Docker


توفر هذه الأداة برامج نصية للنسخ الاحتياطي واستعادة قواعد بيانات Odoo التي تعمل في حاويات Docker. كما أنها تنشئ مجلدًا داخل المضيف '/opt/' يسمى 'odoo-backups' لتخزين ملفات النسخ الاحتياطي. بالإضافة إلى ذلك، تضيف الأداة تلقائيًا وتحدد موقع مخزن ملفات أودو من حاوية أودو دوكر.


## المتطلبات الأساسية


- تثبيت Docker وتشغيله.
- إعداد حاوية أودو دوكر Docker وتشغيلها.


## التثبيت


1. ** استنساخ المستودع**


'''باش
git clone https://github.com/pro-777/odoo-docker-backup-restore.git
cd odoo-docker-backup-backup-الاستعادة
التحقق من الثنائيات


تأكد من تنفيذ الثنائيات بشكل صحيح:




./odoo_backup.sh.x
./odoo_restore.sh.x
يجب أن ترى المخرجات:




هذا هو البرنامج النصي للنسخ الاحتياطي لأودو.
هذا هو البرنامج النصي لاستعادة أودو.
الاستخدام
النسخ الاحتياطي لقاعدة بيانات أودو
للنسخ الاحتياطي لقاعدة بيانات أودو، قم بتشغيل البرنامج النصي للنسخ الاحتياطي:




./odoo_backup.sh.x
سيقوم هذا النص البرمجي بـ


الاتصال بحاوية Odoo Docker Docker.
إجراء نسخة احتياطية لقاعدة البيانات.
إضافة وتحديد موقع مخزن ملفات Odoo تلقائيًا من حاوية Odoo Docker.
احفظ ملف النسخ الاحتياطي ومخزن الملفات في دليل /opt/odoo-backups.
استعادة قاعدة بيانات أودو
لاستعادة قاعدة بيانات أودو، قم بتشغيل البرنامج النصي للاستعادة:




./odoo_restore.sh.x
سيقوم هذا البرنامج النصي بـ


الاتصال بحاوية Odoo Docker Docker.
استعادة قاعدة البيانات من ملف النسخ الاحتياطي المحدد الموجود في دليل /opt/odoo-backups.
استعادة مخزن الملفات من النسخة الاحتياطية.
التحقق من عملية الاستعادة.
التكوين
يمكنك تخصيص عمليات النسخ الاحتياطي والاستعادة عن طريق تعديل البرامج النصية. على سبيل المثال، يمكنك تحديد موقع النسخ الاحتياطي وبيانات اعتماد قاعدة البيانات ومعلمات أخرى.


المساهمة
المساهمات مرحب بها! يرجى فتح مشكلة أو إرسال طلب سحب.


الترخيص
هذا المشروع مرخص بموجب رخصة MIT. راجع ملف LICENSE للحصول على التفاصيل.
