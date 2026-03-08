**LAPORAN ANALISIS TRANSKRIPTOMIK** 

**IDENTIFIKASI GEN YANG DIEKSPRESIKAN SECARA BERBEDA  PADA KANKER SERVIKS** 

Dibuat oleh: Syarifah Tashara 

**PENDAHULUAN** 

Kanker serviks merupakan salah satu jenis kanker dengan penyumbang kematian tertinggi pada wanita di dunia. Menurut data *Global Burden of Cancer Study* (Globocan) dari *World Health Organization* (WHO) tahun 2022, sekitar 36.964 (16,8%) perempuan Indonesia terkena kanker serviks paling tinggi kedua setelah kanker payudara. Faktor utama penyebab kanker serviks yaitu akibat dari infeksi Human Papilloma Virus (HPV) yang ditularkan melalui kontak seksual (Karimah et al., 2025). Infeksi HPV umumnya berkembang secara bertahap dimana sel normal akan berubah menjadi  lesi pada sel intraepitel serviks hingga akhirnya menjadi kanker (Yo & Kartika, 2023). Lesi intraepitel serviks atau *Cervical intraepithelial Neoplasia* (CIN) merupakan perubahan abnormal awal pada sel epitel serviks sebelum menjadi kanker serviks (Waghe & Neema, 2024). Lesi prakanker ini terbagi menjadi tiga tingkat perubahan yang mengindikasikan tingkat keparahan sel, yaitu CIN1 (perubahan sel epitel serviks ringan), CIN2 (perubahan sel epitel serviks sedang), dan CIN3 (perubahan sel epitel serviks berat) (den Boon et al., 2015). Tingkat lesi CIN ini sangat penting untuk mendeteksi perubahan sel serviks secara dini dan menghentikan lesi agar tidak meluas dan berkembang menjadi kanker serviks. Beberapa  metode  telah  dikembangkan  saat  ini  untuk  mengidentifikasi  tingkat  CIN diantaranya Pap smear dan tes HPV (Mayasari, 2025). Namun, beberapa kasus lesi CIN ini seringkali tidak menunjukkan adanya gejala tahap awal (Mello & Renee, 2023). Hal ini menyebabkan keterlambatan diagnosis yang menyebabkan penyakit ini berkembang menjadi  kanker  serviks  tingkat  lanjut.  Perkembangan  teknologi  saat  ini  telah memungkinkan  untuk  mengindentifikasi  perubahan  ekspresi  gen-gen  yang  berperan dalam perkembangan penyakit. Salah satu metode yang telah banyak digunakan yaitu transkriptomik yang dapat menganalisis *Differentially Expressed Genes* (DEGs) pada jaringan  normal  hingga  kanker  (Shemuel  et  al.,  2023).  Melalui  analisis  ini,  dapat diketahui  juga  gen-gen  yang  berperan  dalam  perkembangan  lesi  prakanker  serviks sehingga dapat mendukung upaya deteksi dini serta pengobatan yang tepat.  

Tujuan analisis ini adalah untuk mengetahui hasil analisis Differentially Expressed Genes (DEGs) pada pasien dengan kondisi berbeda, yaitu antara jaringan serviks sehat sebagai kontrol (normal) dan jaringan prakanker serviks dengan tingkat lesi yang berbeda, yaitu Cervical Intraepithelial Neoplasia tingkat CIN1, CIN2, dan CIN3, serta melakukan visualisasi  dan  interpretasi  data  ekspresi  gen  untuk  memahami  perubahan  gen  yang berperan dalam perkembangan lesi prakanker serviks. 

**METODE** 

1. **Pencarian dan Pengunduhan Dataset Ekspresi Gen Publik Kanker Serviks** Dataset yang digunakan yaitu *GSE63514* *Homo sapiens* yang diambil dari database *Gene  Expression  Omnibus*  (GEO)  [(*https://www.ncbi.nlm.nih.gov/geo/*)](https://www.ncbi.nlm.nih.gov/geo/)  tertera  pada Gambar 1. Dataset ini dipilih karena berisi data mengenai ekspresi gen pada sel epitel serviks normal, sel epitel prakanker serviks meliputi CIN1, CIN2, dan CIN3, hingga sel 

   epitel kanker serviks.  

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.001.jpeg)

Gambar 1. Halaman dataset *GSE63514* pada database GEO 

2. **Identifikasi *Differentially Expressed Genes* (DEGs) Pada Kanker Serviks** Identifikasi  menggunakan  alat  analisis  *online*  GEO2R [(*https://www.ncbi.nlm.nih.gov/geo/geo2r*). ](https://www.ncbi.nlm.nih.gov/geo/geo2r) GEO2R  digunakan  untuk  mengidentifikasi gen-gen yang dieskpresikan secara berbeda berdasarkan kondisi biologis atau perlakuan. Dalam analisis ini yaitu mengidentifikasi ekspresi gen yang berbeda pada sampel sel epitel serviks sehat atau normal sebanyak 24 sampel, serta sel epitel dengan tingkat lesi prakanker serviks yang berbeda diantaranya CIN1 sebanyak 14 sampel, CIN2 sebanyak 22 sampel, dan CIN 3 sebanyak 40 sampel tertera pada Gambar 2. 

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.002.jpeg)

Gambar 2. Hasil pengelompokkan sampel gen pasien kontrol dan perlakuan penderita 

prakanker serviks 

Sampel dilakukan pengelompokkan yaitu Group 1 = sel epitel serviks pasien sehat (Kontrol) dan Group 2 = sel epitel pasien dengan lesi prakanker serviks CIN1, CIN2, CIN3 (penderita prakanker serviks) yang berbeda. Koreksi *multiple testing* menggunakan metode Benjamini & Hochberg (*False Discovery Rate*). Metode Benjamini & Hochberg (FDR) digunakan untuk mengurangi kemungkinan kesalahan tipe I akibat dari pengujian ribuan gen secara bersamaan. Perhitungan *differential expression* menggunakan metode limma. Gen dikategorikan sebagai DEGs apabila memenuhi kriteria:  *Adjusted* p-*value* < 0,05 dan |*log2* *fold change*| ≥ 0 tertera pada Gambar 3. Untuk memastikan konsistensi hasil, analisis GEO2R dilakukan sebanyak tiga kali replikasi dengan parameter dan alur yang sama. 

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.003.jpeg)

Gambar 3. Parameter untuk GEO2R pada filter kontrol dan perlakuan penderita prakanker 

serviks 

3. **Analisis Visualisasi *Differentially Expressed Genes* (DEGs) Pada Kanker Serviks** Analisis DEG divisualisasikan menggunakan empat visual diantaranya *Volcano Plot*, diagram *Mean-difference plot*, diagram *Venn*, dan *Heatmap*. Empat visualisasi ini untuk memudahkan menginterpretasi data. *Volcano plot* untuk melihat hasil distribusi gen yang mengalami  peningkatan  (up-regulation)  dan  penurunan  (down-regulation)  secara signifikan. Diagram *Mean-difference plot* digunakan untuk melihat hubungan antara rata- rata ekpresi gen dan perubahan ekspresi gen antar kelompok sampel. Diagram *Venn* digunakan untuk melihat adanya kesamaan gen yang signifikan antar kelompok data sampel. *Heatmap* digunakan untuk menampilkan pola ekspresi gen pada setiap kelompok sampel. 
3. **Analisis *Enrichment Gene Ontology* (GO) dan KEGG**  

   Gen yang signifikan kemudian dilakukan analisis *Enrichment Gene Ontology* (GO) dan  *Kyoto  Encyclopedia  of  Genes  and  Genomes*  (KEGG)  yang  tujuannya  untuk mengetahui fungsi biologis gen tersebut. Analisis ini mengelompokkan gen berdasarkan proses biologis, fungsi molekuler, dan komponen selulernya. Analisis GO dan KEGG menggunakan  bahasa  pemrograman  R  dengan  metode  *enrichment  analysis*  untuk identifikasi kategori GO dan KEGG yang signifikan dari gen-gen yang telah diperoleh. 

5. **Analisis Jalur Biologis (*KEGG Pathway Analysis*)** 

Gen  yang  terlah  dianalisis  Enrichment  selanjutnya  dianalisis  jalur  biologisnya menggunakan KEGG *Pathway analysis*. Tujuan analisis ini yaitu untuk mengetahui peta jalur tentang interaksi jaringan, reaksi, dan hubungan mekanisme molekuler yang terlibat dalam penyakit tersebut. Analisis KEGG *pathway* menggunakan *platform* ShinyGO versi 0.85.  

**HASIL DAN INTERPRETASI** 

Berdasarkan  hasil  analisis  DEG  pada  dataset  *GSE63514*  menggunakan  GEO2R diperoleh 1458 gen yang diekspresikan secara berbeda antara kelompok sampel kontrol (normal) dan penderita prakanker serviks. Gen-gen yang diekspresikan secara berbeda terdiri dari 428 gen *upregulated* dan 1030 gen *downregulated*. Hasil visualisasi Volcano Plot dan Diagram *Mean-difference plot* (Gambar 4a dan 4b) memperlihatkan sejumlah gen yang menunjukkan perbedaan ekspresi gen yang signifikan antar kedua kelompok baik kontrol dan penderita prakanker serviks. Distribusi titik-titik plot yang mewakili sebuah gen terlihat cukup banyak pada kedua sisi grafik menunjukkan adanya perubahan ekspresi gen yang cukup besar. Titik-titik merah pada volcano plot mewakili gen yang mengalami peningkatan ekspresi pada prakanker serviks, sedangkan titik biru mewakili gen yang mengalami penurunan ekspresi pada prakanker serviks, serta titik abu-abu mewakili gen yang tidak berbeda secara signifikan. Pada *Mean-difference plot* semakim curam kemiringan garis yang menghubungan suatu gen dengan titik asal menunjukkan adanya perbedaan ekspresi antara sampel kontrol dan penderita prakanker serviks. Selain itu, hasil visualisasi diagram *venn* (Gambar 4c) memperlihatkan bahwa sebanyak 8163 gen berperan aktif terhadap prakanker serviks dan memenuhi kriteria tertentu (log2FC >0 dan Padj. <0,5).  



|**a.** |![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.004.jpeg)|**b.** |![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.005.jpeg)|
| - | - | - | - |
|||||
**c. ![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.006.png)**

Gambar 4. Visualisasi hasil GEO2R terhadap perbandingan pasien kontrol dan penderita 

prakanker  serviks  a.  *Volcano  Plot*;  b.  Diagram  *Mean-difference  plot*;  c. Diagram *Venn* 

Hasil visualisasi 50 DEGs teratas pada dataset GSE63514 ditampilkan dalam bentuk heatmap (Gambar 5). Terlihat warna merah yang menujukkan tingkat ekspresi gen yang tinggi (*up-regulated*) dan warna biru menunjukkan tingkat ekspresi gen yang rendah (*down-regulated*). Dari hasil klasterisasai heatmap memperlihatkan adanya pemisahan pola ekspresi gen antara kelompok normal dan prakanker seviks, dengan sebagian besar sampel  gen  masing-masing  kelompok  terlihak  membentuk  kelompok  bersama. Visualisasi  ini menunjukkan bahwa perubahan  regulasi gen telah terjadi  pada tahap prakanker serviks. Selain itu, terlihat juga adanya kelompok gen yang memiliki pola ekspresi yang tampak serupa di sisi kiri gambar. Gen-gen ini kemungkinan memiliki peran jalur biologis atau proses seluler yang sama. Adanya perbedaan pola ekspresi gen yang jelas dapat mengindikasikan bahwa gen tersebut dapat menjadi biomarker molekuler untuk deteksi dini prakanker serviks.  

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.007.jpeg)

Gambar 5. Heatmap dari 50 DEGs teratas Dataset GSE63514 normal serviks vs prakanker 

serviks* 

Gambar 6 memperlihatkan grafik dari hasil analisis *enrichment gene ontology* (GO) kategori biologi proses dari DEG. Sumbu X (count) pada grafik menunjukkan gumlah gen yang terlibat dalam proses biologis, warna grafik menunjukkan tingkat nilai p. adjust, dan warna merah menunjukkan tingkat signifikansi yang sangat tinggi. Dari hasil analisis menunjukkan  bahwa  sebagian  besar  DEG  yang  di  *enrichment*  berkaitan  dengan pembelahan dan siklus sel terlihat dari proses biologis diantaranya *DNA replication, mitotic nuclear division, nuclear division,* dan *chromosome segregation*. Dimana masing- masing proses biologis tersebut memiliki jumlah gen yang tinggi dan signifikan. Selain itu juga terlihat ada proses biologi seperti transisi fase siklus sel dan regulasi siklus sel. Dimana  proses  biologis  yang  berkaitan  dengan  pengaturan  dalam  proliferasi  sel menunjukkan bahwa tahap awal kanker terjadi peningkatan aktivitas replikasi DNA dan pembelahan sel.  

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.008.jpeg)

Gambar 6. *Gen Ontology* (GO) *Enrichment* dari sampel normal dan prakanker serviks 

menggunakan dataset *GSE63514* 

Gambar 7 memperlihatkan grafik dari hasil analisis *enrichment KEGG Pathway* dari DEG yang mengalami perubahan ekspresi pada prakanker serviks. Sumbu x (count) pada grafik  menunjukkan  gumlah  gen  yang  terlibat  dalam  proses  biologis,  warna  grafik menunjukkan tingkat nilai p. adjust, dan warna merah menunjukkan tingkat signifikansi yang sangat tinggi. Berdasarkan hasil analisis menunjukkan bahwa jalur yang paling banyak di*enrichment* adalah *cell cycle*, *cellular senescence*, *DNA replication,* dan *P5E signaling  pathway*.  Dimana  jalur  ini  berkaitan  erat  dengan  proses  pembelahan  sel, proliferasi sel, perbaikan DNA, respon saat terjadi kerusakan gen, dan pengaturan siklus sel. Selain itu, terlihat juga beberapa jalur lain seperti *base excision repair* dan *mismatch repair*. Dimana jalur ini berkaitan erat dalam mekanisme perbaikan DNA. Dari hasil visualisasi ini menunjukkan bahwa ekspresi gen pada prakanker serviks berkaitan erat dengan  regulasi  perbaikan  DNA,  replikasi  DNA,  dan  siklus  sel,  dimana  ketiganya merupakan proses penting dalam perkembangan kanker stadium awal. 

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.009.jpeg)

Gambar  7.  *KEGG  Pathway  Enrichment*  dari  sampel  normal  dan  prakanker  serviks 

menggunakan dataset *GSE63514* 

Gambar 8 memperlihatkan visualisasi jalur *pathway in cancer* dari hasil analisis KEGG pathway dari DEG antara jaringan epitel serviks normal dan prakanker serviks dari dataset *GSE 63514* menggunakan ShinyGo 0.85. Berdasarkan hasil visualisasi peta terlihat adanya kotak berwarna merah yang mengindikasikan adanya gen yang mengalami perubahan ekspresi yang signifikan pada prakanker serviks. Dimana sebagian besar gen yang mengalami perubahan ekspresi terlibat dalam jalur yang berkaitan dengan apoptosis, perbaikan DNA, proliferasi sel, dan regulasi siklus sel. Beberapa jalur sinyal seperti *cell cycle checkpoint, DNA damage response, MAPK signaling,* dan *p53 signaling* tampak aktif.  Aktifnya  jalur  ini  berkaitan  erat  dengan  penyebab  dari  adanya  peningkatan pembelahan sel  yang tidak terkontrol dan berkurangnya proses perbaikan kerusakan DNA.  Lalu  adanya  aktivasi  jalur  apoptosis  menunjukkan  bahwa  adanya  perubahan mekanisme kematian sel terpogram sehingga sel abnormal yang seharusnya dieliminasi tetap bertahap dan berkembang sehingga menyebabkan kanker serviks tahap lanjut. Dari KEGG  pathway  ini  memperkuat  hasil  *enrichment*  KEGG  bahwa  proses  siklus  sel, perbaikan  dan  replikasi  DNA  merupakan  proses  biologi  utama  perkembangan  lesi prakanker serviks menjadi kanker serviks. 

![](Aspose.Words.4ec2db01-55ac-42c0-88d5-f3fcc96a5cfc.010.jpeg)

Gambar 8. Visualisasi jalur *Pathways in cancer* berdasarkan analisis KEGG *pathway* dari 

gen yang diekspresikan secara berbeda pada jaringan serviks normal dan prakanker serviks (dataset GSE63514) 

**KESIMPULAN** 

Hasil analisis DEGs pada dataset GSE63514 didapatkan total DEGs sebanyak 1458 gen,  dengan  428  gen  *upregulation*  dan  1030  gen  *downregulation*.  Hasil  visualisasi *volcano plot, mean-difference plot,* dan *heatmap* menunjukkan adanya perbedaan pola ekspresi gen yang jelas antara kedua kelompok sampel. Analisis *Gene Ontology* (GO) dan *KEGG pathway* menunjukkan bahwa gen-gen tersebut terutama terlibat dalam proses siklus sel, replikasi DNA, pembelahan sel, serta mekanisme perbaikan DNA. Secara keseluruhan, hasil ini menunjukkan bahwa perubahan regulasi gen pada tahap prakanker serviks berkaitan dengan peningkatan proliferasi sel dan gangguan mekanisme kontrol siklus sel yang berperan dalam perkembangan awal kanker serviks. 

**DAFTAR PUSTAKA** 

den Boon, J. A., Dohun, P., Sophia, S. W., Mark, H., Mark, S., Mark, S., Rosemary, E. 

Z., Zhishi, W., Stephen, M. H., Rachel, P., Meghan, S., Lisa, C., Qiuling, H., Paul, L., Joan, W., Michael, A. N., Nicolas, W., Paul, A. (2015). Molecular transitions from papillomavirus infection to cervical precancer and cancer: Role of stromal estrogen  receptor  signaling.  *The  Proceedings  of  the  National  Academy  of Sciences*, 112(25). Doi: 10.1073/pnas.1509322112. 

Globocan.  (2022).  Cancer  Today  Indonesia.  *World  Health  Organization*. 

[https://gco.iarc.who.int/media/globocan/factsheets/populations/360-indonesia- fact-sheet.pdf.](https://gco.iarc.who.int/media/globocan/factsheets/populations/360-indonesia-fact-sheet.pdf) 

Karimah, R., Endah, I., Dwinka, S. E., Fira, S., Fatimah, N. F., Muhammad, N. H., Rizka, 

N. H., Desiana, W. S., Rahmah, Y. R., Lely, N., Zain, B. S., & Sonny, F. (2025). peningkatan  deteksi  dini  kanker  serviks  melalui  skrining  HPV  DNA  kepada masyarakat di Institut Teknologi Sepuluh Nopember. *Jurnal Pengabdian Kepada Masyarakat*, 9(6), 1637-1646. Doi: 10.12962/j26139960.v9i6.9141. 

Mayasari, S. P. (2025). Komparasi efikasi skrining kanker serviks menggunakan HPV 

DNA  testing,  pap  smear,  dan  liquid  biopsy:  Tinjauan  Sistematis.  *Indonesian* 

*Journal of Health Community*, 6(1), 33-41. Doi: 10.31331/ijheco.v6i1.3893. \
Mello, V., & Renee, K. S. (2023). Neoplasia Intraepitel Serviks. StatPearls Publishing. 

[https://www.ncbi.nlm.nih.gov/books/NBK544371/.](https://www.ncbi.nlm.nih.gov/books/NBK544371/) 

Shemuel, J., Priscilla, A., Evelina, J., Daniel, R. F., Vania, G., Shaheer, A., & Arli, A. P. 

(2023).  Analisis  gen  komparatif  karsinoma  sel  skuamosa  paru-paru  antara individu  merokok  dan  tidak  merokok.  *Berita  Biologi*,  22(3).,  291-304.  Doi: 10.14203/beritabiologi.v20i1.3991. 

Waghe,  T.,  &  Neema,  A.  (2024).  Advancements  in  the  management  of  cervical 

intraepithelial  neoplasia:  a  comprehensive  review.  *Cureus*,  16(4),  1-11.  Doi: 10.7759/cureus.58645. 

Yo, E. C., & Kartika, H. N. (2023). Molecular and host lifestyle factors associated with 

persistent human Papillomavirus infection and progression into cervical cancer: a literature  review. *Indonesian  Journal  of  Cancer*,  18(2),  227–233.  Doi: 10.33371/ijoc.v18i2.1068. 
