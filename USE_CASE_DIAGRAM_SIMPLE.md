# Use Case Diagram Sistem Manajemen Proyek (Format Sederhana)

## Struktur Diagram Berdasarkan Referensi

Diagram ini mengikuti pola referensi dengan aktor di kiri dan kanan, use case di tengah.

```
                              [Sistem Manajemen Proyek]
                                         |
                    +--------------------+--------------------+
                    |                                         |
            [Admin]                                        [Member]
                    |                                         |
        +-----------+-----------+                 +-----------+-----------+
        |                       |                 |                       |
    [Login]              [Data Projects]    [Login]              [Informasi Projects]
        |                       |                 |                       |
        |                   [Data Tasks]          |                   [Informasi Tasks]
        |                       |                 |                       |
        |                   [Data Teams]          |                   [Form Update Status Task]
        |                       |                 |                       |
        |                   [Data Users]          |                       |
        |                       |                 |                       |
        +-----------------------+                 +-----------------------+
                    |                                         |
            [Dashboard]                                 [Dashboard]
            [Profile]                                   [Profile]
            [Upload Document]                           [Upload Document]
            [Edit Document]                             [Edit Document]
            [Tambah Comment]                            [Tambah Comment]
            [Edit Comment]                              [Edit Comment]
            [Hapus Comment]                             [Logout]
            [Logout]
```

---

## Detail Use Cases per Aktor

### Aktor: Guest
- **Register** - Membuat akun baru
- **Login** - Masuk ke sistem

### Aktor: Admin
Setelah Login:
- **Data Projects** - Kelola data proyek (Create, Read, Update, Delete)
- **Data Tasks** - Kelola data tugas
- **Data Teams** - Kelola data tim
- **Data Users** - Kelola data pengguna
- **Dashboard** - Melihat statistik lengkap sistem
- **Profile** - Melihat informasi profile
- **Upload Document** - Mengunggah dokumen
- **Edit Document** - Mengedit dokumen
- **Hapus Document** - Menghapus dokumen (semua dokumen)
- **Tambah Comment** - Menambahkan komentar
- **Edit Comment** - Mengedit komentar
- **Hapus Comment** - Menghapus komentar (semua komentar)
- **Logout** - Keluar dari sistem

### Aktor: Manager
Setelah Login:
- **Data Projects** - Kelola data proyek yang di-manage
- **Data Tasks** - Kelola data tugas dalam project yang di-manage
- **Data Teams** - Kelola data tim
- **Dashboard** - Melihat statistik projects yang di-manage
- **Profile** - Melihat informasi profile
- **Upload Document** - Mengunggah dokumen
- **Edit Document** - Mengedit dokumen
- **Hapus Document** - Menghapus dokumen dalam project yang di-manage
- **Tambah Comment** - Menambahkan komentar
- **Edit Comment** - Mengedit komentar
- **Hapus Comment** - Menghapus komentar dalam project yang di-manage
- **Logout** - Keluar dari sistem

### Aktor: Member
Setelah Login:
- **Informasi Projects** - Melihat informasi proyek yang terlibat
- **Informasi Tasks** - Melihat informasi tugas yang ditugaskan
- **Form Update Status Task** - Mengupdate status tugas yang ditugaskan
- **Dashboard** - Melihat tasks yang ditugaskan dan deadline reminder
- **Profile** - Melihat informasi profile
- **Upload Document** - Mengunggah dokumen sendiri
- **Edit Document** - Mengedit dokumen yang diupload sendiri
- **Tambah Comment** - Menambahkan komentar pada task
- **Edit Comment** - Mengedit komentar sendiri
- **Logout** - Keluar dari sistem

---

## Relasi Dependency (Include/Extend)

### Include Relationships:
1. **Data Projects** <<include>> **Dashboard** - Dashboard menampilkan informasi projects
2. **Data Tasks** <<include>> **Data Projects** - Tasks terkait dengan Projects
3. **Informasi Tasks** <<include>> **Informasi Projects** - Tasks terkait dengan Projects
4. **Form Update Status Task** <<include>> **Informasi Tasks** - Update status dilakukan pada task
5. **Upload Document** <<include>> **(Projects atau Tasks)** - Document terkait dengan Project atau Task
6. **Tambah Comment** <<include>> **Informasi Tasks** - Comment dilakukan pada Task

### Penjelasan Relasi Berdasarkan Kode:
- Semua fitur memerlukan **Login** terlebih dahulu (auth_check.php)
- **Data Projects** menghasilkan data yang ditampilkan di **Dashboard**
- **Data Tasks** dibuat dalam konteks **Data Projects** (project_id foreign key)
- **Informasi Tasks** ditampilkan dalam detail **Informasi Projects**
- **Form Update Status Task** memerlukan akses ke **Informasi Tasks**
- **Upload Document** dapat dilakukan dari halaman Project atau Task detail
- **Tambah Comment** dilakukan pada halaman Task detail

---

## Tabel Mapping Use Case ke File Kode

| Use Case | File/Folder Kode | Role Akses |
|----------|------------------|------------|
| Register | register.php | Guest |
| Login | login.php | Guest, Admin, Manager, Member |
| Data Projects | form_project.php, projects.php, handle/project/* | Admin, Manager |
| Data Tasks | form_task.php, task_detail.php, handle/task/* | Admin, Manager |
| Data Teams | form_team.php, teams.php, team_detail.php, handle/team/* | Admin, Manager |
| Data Users | form_user.php, users.php, handle/user/* | Admin |
| Informasi Projects | projects.php, project_detail.php | All (filtered by role) |
| Informasi Tasks | task_detail.php | All (filtered by role) |
| Form Update Status Task | task_detail.php, handle/task/handle_update_task_status.php | All (for assigned tasks) |
| Dashboard | dashboard.php | All (with different stats) |
| Profile | profile.php | All |
| Upload Document | form_document.php, handle/document/handle_create_document.php | All |
| Edit Document | form_document.php, handle/document/handle_update_document.php | All (own documents) |
| Hapus Document | handle/document/handle_delete_document.php | Admin, Manager, Owner |
| Tambah Comment | task_detail.php, handle/comment/handle_create_comment.php | All |
| Edit Comment | form_comment.php, handle/comment/handle_update_comment.php | All (own comments) |
| Hapus Comment | handle/comment/handle_delete_comment.php | Admin, Manager, Owner |
| Logout | logout.php | All |

---

## Notasi Diagram (Mengikuti Referensi)

- **Aktor**: Stick figure (dilambangkan dengan nama dalam kurung siku [])
- **Use Case**: Oval (dilambangkan dengan nama dalam kurung biasa ())
- **Sistem Boundary**: Rectangle (Sistem Manajemen Proyek)
- **Association**: Garis dari aktor ke use case
- **Dependency (Include)**: Garis putus-putus dengan panah dan label <<include>>

