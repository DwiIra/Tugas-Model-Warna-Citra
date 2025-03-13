# Tugas-Model-Warna-Citra
1. Citra Negatif <br>
Kondisi Input:<br>
Citra dengan nilai piksel antara 0 dan 255.<br>
Kondisi Output:<br>
Citra di mana setiap piksel I diubah menjadi 255 - I.<br>
Hasilnya adalah citra dengan kontras yang tinggi, di mana area gelap menjadi terang dan sebaliknya.<br>
<br>
3. Transformasi Log<br>
Kondisi Input:<br>
Citra dengan intensitas piksel yang bervariasi secara besar.<br>
Kondisi Output:<br>
Citra dengan transformasi O = c * log(1 + I) (di mana I adalah intensitas input dan c adalah konstanta skala).<br>
Meningkatkan detail di area dengan intensitas rendah dan mengurangi detail di area dengan intensitas tinggi.<br>
<br>
3. Transformasi Power Law<br>
Kondisi Input:<br>
Citra dengan nilai piksel yang bervariasi.<br>
Kondisi Output:<br>
Citra diubah menggunakan rumus O = c * I^γ (di mana γ adalah eksponen yang menentukan level kecerahan).<br>
Mengontrol kontras dan kecerahan citra; nilai γ < 1 meningkatkan kecerahan, sedangkan γ > 1 meningkatkan kontras.<br>
<br>
4. Histogram Equalization<br>
Kondisi Input:<br>
Citra dengan distribusi intensitas piksel yang tidak merata.<br>
Kondisi Output:<br>
Citra yang memiliki histogram mendekati uniform, meningkatkan kontras global.<br>
Membantu dalam memperbaiki citra yang terlalu gelap atau terlalu terang.<br>
<br>
5. Histogram Normalization<br>
Kondisi Input:<br>
Citra dengan rentang intensitas piksel yang bervariasi.<br>
Kondisi Output:<br>
Rentang intensitas piksel distandarisasi antara nilai tertentu (misalnya, 0-255).<br>
Memastikan bahwa distribusi intensitas lebih merata dan tidak ada piksel yang terbuang di luar rentang yang ditentukan.<br>
<br>
6. Konversi RGB ke HSI dan Thresholding<br>
Kondisi Input:<br>
Citra berformat RGB yang terdiri dari tiga channel (Merah, Hijau, Biru).<br>
Kondisi Output:<br>
Citra berformat HSI yang terdiri dari tiga channel (Hue, Saturation, Intensity).<br>
Melalui konversi ini, dapat dilakukan thresholding berdasarkan komponen Intensitas untuk segmentasi.<br>
<br>
Cara Menentukan Thresholding:<br>
1. Identifikasi Nilai Intensity:<br>
Pertama, analisis histogram dari channel Intensitas untuk menentukan distribusi piksel.<br>
2. Pemilihan Threshold:<br>
Tentukan batas (threshold) berdasarkan pemisah intensitas yang diinginkan. Misalnya, bisa memilih nilai tengah dari histogram untuk memisahkan objek dari latar belakang.<br>
3. Aplikasi Threshold:<br>
Ciptakan mask biner, di mana piksel yang memenuhi syarat intensitas di-set menjadi 1 (putih), dan yang tidak di-set menjadi 0 (hitam).<br>
