# Capstone-Project-Final-Project-Project-Based-Learning-Bioinformatics

# LAPORAN ANALISIS TRANSKRIPTOMIK
# IDENTIFIKASI GEN YANG DIEKSPRESIKAN SECARA BERBEDA PADA KANKER SERVIKS
Dibuat oleh: Syarifah Tashara

# Pendahuluan
Kanker serviks merupakan salah satu jenis kanker dengan penyumbang kematian tertinggi pada wanita didunia. Menurut data Global Burden of Cancer Study (Globocan) dari World Health Organization (WHO) tahun 2022, sekitar 36.964 (16,8%) perempuan Indonesia terkena kanker serviks paling tinggi kedua setelah kanker payudara. Faktor utama penyebab kanker serviks yaitu akibat dari infeksi Human Papilloma Virus (HPV) yang ditularkan melalui kontak seksual (Karimah et al., 2025). Infeksi HPV umumnya berkembang secara bertahap dimana sel Normal Serviks akan berubah menjadi lesi pada sel intraepitel serviks hingga akhirnya menjadi kanker (Yo & Kartika, 2023). Lesi intraepitel serviks atau Cervical intraepithelial Neoplasia (PRAKANKER SERVIKS) merupakan perubahan abNormal Serviks awal pada sel epitel serviks sebelum menjadi kanker serviks (Waghe & Neema, 2024). Lesi prakanker ini terbagi menjadi tiga tingkat perubahan yang mengindikasikan tingkat keparahan sel, yaitu PRAKANKER SERVIKS1 (perubahan sel epitel serviks ringan), PRAKANKER SERVIKS2 (perubahan sel epitel serviks sedang), dan PRAKANKER SERVIKS3 (Perubahan sel epitel serviks berat) (den Boon et al., 2015). Tingkat lesi PRAKANKER SERVIKS ini sangat penting untuk mendeteksi perubahan sel serviks secara dini dan menghentikan lesi agar tidak meluas dan berkembang menjadi kanker serviks. Beberapa metode telah dikembangkan saat ini untuk mengidentifikasi tingkat PRAKANKER SERVIKS diantaranya Pap smear dan tes HPV (Mayasari, 2025). Namun, beberapa kasus lesi PRAKANKER SERVIKS ini seringkali tidak menunjukkan adanya gejala tahap awal (Mello & Renee, 2023). Hal ini menyebabkan keterlambatan diagnosis yang menyebabkan penyakit ini berkembang menjadi kanker serviks tingkat lanjut. Perkembangan teknologi saat ini telah memungkinkan untuk mengindentifikasi perubahan ekspresi gen-gen yang berperan dalam perkembangan penyakit. Salah satu metode yang telah banyak digunakan yaitu transkriptomik yang dapat menganalisis Differentially Expressed Genes (DEGs) pada jaringan Normal Serviks hingga kanker (Shemuel et al., 2023). Melalui analisis ini, dapat diketahui juga gen-gen yang berperan dalam perkembangan lesi prakanker serviks sehingga dapat mendukung upaya deteksi dini serta pengobatan yang tepat. 
Tujuan analisis ini adalah untuk mengetahui hasil analisis Differentially Expressed Genes (DEGs) pada pasien dengan kondisi berbeda, yaitu antara jaringan serviks sehat sebagai Normal Serviks (Normal Serviks) dan jaringan prakanker serviks dengan tingkat lesi yang berbeda, yaitu Cervical Intraepithelial Neoplasia tingkat PRAKANKER SERVIKS1, PRAKANKER SERVIKS2, dan PRAKANKER SERVIKS3, serta melakukan visualisasi dan interpretasi data ekspresi gen untuk memahami perubahan gen yang berperan dalam perkembangan lesi prakanker serviks.

# Metode
# Analisis Menggunakan GEO2R
**1.	Pencarian dan Pengunduhan Dataset Ekspresi Gen Publik Kanker Serviks**
Dataset yang digunakan yaitu GSE63514 Homo sapiens yang diambil dari database Gene Expression Omnibus (GEO) (https://www.ncbi.nlm.nih.gov/geo/). Dataset ini dipilih karena berisi data mengenai ekspresi gen pada sel epitel serviks normal, sel epitel prakanker serviks meliputi CIN1, CIN2, dan CIN3, hingga sel epitel kanker serviks. 

**2.	Identifikasi Differentially Expressed Genes (DEGs) Pada Kanker Serviks**
Identifikasi menggunakan alat analisis online GEO2R (https://www.ncbi.nlm.nih.gov/geo/geo2r). GEO2R digunakan untuk mengidentifikasi gen-gen yang dieskpresikan secara berbeda berdasarkan kondisi biologis atau perlakuan. Dalam analisis ini yaitu mengidentifikasi ekspresi gen yang berbeda pada sampel sel epitel serviks sehat atau normal sebanyak 24 sampel, serta sel epitel dengan tingkat lesi prakanker serviks yang berbeda diantaranya CIN1 sebanyak 14 sampel, CIN2 sebanyak 22 sampel, dan CIN 3 sebanyak 40 sampel.
Sampel dilakukan pengelompokkan yaitu Group 1 = sel epitel serviks pasien sehat (Kontrol) dan Group 2 = sel epitel pasien dengan lesi prakanker serviks CIN1, CIN2, CIN3 (penderita prakanker serviks) yang berbeda. Koreksi multiple testing menggunakan metode Benjamini & Hochberg (False Discovery Rate). Metode Benjamini & Hochberg (FDR) digunakan untuk mengurangi kemungkinan kesalahan tipe I akibat dari pengujian ribuan gen secara bersamaan. Perhitungan differential expression menggunakan metode limma. Gen dikategorikan sebagai DEGs apabila memenuhi kriteria:  Adjusted p-value < 0,05 dan |log2 fold change| ≥ 0 tertera pada Gambar 3. Untuk memastikan konsistensi hasil, analisis GEO2R dilakukan sebanyak tiga kali replikasi dengan parameter dan alur yang sama.

**3.	Analisis Visualisasi Differentially Expressed Genes (DEGs) Pada Kanker Serviks**
Analisis DEG divisualisasikan menggunakan empat visual diantaranya Volcano Plot, diagram Mean-difference plot, diagram Venn, dan Heatmap. Empat visualisasi ini untuk memudahkan menginterpretasi data. Volcano plot untuk melihat hasil distribusi gen yang mengalami peningkatan (up-regulation) dan penurunan (down-regulation) secara signifikan. Diagram Mean-difference plot digunakan untuk melihat hubungan antara rata-rata ekpresi gen dan perubahan ekspresi gen antar kelompok sampel. Diagram Venn digunakan untuk melihat adanya kesamaan gen yang signifikan antar kelompok data sampel. Heatmap digunakan untuk menampilkan pola ekspresi gen pada setiap kelompok sampel.

**4. Analisis Enrichment Gene Ontology (GO) dan KEGG**
Gen yang signifikan kemudian dilakukan analisis Enrichment Gene Ontology (GO) dan Kyoto Encyclopedia of Genes and Genomes (KEGG) yang tujuannya untuk mengetahui fungsi biologis gen tersebut. Analisis ini mengelompokkan gen berdasarkan proses biologis, fungsi molekuler, dan komponen selulernya. Analisis GO dan KEGG menggunakan bahasa pemrograman R dengan metode enrichment analysis untuk identifikasi kategori GO dan KEGG yang signifikan dari gen-gen yang telah diperoleh.

**5. Analisis Jalur Biologis (KEGG Pathway Analysis)**
Gen yang terlah dianalisis Enrichment selanjutnya dianalisis jalur biologisnya menggunakan KEGG Pathway analysis. Tujuan analisis ini yaitu untuk mengetahui peta jalur tentang interaksi jaringan, reaksi, dan hubungan mekanisme molekuler yang terlibat dalam penyakit tersebut. Analisis KEGG pathway menggunakan platform ShinyGO versi 0.85. 

# 6. Analisis Menggunakan Perangkat R
**6.1 Persiapan Perangkat Lunak dan Pengolahan Data**
a. Terlebih dahulu mengunduh dan menginstal perangkat lunak R for Window (versi 4.5.2) di (https://cran.r-project.org/) dan Rstudio Dekstop (versi 2026.01.1+403) di (: https://posit.co/download/rstudio-desktop/). 
b. Setelah itu, menginstal manager paket Bioconductor yaitu BiocManager. Dengan menggunakan script tertera:
if (!require("BiocManager", quietly = TRUE))
install.packages("BiocManager") 
BiocManager::install(version = "3.22")
BiocManager::install("hgu133a.db")
c. BiocManager yang digunakan dalam analisis ini yaitu GEOquery dan limma. Dengan menggunakan script tertera:
BiocManager::install(c("GEOquery", "limma"), ask = FALSE, update = FALSE) 
d. Selanjutnya menginstal dplyr untuk memotong dan merapikan tabel data agar mudah diolah. Dengan menggunakan script tertera:
install.packages("dplyr")
e. Setelah itu menginstal paket CRAN untuk visualisasi meliputi ggplot (Volcano Plot), pheatmap (Heatmap), gplots & RcolorBrewer (Diagram Venn dan palet warna), dan UMAP. Dengan menggunakan script tertera:
install.packages(c("ggplot2", "pheatmap", "gplots", "RColorBrewer"))
f. Tahap terakhir cek instalasi. Dengan menggunakan script tertera:
library(GEOquery)
library(limma)
library(dplyr)
library(ggplot2)
library(pheatmap)
library(gplots)
library(RColorBrewer)
library(hgu133a.db)
library(AnnotationDbi)

**2.4. Pengambilan Data dari GEO**
Proses analisis DEG dengan dataset GSE63514 menggunakan script tertera:
library(GEOquery)
gset <- getGEO("GSE63514", GSEMatrix = TRUE, AnnotGPL = TRUE)[[1]]
expr_matrix <- exprs(gset)
sample_info <- pData(gset)
feature_info <- fData(gset)

**2.5. Pre-Processing Data Ekspresi**
Proses pre-processing dilakukan untuk memastikan bahwa data ekspresi gen sesuai sebelum dianalisis DEG. Proses pre-processing menggunakan script tertera:
Mengambil matriks ekspresi menggunakan script tertera:
ex <- exprs(gset)
Menghitung distribusi nilai kuantil menggunakan script tertera:
qx <- as.numeric(quantile(ex, 
c(0, 0.25, 0.5, 0.75, 0.99, 1), 
na.rm = TRUE))
Menentukan apakah perlu transform log2 menggunakan script tertera:
LogTransform <- (qx[5] > 100) || 
(qx[6] - qx[1] > 50 && qx[2] > 0)
Melakukan transformasi log2 jika diperlukan menggunakan script tertera:
if (LogTransform) {
ex[ex <= 0] <- NA
ex <- log2(ex)
}

**2.6. Definisi Kelompok Sampel**
Proses definisi kelompok sampel dilakukan untu mengekompokkan sampel yang terdapat pada dataset GSE63514 berdasarkan kondisi biologis.
Melihat metadata sampel menggunakan script tertera:
sample_info <- pData(gset)
group_info <- sample_info$source_name_ch1
Melakukan grouping pada sampel menggunakan script tertera:
groups <- ifelse(
grepl("normal", group_info, ignore.case = TRUE), "Normal_Serviks",
ifelse(grepl("low grade|moderate grade|high grade", group_info, ignore.case = TRUE),
"Prakanker_Serviks", NA)
)
groups <- factor(groups)
table(groups)
Menghilangkan kelompok sampel kanker serviks menggunakan script tertera:
keep <- !is.na(groups)
gset <- gset[, keep]
groups <- groups[keep]
Melakukan pengecekan ulang menggunakan script tertera:
table(groups)
dim(exprs(gset))

**2.7. Design Matrix (Kerangka Statistik)**
Membuat design matrix tanpa intercept menggunakan script tertera:
design <- model.matrix(~0 + gset$group)
colnames(design) <- levels(gset$group)
design
Menentukan perbandingan biologi yang akan dianalisis menggunakan script tertera:
contrast.matrix <- makeContrasts(
Prakanker_vs_Normal = Prakanker_Serviks - Normal_Serviks,
levels = design
)

**2.8. Analisis Differentially Expressed Gene (DEG) dengan Limma**
Analisis DEG dilakukaan menggunakan paket linear model linear dan metode Empirical Bayes. menggunakan script tertera:
fit <- lmFit(exprs(gset), design)
fit2 <- contrasts.fit(fit, contrast.matrix)
fit2 <- eBayes(fit2)
deg <- topTable(fit2,
fit2,
coef="Prakanker_vs_Normal",
number=Inf,
adjust.method="BH"
)
head(deg)
Melakukan filter gen signifikan
deg_filtered <- deg[deg$adj.P.Val < 0.05 & abs(deg$logFC) >= 1, ]
Mengecek jumlah gen signifikan 
nrow(deg_filtered)

**2.9. Anotasi Nama Gen**
Mengecek anotasi bawaan GEO menggunakan script tertera:
head(fData(gset))
colnames(fData(gset))
Mengambil informasi anotasi gen bawaan dari GEO menggunakan script tertera:
feature_info <- fData(gset)
Menyalin hasil DEG menggunakan script tertera:
topTableResults <- deg
Menambahkan ID gen (rownames) sebagai kolom menggunakan script tertera:
topTableResults$ID <- rownames(topTableResults)
Memberi ID sebegai simbol gen (apabila tidak ada gen simbol) menggunakan script tertera:
topTableResults$SYMBOL <- topTableResults$ID
Menambahkan deskripsi gen dari GEO menggunakan script tertera:
topTableResults$SYMBOL <- feature_info[
match(topTableResults$ID, feature_info$ID),
"Gene symbol"
]
topTableResults$GENENAME <- feature_info[
match(topTableResults$ID, feature_info$ID),
"Gene title "
]
Memeriksa hasil anotasi menggunakan script tertera:
head(topTableResults[, c("ID","SYMBOL","GENENAME")])

**2.9. Visualisasi Volcano Plot**
Menyiapkan data untuk volcano plot menggunakan script tertera:
volcano_data <- data.frame(
logFC = topTableResults$logFC,
adj.P.Val = topTableResults$adj.P.Val,
Gene = topTableResults$SYMBOL
)
Mengklasifikasikan status gen menggunakan script tertera:
volcano_data$status <- "NO"
volcano_data$status[
volcano_data$logFC > 1 & 
volcano_data$adj.P.Val < 0.05
] <- "UP"
volcano_data$status[
volcano_data$logFC < -1 & 
volcano_data$adj.P.Val < 0.05
] <- "DOWN"
Membuat Volcano Plot menggunakan script tertera:
ggplot(volcano_data, 
       aes(x = logFC, 
           y = -log10(adj.P.Val), 
           color = status)) +
  geom_point(alpha = 0.6) +
  scale_color_manual(values = c("DOWN" = "blue",
                                "NO" = "black",
                                "UP" = "red")) +
  geom_vline(xintercept = c(-1, 1), linetype = "dashed") +
  geom_hline(yintercept = -log10(0.05), linetype = "dashed") +
  theme_minimal() +
  ggtitle("Volcano Plot DEGs Prakanker_vs_Normal (GSE63514)")

**2.10. Visualisasi Heatmap**
Mengambil top 50 DEG terlebih dahulu (apabila hasil tidak ada gen tersisa) menggunakan script tertera:
top50 <- deg_filtered[order(deg_filtered$adj.P.Val), ][1:50, ]
Mengambil ekspresi dari gset (menggunakan ID gen sebagai rownames) menggunakan script tertera:
mat_heatmap <- exprs(gset)[rownames(top50), ]
Menghapus NA (wajib sebelum heatmap) menggunakan script tertera:
mat_heatmap <- mat_heatmap[complete.cases(mat_heatmap), ]
Membuang gen tanpa variasi menggunakan script tertera:
mat_heatmap <- mat_heatmap[
apply(mat_heatmap, 1, sd, na.rm = TRUE) > 0,
]
Melakukan pengencekan jumlah gen kembali menggunakan script tertera:
dim(mat_heatmap)
Membuat annotation sampel menggunakan script tertera:
annotation_col <- data.frame(
Group = groups
)
rownames(annotation_col) <- colnames(mat_heatmap)
dim(annotation_col)
Menjalankan heatmap menggunakan script tertera:
pheatmap(
    mat_heatmap,
    scale = "row",
    annotation_col = annotation_col,
    show_colnames = FALSE,
    show_rownames = TRUE,
    fontsize_row = 7,
    clustering_distance_rows = "euclidean",
    clustering_distance_cols = "euclidean",
    clustering_method = "complete",
    main = "Top 50 DEGs Prakanker Serviks vs Normal Serviks (GSE63514)"
)


**2.11. Analisis Enrichment Gene Ontology (GO) dan KEGG Pathway**
a. Menginstal dan load package menggunakan script tertera:
if (!require("BiocManager", quietly = TRUE))
install.packages("BiocManager")
BiocManager::install(c(
"clusterProfiler",
"org.Hs.eg.db",
"AnnotationDbi"
), ask = FALSE, update = FALSE)
install.packages("ggplot2")
b. Meload library menggunakan script tertera:
library(clusterProfiler)
library(org.Hs.eg.db)
library(AnnotationDbi)
library(ggplot2)
c. Memastikan platform dataset menggunakan script tertera:
annotation(gset)
d. Mengambil data DEG signifikan menggunakan script tertera:
deg_sig <- topTableResults[
  abs(topTableResults$logFC) >= 1 &
  topTableResults$adj.P.Val < 0.05,
]
nrow(deg_sig)
e. Melakukan pembersihan nama gen menggunakan script tertera:
symbol_clean <- deg_sig$GENENAME
symbol_clean <- gsub("\\s*\\[.*\\]", "", symbol_clean)
symbol_clean <- trimws(symbol_clean)
symbol_clean <- symbol_clean[symbol_clean != ""]
symbol_clean <- symbol_clean[!grepl(
"novel|query|LOC|ENSG|uncharacterized",
symbol_clean,
ignore.case = TRUE
)]
symbol_clean <- unique(symbol_clean)
length(symbol_clean)
head(symbol_clean)
f. Melakukan convert GENENAME menjadi ENTREZID menggunakan script tertera:
gene_df <- bitr(symbol_clean,
                fromType = "GENENAME",
                toType   = c("SYMBOL","ENTREZID"),
                OrgDb    = org.Hs.eg.db)
head(gene_df)
nrow(gene_df)
g. Melakukan GO Enrichment (Biological process) menggunakan script tertera:
ego <- enrichGO(
  gene          = gene_df$ENTREZID,
  OrgDb         = org.Hs.eg.db,
  ont           = "BP",
  pAdjustMethod = "BH",
  pvalueCutoff  = 0.05,
  readable      = TRUE
)
head(ego)
h. Membuat Grafik Gene Ontology (GO) menggunakan script tertera:
dotplot(ego, showCategory = 15) +
  ggtitle("GO Biological Process")
barplot(ego, showCategory = 15)
  ggtitle("GO Biological Process")

i. Membuat Grafik KEGG Pathway menggunakan script tertera:
ekegg <- enrichKEGG(
  gene         = gene_df$ENTREZID,
  organism     = "hsa",
  pvalueCutoff = 0.05
)
head(ekegg)
dotplot(ekegg, showCategory = 15) +
ggtitle("KEGG Pathway Enrichment")
barplot(ekegg, showCategory = 15)
ggtitle("KEGG Pathway Enrichment")

**2.12. Menyimpan Hasil**
Menyimpan seluruh worskpace (backup) menggunakan script tertera:
save.image("backup.RData")
Menghapus objek besar yang sudah tidak dipakai menggunakan script tertera:
rm(fit, fit2)
gc()
Menyimpan hasil analisis ke file csv menggunakan menggunakan script tertera:
write.csv(topTableResults,
"Hasil_GSE63514_DEG.csv",
row.names = FALSE)
Analisis selesai menggunakan script tertera:
message("Analisis selesai. File hasil telah disimpan.")


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
