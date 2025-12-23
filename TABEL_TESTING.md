# Tabel Blackbox Testing dan User Acceptance Testing

## Gambar 3.1.12 Tabel Blackbox Testing

| No | Fitur | Skenario Uji | Input | Output Diharapkan | Hasil |
|----|-------|--------------|-------|-------------------|-------|
| 1 | Register (Guest) | Registrasi akun baru dengan data lengkap | Nama, Email, Password lengkap | Registrasi berhasil, redirect ke halaman login | Lulus |
| 2 | Register (Guest) | Registrasi akun dengan email sudah terdaftar | Email yang sudah ada di database | Pesan error email sudah digunakan | Lulus |
| 3 | Login (Admin & User) | Login dengan data valid | Email dan password yang benar | Login berhasil, redirect ke dashboard | Lulus |
| 4 | Login (Admin & User) | Login dengan password salah | Email benar, password salah | Pesan error login gagal | Lulus |
| 5 | Login (Admin & User) | Login dengan akun tidak terdaftar | Email tidak ada di database | Pesan error akun tidak terdaftar | Lulus |
| 6 | Tambah Data Project (Admin & Manager) | Menambahkan project baru dengan form lengkap | Nama, Deskripsi, Start Date, End Date, Status, Priority, Manager ID, Team IDs | Data project tersimpan di database | Lulus |
| 7 | Edit Data Project (Admin & Manager) | Mengedit data project yang sudah ada | Mengubah nama, deskripsi, atau field lain | Data project berhasil diupdate | Lulus |
| 8 | Hapus Data Project (Admin & Manager) | Menghapus project dengan klik tombol delete | ID project yang akan dihapus | Project terhapus dari sistem | Lulus |
| 9 | Tambah Data Task (Admin & Manager) | Menambahkan task baru dengan form lengkap | Title, Description, Priority, Status, Due Date, Project ID, Assignee | Data task tersimpan di database | Lulus |
| 10 | Edit Data Task (Admin & Manager) | Mengedit data task yang sudah ada | Mengubah title, description, status, atau field lain | Data task berhasil diupdate | Lulus |
| 11 | Update Status Task (All Roles) | Mengubah status task melalui dropdown | Status baru (TO_DO, IN_PROGRESS, REVIEW, DONE) | Status task berhasil diupdate | Lulus |
| 12 | Hapus Data Task (Admin & Manager) | Menghapus task dengan klik tombol delete | ID task yang akan dihapus | Task terhapus dari sistem | Lulus |
| 13 | Tambah Data Team (Admin & Manager) | Menambahkan team baru dengan form lengkap | Nama, Deskripsi, Logo, Team Head ID, Members | Data team tersimpan di database | Lulus |
| 14 | Edit Data Team (Admin & Manager) | Mengedit data team yang sudah ada | Mengubah nama, deskripsi, logo, atau members | Data team berhasil diupdate | Lulus |
| 15 | Hapus Data Team (Admin & Manager) | Menghapus team dengan klik tombol delete | ID team yang akan dihapus | Team terhapus dari sistem | Lulus |
| 16 | Tambah Data User (Admin) | Menambahkan user baru dengan form lengkap | Nama, Email, Password, Role | Data user tersimpan di database | Lulus |
| 17 | Edit Data User (Admin) | Mengedit data user yang sudah ada | Mengubah nama, email, atau role | Data user berhasil diupdate | Lulus |
| 18 | Hapus Data User (Admin) | Menghapus user dengan klik tombol delete | ID user yang akan dihapus | User terhapus dari sistem | Lulus |
| 19 | Upload Document (All Roles) | Mengunggah dokumen dengan form lengkap | Title, Description, File, Category, Project ID atau Task ID | Dokumen tersimpan dan dapat diunduh | Lulus |
| 20 | Edit Document (All Roles) | Mengedit informasi dokumen yang sudah diupload | Mengubah title, description, atau category | Data dokumen berhasil diupdate | Lulus |
| 21 | Hapus Document (Admin, Manager, Owner) | Menghapus dokumen yang diupload | ID dokumen yang akan dihapus | Dokumen terhapus dari sistem | Lulus |
| 22 | Tambah Comment (All Roles) | Menambahkan komentar pada task | Content, Type, Privacy, Attachment (opsional), Is Pinned | Komentar tersimpan dan tampil di task | Lulus |
| 23 | Edit Comment (All Roles) | Mengedit komentar yang sudah dibuat | Mengubah content atau is_pinned | Komentar berhasil diupdate | Lulus |
| 24 | Hapus Comment (Admin, Manager, Owner) | Menghapus komentar yang sudah dibuat | ID komentar yang akan dihapus | Komentar terhapus dari sistem | Lulus |
| 25 | Lihat Dashboard (All Roles) | Mengakses halaman dashboard | Session user yang valid | Dashboard menampilkan statistik dan informasi sesuai role | Lulus |
| 26 | Lihat Projects (All Roles) | Melihat daftar projects | Session user yang valid | Menampilkan projects yang dapat diakses sesuai role | Lulus |
| 27 | Filter Projects (All Roles) | Memfilter projects berdasarkan status | Status filter (PLANNING, ACTIVE, ON_HOLD, COMPLETED, CANCELLED) | Menampilkan projects dengan status yang dipilih | Lulus |
| 28 | Search Projects (All Roles) | Mencari projects berdasarkan kata kunci | Kata kunci pencarian | Menampilkan projects yang sesuai dengan kata kunci | Lulus |
| 29 | Lihat Profile (All Roles) | Mengakses halaman profile | Session user yang valid | Menampilkan informasi profile user | Lulus |
| 30 | Logout (All Roles) | Melakukan logout dari sistem | Klik tombol logout | Session dihapus, redirect ke halaman login | Lulus |

---

## Gambar 3.1.13 Tabel User Acceptance Testing

| No | Aktor | Fitur | Langkah Pengujian | Hasil Diharapkan | Status |
|----|-------|-------|-------------------|------------------|--------|
| 1 | Admin | Kelola Data Projects | Login → Projects → Tambah/Edit/Hapus project | Data project terkelola dengan baik, dapat melihat semua projects | Diterima |
| 2 | Admin | Kelola Data Users | Login → Users → Tambah/Edit/Hapus user | Data user terkelola dengan baik, dapat mengatur role user | Diterima |
| 3 | Admin | Kelola Data Teams | Login → Teams → Tambah/Edit/Hapus team | Data team terkelola dengan baik, dapat mengatur anggota team | Diterima |
| 4 | Admin | Dashboard & Statistik | Login → Dashboard | Dashboard menampilkan statistik lengkap semua projects, users, teams | Diterima |
| 5 | Manager | Kelola Data Projects | Login → Projects → Tambah/Edit/Hapus project yang di-manage | Data project terkelola dengan baik, hanya dapat mengelola projects yang menjadi manager | Diterima |
| 6 | Manager | Kelola Data Tasks | Login → Project Detail → Tasks → Tambah/Edit/Hapus task | Task terkelola dengan baik dalam project yang di-manage | Diterima |
| 7 | Manager | Kelola Data Teams | Login → Teams → Tambah/Edit/Hapus team | Data team terkelola dengan baik | Diterima |
| 8 | Manager | Dashboard & Statistik | Login → Dashboard | Dashboard menampilkan statistik projects yang di-manage dan tasks distribution | Diterima |
| 9 | Member | Lihat Projects | Login → Projects | Dapat melihat projects yang terlibat (sebagai anggota team) | Diterima |
| 10 | Member | Lihat & Update Tasks | Login → Project Detail → Tasks → Lihat detail task, update status task yang ditugaskan | Dapat melihat tasks dan mengupdate status task yang ditugaskan kepadanya | Diterima |
| 11 | Member | Upload & Kelola Documents | Login → Project/Task Detail → Documents → Upload/Edit/Hapus document sendiri | Dapat mengunggah, mengedit, dan menghapus dokumen yang diupload sendiri | Diterima |
| 12 | Member | Komentar pada Task | Login → Task Detail → Comments → Tambah/Edit/Hapus komentar sendiri | Dapat menambahkan, mengedit, dan menghapus komentar pada task dengan privasi sesuai pilihan | Diterima |
| 13 | Member | Dashboard & My Tasks | Login → Dashboard | Dashboard menampilkan tasks yang ditugaskan dan deadline reminder | Diterima |
| 14 | Member | Profile | Login → Profile | Dapat melihat informasi profile sendiri | Diterima |
| 15 | Guest | Register | Akses halaman register → Isi form → Submit | Dapat membuat akun baru sebagai Member | Diterima |
| 16 | Guest | Login | Akses halaman login → Masukkan email dan password → Submit | Dapat masuk ke sistem setelah registrasi | Diterima |
| 17 | All Roles | Logout | Login → Klik dropdown user → Logout | Dapat keluar dari sistem dengan aman, session dihapus | Diterima |
| 18 | All Roles | Pencarian & Filter Projects | Login → Projects → Gunakan search dan filter | Dapat mencari dan memfilter projects dengan mudah | Diterima |
| 19 | All Roles | Detail Project | Login → Projects → Klik project → Project Detail | Dapat melihat detail project lengkap dengan tasks dan documents | Diterima |
| 20 | All Roles | Detail Task | Login → Project Detail → Klik task → Task Detail | Dapat melihat detail task lengkap dengan comments dan documents terkait | Diterima |

