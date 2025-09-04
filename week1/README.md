# 📘 Physically Based Animation – Week 1 Notes
### Topik: Kinematics (Gerak Lurus)

---

## 1. Kenapa Fisika Penting di Animasi?
- **Animasi berbasis fisika** = gunakan hukum fisika untuk menghasilkan simulasi realistis.
- Bisa **real-time** (game) atau **pre-rendered** (film CGI).
- Animasi komputer bekerja dengan **frame per second (fps)** → 30 fps artinya 30 gambar per detik.

---

## 2. Konsep Dasar Kinematika
- **Kinematika**: mempelajari gerak benda tanpa memperhatikan gaya penyebabnya.  
- Fokus: **posisi (s)**, **kecepatan (v)**, dan **percepatan (a)**.  
- Anggap benda sebagai **partikel**.

### Perbedaan Penting
| Konsep      | Jenis    | Rumus Dasar                     | Keterangan |
|-------------|----------|---------------------------------|------------|
| Speed       | Skalar   | `speed = jarak / waktu`         | Tidak ada arah |
| Velocity    | Vektor   | `velocity = perpindahan / waktu`| Ada arah |
| Distance    | Skalar   | Panjang lintasan                | Bisa berliku |
| Displacement| Vektor   | Posisi akhir – awal             | Bisa 0 meski jarak ≠ 0 |

---

## 3. Lambang & Notasi Penting
| Simbol | Arti                          | Satuan SI   |
|--------|-------------------------------|-------------|
| `s`    | Posisi / Perpindahan          | meter (m)   |
| `d`    | Jarak (Distance)              | meter (m)   |
| `v`    | Kecepatan (Velocity, vektor)  | m/s         |
| `v_avg`| Kecepatan rata-rata           | m/s         |
| `v0`   | Kecepatan awal                | m/s         |
| `vt`   | Kecepatan saat t              | m/s         |
| `a`    | Percepatan (Acceleration)     | m/s²        |
| `t`    | Waktu                         | sekon (s)   |
| `Δt`   | Selang waktu                  | sekon (s)   |

---

## 3b. Contoh Penerapan Lambang

**1) Simbol $s$ (posisi / perpindahan)**  
Rumus:

$$
s = v \cdot t
$$

Contoh: Jika $v=10 \,\mathrm{m/s}$ dan $t=5 \,\mathrm{s}$, maka

$$
s = 10 \cdot 5 = 50 \,\mathrm{m}
$$

---

**2) Simbol $d$ (jarak / distance)**  
Rumus:

$$
d = v \cdot t
$$

Contoh: Sepeda dengan $v=5 \,\mathrm{m/s}$, $t=60 \,\mathrm{s}$

$$
d = 5 \cdot 60 = 300 \,\mathrm{m}
$$

---

**3) Simbol $v$ (kecepatan / velocity)**  
Rumus:

$$
v = \frac{s}{t}
$$

Contoh: $s=150 \,\mathrm{m}$, $t=20 \,\mathrm{s}$

$$
v = \frac{150}{20} = 7.5 \,\mathrm{m/s}
$$

---

**4) Simbol $v_{avg}$ (kecepatan rata-rata)**  
Rumus:

$$
v_{avg} = \frac{\Delta s}{\Delta t}
$$

Contoh: Perjalanan $100 \,\mathrm{km}$ dalam $2 \,\mathrm{jam}$

$$
v_{avg} = \frac{100}{2} = 50 \,\mathrm{km/h}
$$

---

**5) Simbol $v_0$ (kecepatan awal)**  
Rumus:

$$
v_t = v_0 + a \cdot t
$$

Contoh: $v_0=0$, $a=2 \,\mathrm{m/s^2}$, $t=5 \,\mathrm{s}$

$$
v_t = 0 + 2 \cdot 5 = 10 \,\mathrm{m/s}
$$

---

**6) Simbol $a$ (percepatan)**  
Rumus:

$$
a = \frac{\Delta v}{\Delta t}
$$

Contoh: $v$ naik dari $0$ ke $20 \,\mathrm{m/s}$ dalam $10 \,\mathrm{s}$

$$
a = \frac{20 - 0}{10} = 2 \,\mathrm{m/s^2}
$$

---

**7) Simbol $t$ (waktu)**  
Variabel waktu; misalnya $t=60 \,\mathrm{s}$ berarti 1 menit.

---

**8) Simbol $\Delta t$ (selang waktu)**  
Rumus:

$$
\Delta t = t_2 - t_1
$$

Contoh: $t_1=2 \,\mathrm{s}$, $t_2=5 \,\mathrm{s}$

$$
\Delta t = 5 - 2 = 3 \,\mathrm{s}
$$

---

## 4. Rumus Utama
- **Speed**:  
  $$
  \text{Speed} = \frac{\text{Distance}}{\text{Time}}
  $$

- **Velocity**:  
  $$
  \text{Velocity} = \frac{\text{Displacement}}{\text{Time}}
  $$

- **Average Speed** = Total Jarak ÷ Total Waktu  
- **Average Velocity** = Total Perpindahan ÷ Total Waktu  

---

## 5. Contoh Soal + Pembahasan

### Soal 1  
Mobil menempuh 150 m dalam 20 s. Hitung speed-nya.

**Langkah 1**: Tuliskan rumus  
$$
\text{Speed} = \frac{Distance}{Time}
$$

**Langkah 2**: Masukkan angka  
$$
\text{Speed} = \frac{150}{20}
$$

**Langkah 3**: Hitung  
$$
\text{Speed} = 7.5 \, m/s
$$

✅ Jawaban: **7.5 m/s**

---

### Soal 2  
Teman lari dengan kecepatan 2 m/s. Jarak ke Indomaret 20 m. Berapa waktu yang dibutuhkan?

**Langkah 1**: Rumus dasar  
$$
Time = \frac{Distance}{Speed}
$$

**Langkah 2**: Masukkan angka  
$$
Time = \frac{20}{2}
$$

**Langkah 3**: Hitung  
$$
Time = 10 \, s
$$

✅ Jawaban: **10 detik**

---

### Soal 3  
Bus berangkat dari Ubaya ke Jatim Park 2 (100 km). Berangkat pukul 08.30, tiba pukul 10.00. Hitung average speed dalam km/h.

**Langkah 1**: Cari total waktu  
08.30 → 10.00 = **1,5 jam**

**Langkah 2**: Rumus  
$$
\text{Speed} = \frac{Distance}{Time}
$$

**Langkah 3**: Masukkan angka  
$$
\text{Speed} = \frac{100}{1.5}
$$

**Langkah 4**: Hitung  
$$
\text{Speed} = 66.7 \, km/h
$$

✅ Jawaban: **≈ 66.7 km/h**

---

### Soal 4  
Trip A ↔ B (240 km).  
- A → B: 40 km/h  
- Istirahat: 2 jam  
- B → A: 60 km/h  

**Langkah 1**: Waktu A → B  
$$
t = \frac{240}{40} = 6 \, jam
$$

**Langkah 2**: Waktu B → A  
$$
t = \frac{240}{60} = 4 \, jam
$$

**Langkah 3**: Total jarak  
$$
240 + 240 = 480 \, km
$$

**Langkah 4**: Total waktu (termasuk istirahat)  
$$
6 + 2 + 4 = 12 \, jam
$$

**Langkah 5**: Average speed  
$$
\frac{480}{12} = 40 \, km/h
$$

**Langkah 6**: Average velocity  
Karena pulang ke titik awal, perpindahan = 0.  
$$
\text{Average velocity} = 0
$$

✅ Jawaban: **Speed = 40 km/h**, **Velocity = 0**

---

### Soal 5  
Balap sendok telur:  
- Pergi 25 m dalam 20 s  
- Balik 25 m dalam 15 s  

**Langkah 1**: Average velocity per segmen  
- Pergi:  
$$
\frac{25}{20} = 1.25 \, m/s
$$  
- Balik:  
$$
\frac{25}{15} \approx 1.67 \, m/s
$$

**Langkah 2**: Round trip displacement  
Posisi akhir kembali ke awal → **0 m**  
$$
\text{Average velocity round trip} = \frac{0}{35} = 0
$$

**Langkah 3**: Round trip speed  
$$
\text{Average speed} = \frac{50}{35} \approx 1.43 \, m/s
$$

✅ Jawaban:  
- Pergi: **1.25 m/s**  
- Balik: **1.67 m/s**  
- Average velocity round trip: **0**  
- Average speed round trip: **≈ 1.43 m/s**

---

## 6. Aplikasi di Game
- **Velocity** dipakai untuk menentukan arah & kecepatan objek bergerak.  
- Contoh implementasi:  
  ```csharp
  position = position + velocity * deltaTime;
  ```
