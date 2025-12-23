# Tabel Blackbox Testing dan User Acceptance Testing

## Gambar 3.1.12 Tabel Blackbox Testing

| No | Fitur | Skenario Uji | Input | Output Diharapkan | Hasil |
|---|---|---|---|---|---|
| 1 | Register (Guest) | Registrasi akun baru dengan data lengkap | Nama, Email, Password yang valid | Registrasi berhasil dan redirect ke halaman login | Lulus |
| 2 | Register (Guest) | Registrasi dengan email yang sudah terdaftar | Nama, Email yang sudah ada di database, Password | Pesan error email sudah terdaftar | Lulus |
| 3 | Login (Admin & User) | Login dengan data valid | Email dan password yang benar | Login berhasil dan redirect ke dashboard | Lulus |
| 4 | Login (Admin & User) | Login dengan password salah | Email benar, password salah | Pesan error password salah | Lulus |
| 5 | Login (Admin & User) | Login dengan akun tidak terdaftar | Email yang tidak ada di database, password | Pesan error akun tidak terdaftar | Lulus |
| 6 | Tambah Data Proyek (Admin & Manager) | Menambahkan proyek baru dengan form lengkap | Nama, Deskripsi, Start Date, End Date, Status, Priority, Manager ID, Team IDs | Data proyek tersimpan di database dan redirect ke detail proyek | Lulus |
| 7 | Edit Data Proyek (Admin & Manager) | Mengedit data proyek yang sudah ada | Data proyek yang diubah pada form edit | Data proyek berhasil diupdate di database | Lulus |
| 8 | Hapus Data Proyek (Admin & Manager) | Menghapus proyek dengan klik tombol delete | Konfirmasi penghapusan proyek | Data proyek terhapus dari sistem | Lulus |
| 9 | Tambah Data Tim (Admin & Manager) | Menambahkan tim baru dengan form lengkap | Nama, Deskripsi, Logo, Team Head ID, Team Members | Data tim tersimpan di database | Lulus |
| 10 | Edit Data Tim (Admin & Manager) | Mengedit data tim yang sudah ada | Data tim yang diubah pada form edit | Data tim berhasil diupdate di database | Lulus |
| 11 | Hapus Data Tim (Admin & Manager) | Menghapus tim dengan klik tombol delete | Konfirmasi penghapusan tim | Data tim terhapus dari sistem | Lulus |
| 12 | Tambah Data Tugas (Admin & Manager) | Menambahkan tugas baru dengan form lengkap | Title, Deskripsi, Priority, Status, Due Date, Project ID, Assignee | Data tugas tersimpan di database | Lulus |
| 13 | Edit Data Tugas (Admin & Manager) | Mengedit data tugas yang sudah ada | Data tugas yang diubah pada form edit | Data tugas berhasil diupdate di database | Lulus |
| 14 | Update Status Tugas | Mengubah status tugas | Status baru (TO_DO, IN_PROGRESS, REVIEW, DONE) | Status tugas berhasil diupdate | Lulus |
| 15 | Hapus Data Tugas (Admin & Manager) | Menghapus tugas dengan klik tombol delete | Konfirmasi penghapusan tugas | Data tugas terhapus dari sistem | Lulus |
| 16 | Tambah Data Pengguna (Admin) | Menambahkan pengguna baru dengan form lengkap | Nama, Email, Password, Role | Data pengguna tersimpan di database | Lulus |
| 17 | Edit Data Pengguna (Admin) | Mengedit data pengguna yang sudah ada | Data pengguna yang diubah pada form edit | Data pengguna berhasil diupdate di database | Lulus |
| 18 | Hapus Data Pengguna (Admin) | Menghapus pengguna dengan klik tombol delete | Konfirmasi penghapusan pengguna | Data pengguna terhapus dari sistem | Lulus |
| 19 | Upload Dokumen | Mengunggah dokumen ke proyek atau tugas | File dokumen, Title, Deskripsi, Kategori, Project ID/Task ID | Dokumen tersimpan di server dan database | Lulus |
| 20 | Edit Dokumen | Mengedit informasi dokumen | Title, Deskripsi, Kategori yang diubah | Informasi dokumen berhasil diupdate | Lulus |
| 21 | Hapus Dokumen | Menghapus dokumen dari sistem | Konfirmasi penghapusan dokumen | Dokumen terhapus dari server dan database | Lulus |
| 22 | Tambah Komentar | Menambahkan komentar pada tugas | Content, Type, Privacy, File attachment (opsional) | Komentar tersimpan di database | Lulus |
| 23 | Edit Komentar | Mengedit komentar yang sudah ada | Content komentar yang diubah | Komentar berhasil diupdate di database | Lulus |
| 24 | Hapus Komentar | Menghapus komentar dari tugas | Konfirmasi penghapusan komentar | Komentar terhapus dari database | Lulus |
| 25 | Search Proyek | Mencari proyek berdasarkan kata kunci | Kata kunci pencarian | Menampilkan daftar proyek yang sesuai dengan kata kunci | Lulus |
| 26 | Filter Proyek | Memfilter proyek berdasarkan status | Status proyek (PLANNING, ACTIVE, ON_HOLD, COMPLETED, CANCELLED) | Menampilkan daftar proyek sesuai status yang dipilih | Lulus |
| 27 | Lihat Detail Proyek | Mengakses halaman detail proyek | ID proyek | Menampilkan informasi lengkap proyek, tugas, dan dokumen | Lulus |
| 28 | Lihat Detail Tugas | Mengakses halaman detail tugas | ID tugas | Menampilkan informasi lengkap tugas, komentar, dan dokumen | Lulus |
| 29 | Lihat Detail Tim | Mengakses halaman detail tim | ID tim | Menampilkan informasi lengkap tim dan anggota tim | Lulus |

## Gambar 3.1.13 Tabel User Acceptance Testing

| No | Aktor | Fitur | Langkah Pengujian | Hasil Diharapkan | Status |
|---|---|---|---|---|---|
| 1 | Admin | Kelola Data Proyek | Login → Menu Projects → Tambah/Edit/Hapus proyek | Data proyek terkelola dengan baik | Diterima |
| 2 | Admin | Kelola Data Tim | Login → Menu Teams → Tambah/Edit/Hapus tim | Data tim terkelola dengan baik | Diterima |
| 3 | Admin | Kelola Data Pengguna | Login → Menu Users → Tambah/Edit/Hapus pengguna | Data pengguna terkelola dengan baik | Diterima |
| 4 | Admin | Lihat Dashboard | Login → Dashboard | Menampilkan statistik proyek aktif, tim, pengguna, dan distribusi tugas | Diterima |
| 5 | Admin | Akses Semua Proyek | Login → Menu Projects | Dapat melihat dan mengakses semua proyek tanpa filter | Diterima |
| 6 | Manager | Kelola Data Proyek | Login → Menu Projects → Tambah/Edit/Hapus proyek yang dimanage | Data proyek terkelola dengan baik | Diterima |
| 7 | Manager | Kelola Data Tim | Login → Menu Teams → Tambah/Edit/Hapus tim | Data tim terkelola dengan baik | Diterima |
| 8 | Manager | Kelola Data Tugas | Login → Detail Proyek → Tambah/Edit/Hapus tugas | Data tugas terkelola dengan baik | Diterima |
| 9 | Manager | Upload Dokumen | Login → Detail Proyek/Tugas → Upload dokumen | Dokumen berhasil diunggah dan tersimpan | Diterima |
| 10 | Manager | Lihat Dashboard | Login → Dashboard | Menampilkan statistik proyek yang dimanage, tim, dan distribusi tugas | Diterima |
| 11 | Manager | Filter Proyek | Login → Menu Projects → Filter berdasarkan status | Menampilkan proyek sesuai filter status yang dipilih | Diterima |
| 12 | Manager | Search Proyek | Login → Menu Projects → Search dengan kata kunci | Menampilkan proyek yang sesuai dengan kata kunci pencarian | Diterima |
| 13 | Manager | Kelola Komentar | Login → Detail Tugas → Tambah/Edit/Hapus komentar | Komentar terkelola dengan baik | Diterima |
| 14 | Member | Lihat Data Proyek | Login → Menu Projects | Dapat melihat proyek yang terlibat (sebagai anggota tim) | Diterima |
| 15 | Member | Lihat Detail Proyek | Login → Menu Projects → Klik detail proyek | Menampilkan informasi lengkap proyek yang terlibat | Diterima |
| 16 | Member | Lihat Tugas yang Ditugaskan | Login → Dashboard → My Tasks | Menampilkan daftar tugas yang ditugaskan kepada member | Diterima |
| 17 | Member | Update Status Tugas | Login → Detail Tugas → Ubah status tugas | Status tugas berhasil diupdate | Diterima |
| 18 | Member | Tambah Komentar | Login → Detail Tugas → Tambah komentar | Komentar berhasil ditambahkan pada tugas | Diterima |
| 19 | Member | Lihat Dokumen | Login → Detail Proyek/Tugas → Lihat dokumen | Dapat melihat dan mengunduh dokumen yang ada | Diterima |
| 20 | Member | Upload Dokumen | Login → Detail Proyek/Tugas → Upload dokumen | Dokumen berhasil diunggah | Diterima |
| 21 | Member | Lihat Dashboard | Login → Dashboard | Menampilkan statistik proyek yang terlibat dan tugas yang ditugaskan | Diterima |
| 22 | Member | Edit Profile | Login → Profile → Edit data profil | Data profil berhasil diupdate | Diterima |
| 23 | Member | Logout | Login → Klik tombol logout | Berhasil logout dan redirect ke halaman login | Diterima |
| 24 | Guest | Register | Akses halaman register → Isi form → Submit | Berhasil registrasi dan redirect ke halaman login | Diterima |
| 25 | Guest | Login | Akses halaman login → Masukkan email dan password → Submit | Berhasil login sesuai role dan redirect ke dashboard | Diterima |

