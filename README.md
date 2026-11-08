# Tugas 3 Praktik Basis Data (MSIM4206 / STSI4105)

- **Nama**: Subhan Yoga Maulana
- **NIM**: 044876223
- **Program Studi**: Sistem Informasi
- **Fakultas**: Fakultas Sains dan Teknologi (FST)
- **Perguruan Tinggi**: Universitas Terbuka

---

## Ringkasan Praktikum

Repositori ini berisi berkas dan dokumentasi pelaksanaan Tugas 3 Mata Kuliah Praktik Basis Data yang terdiri dari:

1. **Praktikum Transaksi (ACID & Trigger)**:
   - Pengujian transaksi multi-tabel menggunakan Stored Procedure (`transaksi1` s/d `transaksi5`) dengan perintah `START TRANSACTION`, `COMMIT`, `ROLLBACK`, dan `SAVEPOINT`.
   - Pembuatan tabel `obat` dan `transaksi_obat` dengan Foreign Key `CASCADE`.
   - Pembuatan Trigger `tg_stok_obat` (`AFTER INSERT ON transaksi_obat`) untuk pemotongan stok obat otomatis.

2. **Praktikum Basis Data Terdistribusi (Replikasi Master-Slave)**:
   - Konfigurasi Server Master pada Windows (IP `192.168.56.1`, `server-id = 1`, `log-bin = mysql-bin`, `binlog-do-db = rumah_sakit`).
   - Konfigurasi Server Slave pada Linux Ubuntu di VirtualBox (IP `192.168.56.101`, `server-id = 2`, `replicate-do-db = rumah_sakit`).
   - Verifikasi jaringan Host-Only Adapter (`ping` dua arah 0% loss) dan status `Slave_IO_Running: Yes` serta `Slave_SQL_Running: Yes`.

---

## Struktur Berkas

```text
├── docs/
│   ├── TUGAS_3_SUBHAN YOGA MAULANA_044876223.pdf   # Laporan praktikum final
│   └── TUGAS_3_SUBHAN YOGA MAULANA_044876223.docx
├── erd/
│   └── skema_rumah_sakit.graphml                   # Diagram ERD (yEd Graph Editor)
├── sql/
│   ├── 00_persiapan_tugas2.sql                     # Skema awal database rumah_sakit
│   └── 01_full_transaksi_dan_trigger.sql           # Skrip DDL tabel, routine & trigger
└── video/
    └── VIDEO_DOKUMENTER_PRAKTIKUM_TUGAS3_SUBHAN_YOGA_MAULANA_044876223.mp4
```
