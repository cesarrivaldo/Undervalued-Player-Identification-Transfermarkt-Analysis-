# Identifikasi Pemain Berpengalaman yang Undervalued di 5 Liga Top Eropa

## Outline
Analisis data untuk membantu klub papan tengah menemukan pemain berpengalaman (usia 28+) yang harganya terdiskon namun masih produktif, sebagai dasar pengambilan keputusan rekrutmen berbasis data.
```
1. P0M1_cesar_rivaldo.ipynb - Notebook yang berisi pengolahan data dengan python.

2. P0M1_cesar_rivaldo_dataset.csv - Data yang sudah clean 
```
### Problem Background

Klub Papan tengah tidak bisa bersaing budget dengan klub elit, sehingga strategi rekrutmen harus efisien. Market value di Transfermarkt cendrung bias ke usia muda. Pemain 28 tahun ke atas sering mengalami penurunan value meski output di lapangan masih stabil. Proyek ini memetakan celah tersebut menggunakan data, bukan feeling. mencari pemain berpengalaman yang harganya turun faktor usia, bukan karena performanya menurun. 

### Problem Statement 
Sebagai Sport Director klub papan tengah dengan budget transfer terbatas,
mengidentifikasi 10-15 pemain berpengalaman (usia >= 28 tahun) di 5 liga top Eropa
yang undervalued — yaitu memiliki rasio performa-terhadap-market-value terbaik — untuk
dijadikan shortlist rekrutmen, berdasarkan data Transfermarkt terbaru.

Disusun dengan metode SMART:
- **Specific**: pemain 28+ yang undervalued di 5 liga top.
- **Measurable**: shortlist 10-15 nama; "undervalued" diukur via rasio (gol+assist)/value.
- **Achievable**: data publik gratis, scope 5 liga & 4 tabel, tools Python + Tableau.
- **Relevant**: menjawab kebutuhan klub budget terbatas.
- **Time-bound**: memakai snapshot Transfermarkt terbaru, performa musim terkini.`

## Penjabaran Masalah
Visualisasi:
1. Bagaimana pola market value terhadap usia pemain?
2. Di liga dan posisi mana value rata-rata paling murah?
3. Apakah pemain di kelompok harga murah tetap punya kontribusi tinggi?
4. Siapa top 15 pemain berpengalaman paling undervalued?

Statistik Deskriptif:

5. Bagaimana sebaran market value pemain berpengalaman?

Statistik Inferensial:

6. Apakah pemain >= 28 tahun dihargai signifikan lebih murah dibanding pemain < 28?

## Dataset
- **Sumber**: [Football Data from Transfermarkt](https://www.kaggle.com/datasets/davidcariboo/player-scores) (Kaggle, oleh davidcariboo)
- **Asal data**: Transfermarkt, di-scrape dan dikurasi otomatis (update mingguan)
- **Tabel yang dipakai**: `players`, `player_valuations`, `appearances`, `competitions`
- **Cakupan**: pemain aktif di 5 liga top Eropa (Premier League, LaLiga, Bundesliga,
  Serie A, Ligue 1)

Data mentah diproses menjadi satu tabel siap analisis (`P0M1_cesar_rivaldo_dataset.csv`) berisi
satu baris per pemain, lengkap dengan umur, performa 2 musim terakhir, market value, dan
rasio value-for-money.


## Stacks
- **Python**: pandas, numpy, matplotlib, scipy
- **Tableau Public**: dashboard visualisasi & analisis
- **Jupyter Notebook**

## Reference
Dashboard Tableau : https://public.tableau.com/app/profile/cesar.rivaldo/viz/UndervaluedPlayers/Dashboard1?publish=yes

---
