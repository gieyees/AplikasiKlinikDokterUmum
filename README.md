# AplikasiKlinikDokterUmum
kata farhan jangan yang aneh aneh - Tim 2
- Afdeylah Panca (01)
- Anggi Rahmawati (03)
- Farhan Kayyis Gaza (11)

1. Trigger Nomor Antrian Otomatis
Penjelasan :

Trigger ini digunakan untuk menghasilkan nomor antrian secara otomatis setiap kali data pendaftaran pasien ditambahkan. Sistem akan mengambil nomor antrian terakhir pada tanggal yang sama, kemudian menambahkannya sebesar satu. Jika belum terdapat data pada hari tersebut, maka nomor antrian dimulai dari satu.

2. Trigger Waktu Diterima Petugas
Penjelasan :

Trigger ini berfungsi untuk mencatat waktu saat pasien pertama kali didaftarkan oleh petugas. Nilai waktu diisi secara otomatis oleh sistem sehingga tidak memerlukan input manual.

3. Trigger Waktu Selesai
Penjelasan :

Trigger ini mencatat waktu selesai pemeriksaan ketika status pasien berubah menjadi "selesai". Data ini dapat digunakan untuk mengetahui durasi pelayanan pasien.

4. Trigger Perhitungan Subtotal Resep
Penjelasan :

Trigger ini digunakan untuk menghitung subtotal harga obat secara otomatis. Nilai subtotal diperoleh dari hasil perkalian antara harga obat dan jumlah obat yang diresepkan.

5. Trigger Perhitungan Total Pembayaran
Penjelasan :

Trigger ini menjumlahkan seluruh subtotal dari data resep dalam satu pemeriksaan. Hasil penjumlahan tersebut disimpan sebagai total pembayaran pada tabel pembayaran.

6. Trigger Penentuan Biaya Berdasarkan Status BPJS
Penjelasan :

Trigger ini digunakan untuk menentukan biaya berdasarkan status pasien. Jika pasien memiliki status BPJS, maka total pembayaran akan diatur menjadi nol dan status pembayaran menjadi "Gratis". Jika tidak, maka status pembayaran ditetapkan sebagai "Belum Bayar".

BEFORE
Nomor antrian → BEFORE INSERT 
Waktu diterima → BEFORE INSERT
Waktu selesai → BEFORE UPDATE
BPJS gratis → BEFORE INSERT
AFTER
Total pembayaran → AFTER INSERT
Status obat → AFTER INSERT

Kesimpulan : 
Trigger digunakan untuk mengotomatisasi berbagai proses dalam basis data, seperti penomoran antrian, pencatatan waktu pelayanan, perhitungan biaya, serta penentuan status pembayaran. Penggunaan trigger meningkatkan efisiensi sistem, menjaga konsistensi data, serta mengurangi kemungkinan kesalahan akibat input manual.
