# Tugas-Model-Warna-Citra
1. Citra Negatif
Kondisi Input:
Citra dengan nilai piksel antara 0 dan 255.
Kondisi Output:
Citra di mana setiap piksel I diubah menjadi 255 - I.
Hasilnya adalah citra dengan kontras yang tinggi, di mana area gelap menjadi terang dan sebaliknya.

3. Transformasi Log
Kondisi Input:
Citra dengan intensitas piksel yang bervariasi secara besar.
Kondisi Output:
Citra dengan transformasi O = c * log(1 + I) (di mana I adalah intensitas input dan c adalah konstanta skala).
Meningkatkan detail di area dengan intensitas rendah dan mengurangi detail di area dengan intensitas tinggi.

3. Transformasi Power Law
Kondisi Input:
Citra dengan nilai piksel yang bervariasi.
Kondisi Output:
Citra diubah menggunakan rumus O = c * I^γ (di mana γ adalah eksponen yang menentukan level kecerahan).
Mengontrol kontras dan kecerahan citra; nilai γ < 1 meningkatkan kecerahan, sedangkan γ > 1 meningkatkan kontras.

4. Histogram Equalization
Kondisi Input:
Citra dengan distribusi intensitas piksel yang tidak merata.
Kondisi Output:
Citra yang memiliki histogram mendekati uniform, meningkatkan kontras global.
Membantu dalam memperbaiki citra yang terlalu gelap atau terlalu terang.

6. Histogram Normalization
Kondisi Input:
Citra dengan rentang intensitas piksel yang bervariasi.
Kondisi Output:
Rentang intensitas piksel distandarisasi antara nilai tertentu (misalnya, 0-255).
Memastikan bahwa distribusi intensitas lebih merata dan tidak ada piksel yang terbuang di luar rentang yang ditentukan.

6. Konversi RGB ke HSI dan Thresholding
Kondisi Input:
Citra berformat RGB yang terdiri dari tiga channel (Merah, Hijau, Biru).
Kondisi Output:
Citra berformat HSI yang terdiri dari tiga channel (Hue, Saturation, Intensity).
Melalui konversi ini, dapat dilakukan thresholding berdasarkan komponen Intensitas untuk segmentasi.

Cara Menentukan Thresholding:
1. Identifikasi Nilai Intensity:
Pertama, analisis histogram dari channel Intensitas untuk menentukan distribusi piksel.
2. Pemilihan Threshold:
Tentukan batas (threshold) berdasarkan pemisah intensitas yang diinginkan. Misalnya, bisa memilih nilai tengah dari histogram untuk memisahkan objek dari latar belakang.
3. Aplikasi Threshold:
Ciptakan mask biner, di mana piksel yang memenuhi syarat intensitas di-set menjadi 1 (putih), dan yang tidak di-set menjadi 0 (hitam).
