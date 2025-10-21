# 🚗 Car Sales Analysis Dashboard

## 📋 Deskripsi Proyek
Proyek ini merupakan analisis data penjualan mobil dari tahun ke tahun menggunakan **SQL, Python (pandas), dan Power BI**.  
Tujuannya adalah untuk memahami tren penjualan, performa brand dan model, serta market share dalam industri otomotif.

Dashboard ini menampilkan **kinerja penjualan 2001–2020**, dengan insight seperti:
- Total penjualan dan pertumbuhan tahunan (YoY Growth)
- Brand dan model terlaris
- Market share antar merek
- Tren penjualan dari waktu ke waktu

---

## 🗂️ Dataset
**Nama file:** `sales_clean.csv`

**Kolom penting:**
| Kolom | Deskripsi |
|--------|------------|
| `Year` | Tahun penjualan |
| `Brand` | Nama merek mobil |
| `Model` | Model mobil |
| `Sales` | Jumlah penjualan |
| `Country` | Negara asal merek (opsional) |

---

## ⚙️ Tools & Teknologi
- **SQL Server / MySQL** – untuk analisis dan query data
- **Python (pandas, matplotlib)** – untuk eksplorasi dan validasi data
- **Tableau** – untuk visualisasi interaktif
- **GitHub** – untuk dokumentasi proyek dan portofolio

---

## 🔍 Analisis Utama

### 1️⃣ Total Penjualan per Tahun
Mengetahui tren pertumbuhan atau penurunan penjualan dari tahun ke tahun.

```sql
SELECT 
    Year, 
    SUM(Sales) AS Total_Sales
FROM sales_clean
GROUP BY Year
ORDER BY Year;
