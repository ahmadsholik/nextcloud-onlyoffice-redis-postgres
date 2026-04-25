# nextcloud-onlyoffice-redis-postgres
1. Persiapan Folder Jalankan perintah ini untuk menyiapkan lingkungan:  Bash mkdir nextcloud-production &amp;&amp; cd nextcloud-production
2. Buat file docker-compose.yml dan masukkan kode diatas
3. Langkah Instalasi & Integrasi
Jalankan Container:

Bash
docker-compose up -d
Akses Nextcloud:
Buka http://localhost:8080 (atau IP server Anda). Karena kita sudah memasukkan NEXTCLOUD_ADMIN_USER di config, Anda bisa langsung login.

Instal Aplikasi ONLYOFFICE di Nextcloud:

Klik profil (kanan atas) > + Apps.

Cari ONLYOFFICE, lalu klik Download and enable.

Konfigurasi Konektor ONLYOFFICE:

Buka Settings > Administration > ONLYOFFICE.

Document Editing Service address: http://<IP-SERVER-ANDA>:8081/

Secret key: RahasiaKunciInformatika123 (harus sama dengan JWT_SECRET).

Klik Save.

Aktifkan Sistem Cron:

Buka Settings > Administration > Basic settings.

Pada bagian Background jobs, pilih Cron. (Ini akan menggunakan container cron yang kita buat tadi).
