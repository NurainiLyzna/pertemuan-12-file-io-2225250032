# Pertemuan 12: File I/O dan Error Handling

## Identitas
* **Nama:** Lyzna Nuraini
* **NIM:** 2225250032
* **Kelas:** 3E - Pendidikan Matematika FKIP Untirta
* **Mata Kuliah:** Algoritma dan Pemrograman

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file dengan Python secara terstruktur serta aman menggunakan penanganan error dasar (`try-except`).

## Format File Input (`data/nilai.txt`)
File input menggunakan format teks sederhana dengan pemisah koma (`NIM, nilai`):
```text
A001,85
A002,78
A003,92
A004,abc
A005,74
A006,88

## Struktur Repositori
pertemuan-12-file-io-NIM/[cite: 5]
├── .gitignore[cite: 5]
├── README.md[cite: 5]
├── data/[cite: 5]
│   ├── catatan.txt[cite: 5]
│   ├── nilai.txt[cite: 5]
│   └── hasil_rekap.txt[cite: 5]
├── latihan/[cite: 5]
│   ├── 01_tulis_file.py[cite: 5]
│   ├── 02_baca_file.py[cite: 5]
│   ├── 03_append_file.py[cite: 5]
│   ├── 04_proses_baris.py[cite: 5]
│   ├── 05_file_not_found.py[cite: 5]
│   └── 06_value_error.py[cite: 5]
└── tugas/[cite: 5]
    └── rekap_nilai_file.py[cite: 5]

## Cara Menjalankan
```bash
python3 tugas/rekap_nilai_file.py
```[cite: 13]

## Error yang Ditangani
* `FileNotFoundError`[cite: 13]
* `ValueError`[cite: 13]

## Test Case
| Kasus | Kondisi | Hasil yang Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- | :--- |
| **Normal**[cite: 13] | Semua baris valid[cite: 13] | Semua record diproses dan rekap benar.[cite: 13] | Sesuai | Lulus |
| **File hilang**[cite: 13] | `nilai.txt` tidak tersedia[cite: 13] | Pesan file tidak ditemukan; program tidak *crash*.[cite: 13] | Sesuai | Lulus |
| **Nilai invalid**[cite: 13] | `A004,abc`[cite: 13] | Baris invalid dilewati/dilaporkan; record lain tetap diproses.[cite: 13] | Sesuai | Lulus |
| **Baris kosong**[cite: 13] | Ada baris kosong[cite: 13] | Baris kosong dilewati.[cite: 13] | Sesuai | Lulus |
| **Batas lulus**[cite: 13] | Nilai 60[cite: 13] | Dihitung sebagai lulus.[cite: 13] | Sesuai | Lulus |

## Refleksi
Dalam praktikum ini, salah satu error yang ditemukan adalah `ValueError` yang disebabkan oleh adanya data teks pada kolom nilai (seperti `A004, abc`). Program mengantisipasi hal ini dengan menggunakan blok `try-except` di tingkat baris (*per-line*), sehingga baris yang rusak dapat dilewati dengan peringatan, sementara data valid lainnya tetap berhasil diproses dan direkap ke dalam file keluaran tanpa menghentikan jalannya program secara keseluruhan[cite: 8, 12, 13].

## Struktur Repositori
pertemuan-12-file-io-NIM/[cite: 5]
├── .gitignore[cite: 5]
├── README.md[cite: 5]
├── data/[cite: 5]
│   ├── catatan.txt[cite: 5]
│   ├── nilai.txt[cite: 5]
│   └── hasil_rekap.txt[cite: 5]
├── latihan/[cite: 5]
│   ├── 01_tulis_file.py[cite: 5]
│   ├── 02_baca_file.py[cite: 5]
│   ├── 03_append_file.py[cite: 5]
│   ├── 04_proses_baris.py[cite: 5]
│   ├── 05_file_not_found.py[cite: 5]
│   └── 06_value_error.py[cite: 5]
└── tugas/[cite: 5]
    └── rekap_nilai_file.py[cite: 5]

## Cara Menjalankan
```bash
python3 tugas/rekap_nilai_file.py
```[cite: 13]

## Error yang Ditangani
* `FileNotFoundError`[cite: 13]
* `ValueError`[cite: 13]

## Test Case
| Kasus | Kondisi | Hasil yang Diharapkan | Hasil Aktual | Status |
| :--- | :--- | :--- | :--- | :--- |
| **Normal**[cite: 13] | Semua baris valid[cite: 13] | Semua record diproses dan rekap benar.[cite: 13] | Sesuai | Lulus |
| **File hilang**[cite: 13] | `nilai.txt` tidak tersedia[cite: 13] | Pesan file tidak ditemukan; program tidak *crash*.[cite: 13] | Sesuai | Lulus |
| **Nilai invalid**[cite: 13] | `A004,abc`[cite: 13] | Baris invalid dilewati/dilaporkan; record lain tetap diproses.[cite: 13] | Sesuai | Lulus |
| **Baris kosong**[cite: 13] | Ada baris kosong[cite: 13] | Baris kosong dilewati.[cite: 13] | Sesuai | Lulus |
| **Batas lulus**[cite: 13] | Nilai 60[cite: 13] | Dihitung sebagai lulus.[cite: 13] | Sesuai | Lulus |

## Refleksi
Dalam praktikum ini, salah satu error yang ditemukan adalah `ValueError` yang disebabkan oleh adanya data teks pada kolom nilai (seperti `A004, abc`). Program mengantisipasi hal ini dengan menggunakan blok `try-except` di tingkat baris (*per-line*), sehingga baris yang rusak dapat dilewati dengan peringatan, sementara data valid lainnya tetap berhasil diproses dan direkap ke dalam file keluaran tanpa menghentikan jalannya program secara keseluruhan[cite: 8, 12, 13].