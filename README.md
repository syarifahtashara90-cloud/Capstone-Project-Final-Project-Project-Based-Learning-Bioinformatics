# Capstone-Project-Final-Project-Project-Based-Learning-Bioinformatics

# LAPORAN ANALISIS TRANSKRIPTOMIK
# IDENTIFIKASI GEN YANG DIEKSPRESIKAN SECARA BERBEDA PADA KANKER SERVIKS
Dibuat oleh: Syarifah Tashara

# Pendahuluan
Kanker serviks merupakan salah satu jenis kanker dengan penyumbang kematian tertinggi pada wanita didunia. Menurut data Global Burden of Cancer Study (Globocan) dari World Health Organization (WHO) tahun 2022, sekitar 36.964 (16,8%) perempuan Indonesia terkena kanker serviks paling tinggi kedua setelah kanker payudara. Faktor utama penyebab kanker serviks yaitu akibat dari infeksi Human Papilloma Virus (HPV) yang ditularkan melalui kontak seksual (Karimah et al., 2025). Infeksi HPV umumnya berkembang secara bertahap dimana sel Normal Serviks akan berubah menjadi lesi pada sel intraepitel serviks hingga akhirnya menjadi kanker (Yo & Kartika, 2023). Lesi intraepitel serviks atau Cervical intraepithelial Neoplasia (PRAKANKER SERVIKS) merupakan perubahan abNormal Serviks awal pada sel epitel serviks sebelum menjadi kanker serviks (Waghe & Neema, 2024). Lesi prakanker ini terbagi menjadi tiga tingkat perubahan yang mengindikasikan tingkat keparahan sel, yaitu PRAKANKER SERVIKS1 (perubahan sel epitel serviks ringan), PRAKANKER SERVIKS2 (perubahan sel epitel serviks sedang), dan PRAKANKER SERVIKS3 (Perubahan sel epitel serviks berat) (den Boon et al., 2015). Tingkat lesi PRAKANKER SERVIKS ini sangat penting untuk mendeteksi perubahan sel serviks secara dini dan menghentikan lesi agar tidak meluas dan berkembang menjadi kanker serviks. Beberapa metode telah dikembangkan saat ini untuk mengidentifikasi tingkat PRAKANKER SERVIKS diantaranya Pap smear dan tes HPV (Mayasari, 2025). Namun, beberapa kasus lesi PRAKANKER SERVIKS ini seringkali tidak menunjukkan adanya gejala tahap awal (Mello & Renee, 2023). Hal ini menyebabkan keterlambatan diagnosis yang menyebabkan penyakit ini berkembang menjadi kanker serviks tingkat lanjut. Perkembangan teknologi saat ini telah memungkinkan untuk mengindentifikasi perubahan ekspresi gen-gen yang berperan dalam perkembangan penyakit. Salah satu metode yang telah banyak digunakan yaitu transkriptomik yang dapat menganalisis Differentially Expressed Genes (DEGs) pada jaringan Normal Serviks hingga kanker (Shemuel et al., 2023). Melalui analisis ini, dapat diketahui juga gen-gen yang berperan dalam perkembangan lesi prakanker serviks sehingga dapat mendukung upaya deteksi dini serta pengobatan yang tepat. 
Tujuan analisis ini adalah untuk mengetahui hasil analisis Differentially Expressed Genes (DEGs) pada pasien dengan kondisi berbeda, yaitu antara jaringan serviks sehat sebagai Normal Serviks (Normal Serviks) dan jaringan prakanker serviks dengan tingkat lesi yang berbeda, yaitu Cervical Intraepithelial Neoplasia tingkat PRAKANKER SERVIKS1, PRAKANKER SERVIKS2, dan PRAKANKER SERVIKS3, serta melakukan visualisasi dan interpretasi data ekspresi gen untuk memahami perubahan gen yang berperan dalam perkembangan lesi prakanker serviks.

# Metode
**1.	Pencarian dan Pengunduhan Dataset Ekspresi Gen Publik Kanker Serviks**
Dataset yang digunakan yaitu GSE63514 Homo sapiens yang diambil dari database Gene Expression Omnibus (GEO) (https://www.ncbi.nlm.nih.gov/geo/). Dataset ini dipilih karena berisi data mengenai ekspresi gen pada sel epitel serviks normal, sel epitel prakanker serviks meliputi CIN1, CIN2, dan CIN3, hingga sel epitel kanker serviks. 

**2.	Identifikasi Differentially Expressed Genes (DEGs) Pada Kanker Serviks**
Identifikasi menggunakan alat analisis online GEO2R (https://www.ncbi.nlm.nih.gov/geo/geo2r). GEO2R digunakan untuk mengidentifikasi gen-gen yang dieskpresikan secara berbeda berdasarkan kondisi biologis atau perlakuan. Dalam analisis ini yaitu mengidentifikasi ekspresi gen yang berbeda pada sampel sel epitel serviks sehat atau normal sebanyak 24 sampel, serta sel epitel dengan tingkat lesi prakanker serviks yang berbeda diantaranya CIN1 sebanyak 14 sampel, CIN2 sebanyak 22 sampel, dan CIN 3 sebanyak 40 sampel.
Sampel dilakukan pengelompokkan yaitu Group 1 = sel epitel serviks pasien sehat (Kontrol) dan Group 2 = sel epitel pasien dengan lesi prakanker serviks CIN1, CIN2, CIN3 (penderita prakanker serviks) yang berbeda. Koreksi multiple testing menggunakan metode Benjamini & Hochberg (False Discovery Rate). Metode Benjamini & Hochberg (FDR) digunakan untuk mengurangi kemungkinan kesalahan tipe I akibat dari pengujian ribuan gen secara bersamaan. Perhitungan differential expression menggunakan metode limma. Gen dikategorikan sebagai DEGs apabila memenuhi kriteria:  Adjusted p-value < 0,05 dan |log2 fold change| ≥ 0 tertera pada Gambar 3. Untuk memastikan konsistensi hasil, analisis GEO2R dilakukan sebanyak tiga kali replikasi dengan parameter dan alur yang sama.

**3.	Analisis Visualisasi Differentially Expressed Genes (DEGs) Pada Kanker Serviks**
Analisis DEG divisualisasikan menggunakan empat visual diantaranya Volcano Plot, diagram Mean-difference plot, diagram Venn, dan Heatmap. Empat visualisasi ini untuk memudahkan menginterpretasi data. Volcano plot untuk melihat hasil distribusi gen yang mengalami peningkatan (up-regulation) dan penurunan (down-regulation) secara signifikan. Diagram Mean-difference plot digunakan untuk melihat hubungan antara rata-rata ekpresi gen dan perubahan ekspresi gen antar kelompok sampel. Diagram Venn digunakan untuk melihat adanya kesamaan gen yang signifikan antar kelompok data sampel. Heatmap digunakan untuk menampilkan pola ekspresi gen pada setiap kelompok sampel.

**4. Analisis Enrichment Gene Ontology (GO) dan KEGG**

**5. Analisis Jalur Biologis (KEGG Pathway Analysis)**

# 6. Analisis Menggunakan Perangkat R
**6.1 Persiapan Perangkat Lunak dan Pengolahan Data**


# Hasil dan Interpretasi Data

# Kesimpulan

# Daftar Pustaka
den Boon, J. A., Dohun, P., Sophia, S. W., Mark, H., Mark, S., Mark, S., Rosemary, E. Z., Zhishi, W., Stephen, M. H., Rachel, P., Meghan, S., Lisa, C., Qiuling, H., Paul, L., Joan, W., Michael, A. N., Nicolas, W., Paul, A. (2015). Molecular transitions from papillomavirus infection to cervical precancer and cancer: Role of stromal estrogen receptor signaling. The Proceedings of the National Academy of Sciences, 112(25). Doi: 10.1073/pnas.1509322112.

Globocan. (2022). Cancer Today Indonesia. World Health Organization. https://gco.iarc.who.int/media/globocan/factsheets/populations/360-indonesia-fact-sheet.pdf.

Karimah, R., Endah, I., Dwinka, S. E., Fira, S., Fatimah, N. F., Muhammad, N. H., Rizka, N. H., Desiana, W. S., Rahmah, Y. R., Lely, N., Zain, B. S., & Sonny, F. (2025). peningkatan deteksi dini kanker serviks melalui skrining HPV DNA kepada masyarakat di Institut Teknologi Sepuluh Nopember. Jurnal Pengabdian Kepada Masyarakat, 9(6), 1637-1646. Doi: 10.12962/j26139960.v9i6.9141.

Mayasari, S. P. (2025). Komparasi efikasi skrining kanker serviks menggunakan HPV DNA testing, pap smear, dan liquid biopsy: Tinjauan Sistematis. Indonesian Journal of Health Community, 6(1), 33-41. Doi: 10.31331/ijheco.v6i1.3893.

Mello, V., & Renee, K. S. (2023). Neoplasia Intraepitel Serviks. StatPearls Publishing. https://www.ncbi.nlm.nih.gov/books/NBK544371/.

Shemuel, J., Priscilla, A., Evelina, J., Daniel, R. F., Vania, G., Shaheer, A., & Arli, A. P. (2023). Analisis gen komparatif karsinoma sel skuamosa paru-paru antara individu merokok dan tidak merokok. Berita Biologi, 22(3)., 291-304. Doi: 10.14203/beritabiologi.v20i1.3991.
Waghe, T., & Neema, A. (2024). Advancements in the management of cervical intraepithelial neoplasia: a comprehensive review. Cureus, 16(4), 1-11. Doi: 10.7759/cureus.58645.
Yo, E. C., & Kartika, H. N. (2023). Molecular and host lifestyle factors associated with persistent human Papillomavirus infection and progression into cervical cancer: a literature review. Indonesian Journal of Cancer, 18(2), 227–233. Doi: 10.33371/ijoc.v18i2.1068.
