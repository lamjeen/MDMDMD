# Entitas dan Atribut Sistem Manajemen Proyek

Entitas utama yang terdapat pada sistem ini meliputi:

1. **Users (Pengguna)**: menyimpan data pengguna sistem seperti ID, nama, email, password, role (peran), dan tanggal dibuat.

2. **Teams (Tim)**: menyimpan data tim seperti ID, nama tim, deskripsi, path logo, ID kepala tim, dan tanggal dibuat.

3. **Projects (Proyek)**: menyimpan data proyek seperti ID, nama proyek, deskripsi, tanggal mulai, tanggal selesai, status, prioritas, ID manager, dan tanggal dibuat.

4. **Tasks (Tugas)**: menyimpan data tugas seperti ID, judul, deskripsi, prioritas, status, tanggal jatuh tempo, ID proyek, ID pembuat, ID assignee (yang ditugaskan), tanggal dibuat, dan tanggal diupdate.

5. **Documents (Dokumen)**: menyimpan data dokumen seperti ID, judul, deskripsi, path file, nama file, ukuran file, tipe file, kategori, ID pengunggah, ID proyek, ID tugas, dan tanggal diunggah.

6. **Comments (Komentar)**: menyimpan data komentar seperti ID, konten, tanggal dibuat, tanggal diupdate, ID penulis, ID tugas, tipe komentar, privasi, path file lampiran, nama file lampiran, ukuran file lampiran, tipe file lampiran, dan status pin.

7. **Project Team**: merepresentasikan relasi antara proyek dan tim yang terlibat berupa ID proyek dan ID tim.

8. **Team Members**: merepresentasikan relasi antara tim dan anggota tim berupa ID tim dan ID pengguna.

