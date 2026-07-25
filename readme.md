# SOAL LATIHAN — GAYA OSN-P INFORMATIKA/KOMPUTER
*(Disusun mengikuti format Seleksi OSN-P 2023 Bidang Informatika/Komputer)*

---

## BAGIAN A: Analitika & Logika (Isian Singkat)

**A1.**
Pak Dengklek sedang membuat plat nomor koleksi berupa 4 digit angka `d1 d2 d3 d4` (masing-masing digit bernilai 0–9). Sebuah plat disebut *unik* jika `d1 + d2 = d3 + d4`. Berapa banyak plat nomor unik yang mungkin dibuat?

**A2.**
Kwok menuliskan bilangan bulat berurutan dari 1 sampai 500 di tembok tanpa spasi, seperti berikut:
`123456789101112...499500`
Berapakah digit ke-1000 dari deretan angka tersebut?

**A3.**
Sebuah kelas berisi 20 bebek akan dibagi menjadi beberapa kelompok belajar. Setiap kelompok harus beranggotakan minimal 3 bebek. Pak Dengklek ingin tahu, ada berapa banyak cara berbeda untuk menentukan **jumlah kelompok** (bukan susunan anggotanya, cukup jumlah kelompoknya) sedemikian sehingga seluruh 20 bebek habis dibagi rata ke dalam kelompok-kelompok berukuran sama, dan setiap kelompok berisi minimal 3 bebek?

---

## BAGIAN B: Problem Solving (Soal Cerita)

### B1. Menyusun Balok

**DESKRIPSI CERITA**

Pak Dengklek memiliki N buah balok tersusun berjajar dari kiri ke kanan, dengan tinggi balok ke-i adalah H_i (H_i ≥ 1). Pak Dengklek ingin memilih satu **subarray** (balok-balok yang bersebelahan/berurutan) untuk dipajang. Agar terlihat estetis, selisih antara balok tertinggi dan balok terpendek pada subarray yang dipilih tidak boleh lebih dari K.

Di antara semua subarray yang memenuhi syarat tersebut, Pak Dengklek ingin memilih yang **jumlah tinggi totalnya sebesar mungkin**. Bantulah Pak Dengklek menentukan jumlah total tinggi balok maksimum tersebut!

**PERTANYAAN ISIAN SINGKAT**

Untuk menjawab pertanyaan 1 dan 2, gunakan data berikut:
N = 8, H = {4, 1, 5, 6, 2, 8, 7, 3}

1. Jika K = 3, berapakah jumlah total tinggi balok maksimum dari subarray yang memenuhi syarat?
   Jawaban: ……………. *{tuliskan jawaban dalam bentuk ANGKA saja}*

2. Jika K = 5, berapakah jumlah total tinggi balok maksimum dari subarray yang memenuhi syarat?
   Jawaban: ……………. *{tuliskan jawaban dalam bentuk ANGKA saja}*

**MEMBUAT PROGRAM**

3. Buatlah program menggunakan bahasa C/C++ sesuai deskripsi cerita di atas.

**Format Masukan:**
Baris pertama berisi dua buah bilangan: N (banyaknya balok) dan K (batas selisih tinggi maksimum – tinggi minimum yang diperbolehkan). Baris kedua berisi N buah bilangan bulat H_1, H_2, ..., H_N.

**Format Keluaran:**
Sebuah baris berisi satu bilangan bulat, yaitu jumlah total tinggi balok maksimum dari subarray yang memenuhi syarat.

**Peringatan:** Gunakan tipe data `long long` karena jumlah total tinggi bisa sangat besar.

**Contoh Masukan dan Keluaran:**

| Contoh Masukan | Contoh Keluaran |
|---|---|
| `8 3`<br>`4 1 5 6 2 8 7 3` | `15` |
| `8 5`<br>`4 1 5 6 2 8 7 3` | `18` |

**Penjelasan Contoh:**
Pada contoh pertama (K=3), subarray terbaik adalah {8, 7} (indeks ke-6 dan 7), dengan selisih tertinggi–terpendek = 1 ≤ 3, dan total tingginya = 15. Tidak ada subarray lain yang memenuhi syarat dengan total lebih besar dari 15.

**Batasan:**
Untuk semua kasus uji berlaku:
- 1 ≤ N ≤ 100.000
- 0 ≤ K ≤ 10^9
- 1 ≤ H_i ≤ 10^9

**Subtask 1 (25%):** N ≤ 1.000 (boleh solusi O(N²))
**Subtask 2 (25%):** Seluruh nilai H_i berbeda satu sama lain
**Subtask 3 (50%):** Tidak ada batasan tambahan

---

### B2. Menghubungkan Sekolah dengan Internet

**DESKRIPSI CERITA**

Pak Dengklek adalah kepala dinas pendidikan yang ingin menghubungkan N buah sekolah (dinomori 1 s/d N) dengan jaringan kabel fiber optik agar semua sekolah dapat saling terhubung (baik langsung maupun tidak langsung). Terdapat K calon jalur kabel yang bisa dibangun, masing-masing menghubungkan sepasang sekolah dengan biaya pemasangan tertentu.

Pak Dengklek ingin memilih beberapa jalur kabel (dari K calon jalur yang ada) sedemikian sehingga **semua sekolah saling terhubung**, dengan **total biaya pemasangan sekecil mungkin**.

**PERTANYAAN ISIAN SINGKAT**

Untuk menjawab pertanyaan 1 dan 2, perhatikan data berikut.
N = 6 sekolah, dengan K = 9 calon jalur kabel (format: sekolah A, sekolah B, biaya):
```
1 2 4
1 3 1
2 3 2
2 4 5
3 4 8
3 5 10
4 5 2
4 6 6
5 6 3
```

1. Berapakah total biaya minimum agar semua 6 sekolah saling terhubung?
   Jawaban: ……………. *{tuliskan jawaban dalam bentuk ANGKA saja}*

2. Jika calon jalur kabel antara sekolah 2 dan sekolah 4 (biaya 5) ternyata **tidak bisa dibangun** (dihapus dari daftar calon jalur), berapakah total biaya minimum yang baru?
   Jawaban: ……………. *{tuliskan jawaban dalam bentuk ANGKA saja}*

**MEMBUAT PROGRAM**

3. Buatlah program menggunakan bahasa C/C++ sesuai deskripsi cerita di atas.

**Format Masukan:**
Baris pertama berisi dua buah bilangan: N (banyaknya sekolah) dan K (banyaknya calon jalur kabel). K baris berikutnya masing-masing berisi tiga bilangan bulat U, V, dan C, yang menyatakan sebuah calon jalur kabel yang menghubungkan sekolah U dan sekolah V dengan biaya C.

**Format Keluaran:**
Sebuah baris berisi satu bilangan bulat, yaitu total biaya minimum agar semua sekolah saling terhubung. Jika tidak mungkin menghubungkan semua sekolah, keluarkan -1.

**Peringatan:** Gunakan tipe data `long long` karena total biaya bisa sangat besar.

**Contoh Masukan dan Keluaran:**

| Contoh Masukan | Contoh Keluaran |
|---|---|
| `6 9`<br>`1 2 4`<br>`1 3 1`<br>`2 3 2`<br>`2 4 5`<br>`3 4 8`<br>`3 5 10`<br>`4 5 2`<br>`4 6 6`<br>`5 6 3` | `13` |
| `4 2`<br>`1 2 5`<br>`3 4 5` | `-1` |

**Penjelasan Contoh:**
Pada contoh pertama, jalur-jalur yang dipilih adalah (1,3,1), (2,3,2), (4,5,2), (5,6,3), dan (2,4,5), dengan total biaya = 1+2+2+3+5 = 13. Ini adalah *Minimum Spanning Tree* dari graf tersebut.

Pada contoh kedua, sekolah {1,2} dan {3,4} berada pada dua komponen terpisah yang tidak ada jalur penghubungnya sama sekali, sehingga tidak mungkin seluruh sekolah terhubung. Jawabannya -1.

**Batasan:**
Untuk semua kasus uji berlaku:
- 1 ≤ N ≤ 100.000
- 0 ≤ K ≤ 200.000
- 1 ≤ U, V ≤ N, U ≠ V
- 1 ≤ C ≤ 1.000.000.000

**Subtask 1 (25%):** N ≤ 500, K ≤ 2.000
**Subtask 2 (25%):** Dijamin graf yang terbentuk dari K calon jalur selalu terhubung (jawaban tidak pernah -1)
**Subtask 3 (50%):** Tidak ada batasan tambahan

---
---
