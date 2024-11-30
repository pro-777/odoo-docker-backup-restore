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

يوفر هذا الملف README نظرة عامة واضحة على الأداة، وتثبيتها، واستخدامها، وتكوينها، مما يجعل من السهل على المستخدمين فهم واستخدام نصوص النسخ الاحتياطي والاستعادة.


### خطوات تحميل الملف إلى GitHub

1. **إنشاء مستودع جديد على GitHub**

   - انتقل إلى [GitHub](https://github.com) وقم بتسجيل الدخول.
   - انقر على الرمز "+" في الزاوية اليمنى العليا وحدد "New repository".
   - املأ اسم المستودع (مثل `odoo-docker-backup-restore`)، والوصف، والتفاصيل الأخرى.
   - انقر فوق "Create repository".

2. **استنساخ المستودع إلى جهازك المحلي**

   ```bash
   git clone https://github.com/pro-777/odoo-docker-backup-restore.git
   cd odoo-docker-backup-restore
إضافة ملف README

قم بإنشاء ملف README.md في دليل المستودع والصق المحتوى أعلاه فيه.


echo "# أداة نسخ احتياطي واستعادة قاعدة بيانات Odoo Docker
توفر هذه الأداة نصوصًا لنسخ قاعدة بيانات Odoo الاحتياطي واستعادتها التي تعمل في حاويات Docker. كما تنشئ مجلدًا داخل /opt/ يُسمى odoo-backups لتخزين ملفات النسخ الاحتياطي. بالإضافة إلى ذلك، تضيف الأداة وتحدد مستودع الملفات من حاوية Odoo Docker تلقائيًا.

المتطلبات الأساسية
Docker مثبت ويعمل.
حاوية Odoo Docker معدة وتعمل.
التثبيت
استنساخ المستودع


git clone https://github.com/pro-777/odoo-docker-backup-restore.git
cd odoo-docker-backup-restore
التحقق من الثنائيات

تأكد من أن الثنائيات تعمل بشكل صحيح:


./odoo_backup.sh.x
./odoo_restore.sh.x
يجب أن ترى المخرجات:


هذا هو نص النسخ الاحتياطي لـ Odoo.
هذا هو نص استعادة Odoo.
الاستخدام
نسخ قاعدة بيانات Odoo احتياطيًا
لنسخ قاعدة بيانات Odoo احتياطيًا، قم بتشغيل نص النسخ الاحتياطي:


./odoo_backup.sh.x
سيقوم هذا النص بـ:

الاتصال بحاوية Odoo Docker.
إجراء نسخ احتياطي لقاعدة البيانات.
إضافة وتحديد مستودع الملفات من حاوية Odoo Docker تلقائيًا.
حفظ ملف النسخ الاحتياطي ومستودع الملفات في مجلد /opt/odoo-backups.
استعادة قاعدة بيانات Odoo
لاستعادة قاعدة بيانات Odoo، قم بتشغيل نص الاستعادة:


./odoo_restore.sh.x
سيقوم هذا النص بـ:

الاتصال بحاوية Odoo Docker.
استعادة قاعدة البيانات من ملف النسخ الاحتياطي المحدد الموجود في مجلد /opt/odoo-backups.
استعادة مستودع الملفات من النسخ الاحتياطي.
التحقق من عملية الاستعادة.
التكوين
يمكنك تخصيص عمليات النسخ الاحتياطي والاستعادة عن طريق تعديل النصوص. على سبيل المثال، يمكنك تحديد موقع النسخ الاحتياطي، وبيانات اعتماد قاعدة البيانات، ومعلمات أخرى.

المساهمة
المساهمات مرحب بها! يرجى فتح مشكلة أو إرسال طلب سحب.

الترخيص
هذا المشروع مرخص بموجب ترخيص MIT. انظر الملف LICENSE للتفاصيل.

الاتصال
لأي أسئلة أو دعم، يرجى الاتصال بـ m@havari.me.


