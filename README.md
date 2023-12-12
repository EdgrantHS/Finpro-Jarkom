# README - Proyek Jaringan Netlab Corp

## Deskripsi Proyek
Proyek ini merupakan implementasi jaringan untuk Netlab Corp, sebuah perusahaan pendidikan dengan cabang di Jakarta, Singapura, dan Nusantara. Tujuan utama proyek ini adalah untuk menghubungkan semua cabang dan divisi perusahaan dengan menggunakan teknologi jaringan yang sesuai.

## Spesifikasi Jaringan
- **Jumlah Pegawai per Divisi:**
  - **Jakarta:**
    - Research and Development: \( 3 \* 17 \) = 51 orang
    - Finance: \( 12 \* 17 \) = 204 orang
    - Telco: \( 4 \* 17 \) = 68 orang
    - Engineer: \( 15 \* 17 \) = 255 orang
  - **Singapura:**
    - Research and Development: \( 2 \* 17 \) = 34 orang
    - Finance: \( 3 \* 17 \) = 51 orang
    - Telco: \( 3 \* 17 \) = 51 orang
    - Engineer: \( 4 \* 17 \) = 68 orang
  - **Nusantara:**
    - Research and Development: 17 orang
    - Finance: \( 2 \* 17 \) = 34 orang
    - Telco: \( 2 \* 17 + 15 \) = 49 orang
    - Engineer: \( 3 \* 17 - 5 \) = 46 orang

## Struktur Jaringan
- **Topologi:** Disesuaikan dengan kebutuhan dan layout fisik kantor.
- **Alamat IP:** Menggunakan DHCP IPv4 dengan kaidah subnetting yang benar.
- **Komunikasi Antar Divisi:** Terhubung menggunakan VLAN dan InterVLAN.
- **Keamanan Jaringan:** STP dan Etherchannel.
- **Batasan Perangkat:** Sesuai jumlah pegawai di masing-masing divisi.
- **Web Server, DNS Server, dan Email Server:** Terletak di Jakarta dan Singapura.

## Tahapan Pengerjaan
- **27 November 2023:** Mulai pengerjaan proyek.
- **11 - 15 Desember 2023:** Minggu presentasi.

## Dokumentasi
- **Command:** Dilampirkan dalam dokumentasi proyek, termasuk alasan penggunaan.
- **Tabel Pendukung:** Disertakan untuk menjelaskan alokasi sumber daya dan pengaturan jaringan.
- **Pengujian:** Hasil pengujian disertakan untuk memverifikasi kinerja jaringan.

## Penyajian
- **Physical Mode:** Topologi disusun rapi di physical mode dengan 3 kota dan 3 gedung.
- **Logical Mode:** Menggambarkan keadaan jaringan yang sesuai.
