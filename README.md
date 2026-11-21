# Tugas Besar Analitika Perkotaan — Tipologi 17 Kapanewon Kabupaten Sleman

Analisis klasterisasi demografi dan ketersediaan fasilitas pendidikan pada 17 kapanewon di Kabupaten Sleman (data BPS Kabupaten Sleman & Kemendikbud, tahun 2021) menggunakan **K-Means**, **Hierarchical Clustering (Ward)**, dan **PCA**.

## Struktur Folder

```text
tugas-besar-analitika-perkotaan/
├── data/
│   ├── raw/                                # Data mentah asli (jangan diubah)
│   │   ├── Query Builder Result ... 20.17.54 WIB.xlsx   (Sekolah & desa berfasilitas sekolah)
│   │   ├── Query Builder Result ... 20.20.19 WIB.xlsx   (Penduduk & kepadatan per kapanewon)
│   │   ├── Sleman.geojson                               (Batas luar Kabupaten Sleman — GADM)
│   │   ├── sleman_kecamatan.geojson                     (Batas 17 kapanewon / 86 kalurahan — HDX-BPS 2020)
│   │   ├── 1.01.003-jumlah-sekolah-kabupaten-sleman-tahun-2024-2025.{xlsx,csv}
│   │   └── 10.02.001-penduduk-kabupaten-sleman-tahun-2019-2025.xlsx
│   └── processed/                          # Data bersih & tabel hasil klastering
│       ├── dataset_kapanewon_2021.csv
│       ├── hasil_klaster_kapanewon.csv
│       └── ringkasan_profil_klaster.csv
├── notebooks/                              # Pengolahan data & analisis utama
│   └── analisis_klaster_kapanewon_sleman.ipynb
├── output/
│   └── figures/                            # Visualisasi PNG resolusi tinggi (300 DPI)
│       ├── 01_korelasi_fitur.png
│       ├── 02_evaluasi_jumlah_klaster.png
│       ├── 03_dendrogram_hierarki.png
│       ├── 04_peringkat_kepadatan_dan_sekolah.png
│       ├── 05_pca_biplot_klaster.png
│       ├── 06_profil_klaster_radar_dan_bar.png
│       ├── 07_kuadran_pertumbuhan_vs_layanan.png
│       └── 08_peta_choropleth_sleman.png
└── README.md
```

## Cara Menjalankan Ulang

1. Aktifkan environment conda:
   ```powershell
   conda activate analitika-perkotaan
   ```
2. Buka [analisis_klaster_kapanewon_sleman.ipynb](notebooks/analisis_klaster_kapanewon_sleman.ipynb) di VS Code atau JupyterLab, pilih kernel `analitika-perkotaan`, lalu klik **Run All**.
