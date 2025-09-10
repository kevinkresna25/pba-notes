# 📘 Physically Based Animation – Week 2 Notes
### Topik: Kinematics (2) — GLBB & Gerak Jatuh Bebas

> Ringkasan materi berdasarkan slide Week 2 (Kinematics 2). 

---

## 1) Gambaran Umum
- **GLBB (Uniform Acceleration)**: gerak dengan percepatan konstan. Kecepatan bisa **bertambah** atau **berkurang** tergantung arah $a$ relatif terhadap $v$.
- **Inti penting**: "deceleration" di fisika **tetap disebut acceleration** (nilainya bisa negatif tergantung sumbu yang dipilih).
- **GJB (Freefall)**: gerak vertikal di bawah pengaruh gravitasi saja (abaikan hambatan udara). Nilai standar: $g \approx -9.81\,\mathrm{m/s^2}$ (ambil $-10\,\mathrm{m/s^2}$ untuk hitung cepat). Massa **tidak memengaruhi** percepatan jatuh bebas.

---

## 2) Konvensi Tanda (sangat penting)
Pilih arah **positif** sejak awal dan konsisten.
- Jika **atas positif**: $g = -9.81\,\mathrm{m/s^2}$ (atau $-10$). Lempar ke atas → $v$ awal positif, saat turun $v$ jadi negatif.
- Jika **bawah positif**: $g = +9.81\,\mathrm{m/s^2}$.
- **Cepat/lambat**:
  - $a$ **searah** $v$ → objek **mempercepat** (speed up).
  - $a$ **berlawanan** $v$ → objek **memperlambat** (slow down).

---

## 3) Rumus GLBB (percepatan konstan)
Dengan posisi $x$ (atau $s$), kecepatan $v$, percepatan $a$.

- Persamaan kecepatan:

$$
v = v_0 + a t
$$

- Persamaan posisi:

$$
x = x_0 + v_0 t + \tfrac{1}{2} a t^2
$$

- Hubungan $v$–$x$ (tanpa $t$):

$$
v^2 = v_0^2 + 2 a (x - x_0)
$$

- Kecepatan rata-rata (khusus $a$ konstan):

$$
v_{avg} = \tfrac{v_0 + v}{2}, \qquad x - x_0 = v_{avg} \; t
$$

> Tips: pilih persamaan sesuai data yang diketahui (punya $t$ atau tidak, tahu $v$ akhir atau tidak).

---

## 4) Jatuh Bebas (Freefall)
Gunakan persamaan GLBB dengan $a = g$.

- Dari ketinggian $h$ dan dilepas (v_0 = 0) ke bawah:

$$
y = y_0 + v_0 t + \tfrac{1}{2} g t^2, \qquad v = v_0 + g t
$$

- Lempar ke atas dengan $v_0$ (ambil atas positif): di puncak **$v=0$**, lalu turun dengan tanda berlawanan.
- **Massa tidak berpengaruh** (tanpa hambatan udara) → semua benda punya percepatan yang sama.

---

## 5) Simbol & Notasi (ringkas)
| Simbol      | Arti                            | Satuan SI |
|-------------|---------------------------------|-----------|
| $x, y, s$   | posisi/koordinat/perpindahan    | m         |
| $v$         | kecepatan                       | m/s       |
| $a$         | percepatan                      | m/s$^2$   |
| $t$         | waktu                           | s         |
| $g$         | percepatan gravitasi (vertikal) | m/s$^2$   |

---

## 6) Contoh Terkendali (step-by-step)
> Bukan soal tugas, hanya contoh pola pengerjaan. Kerjakan ulang sendiri untuk latihan.

### Contoh A — Menentukan $a$ dari perubahan kecepatan
**Diketahui**: perubahan kecepatan $\Delta v = 10\,\mathrm{m/s}$ dalam $\Delta t = 2\,\mathrm{s}$. Cari $a$.

**Penyelesaian**:

$$
a = \frac{\Delta v}{\Delta t} = \frac{10}{2} = 5\,\mathrm{m/s^2}
$$

---

### Contoh B — Jarak saat mempercepat
**Diketahui**: mobil dari $v_0 = 5\,\mathrm{m/s}$ menjadi $v = 10\,\mathrm{m/s}$ selama $t = 5\,\mathrm{s}$, $a$ konstan. Berapa jarak $\Delta x$?

**Langkah 1**: gunakan $v = v_0 + a t$ untuk cari $a$.

$$
a = \frac{v - v_0}{t} = \frac{10 - 5}{5} = 1\,\mathrm{m/s^2}
$$

**Langkah 2**: pakai $\Delta x = v_0 t + \tfrac{1}{2} a t^2$.

$$
\Delta x = 5(5) + \tfrac{1}{2}(1)(5^2) = 25 + 12.5 = 37.5\,\mathrm{m}
$$

---

### Contoh C — Berhenti karena perlambatan
**Diketahui**: sebuah mobil $v_0 = 72\,\mathrm{km/h} = 20\,\mathrm{m/s}$, perlambatan $a = -2\,\mathrm{m/s^2}$. Jarak sampai berhenti?

**Gunakan** $v^2 = v_0^2 + 2 a \Delta x$ dengan $v=0$.

$$
0 = 20^2 + 2(-2)\,\Delta x \;\Rightarrow\; \Delta x = \frac{400}{4} = 100\,\mathrm{m}
$$

---

### Contoh D — Jatuh bebas sederhana
**Diketahui**: batu dijatuhkan dari $h=20\,\mathrm{m}$, ambil atas positif ($g=-10$). Waktu dan kecepatan saat menyentuh tanah?

**Waktu**: dari $y - y_0 = \tfrac{1}{2} g t^2$ dengan $v_0=0$ dan $y - y_0 = -20$ (turun 20 m):

$$
-20 = \tfrac{1}{2}(-10) t^2 \;\Rightarrow\; t^2 = 4 \;\Rightarrow\; t = 2\,\mathrm{s}
$$

**Kecepatan**: $v = v_0 + g t = 0 + (-10)(2) = -20\,\mathrm{m/s}$ (tanda minus = arah ke bawah).

---

## 7) Pola Soal yang Sering Muncul
1. **Diberi $v_0, a, t$ → cari $v$ atau $\Delta x$** (pakai persamaan 1 & 2).
2. **Diberi $v_0, v, a$ → cari $\Delta x$** (pakai persamaan 3).
3. **Freefall**: ganti $a$ dengan $g$ dan hati-hati dengan **tanda**.
4. **Perlambatan**: $a$ berlawanan arah dengan $v$ (nilai negatif jika arah positif mengikuti $v$ awal).

---

## 8) Mini‑Check (coba dulu, lalu bandingkan dengan rumus)
- [Q1] Bola dilempar vertikal ke atas dengan $v_0 = 15\,\mathrm{m/s}$ (atas positif, $g=-10$). Berapa waktu ke puncak? (hint: puncak $v=0$)  
- [Q2] Truk melambat seragam dari $v_0=12\,\mathrm{m/s}$ ke $v=4\,\mathrm{m/s}$ selama $8\,\mathrm{s}$. Berapa $a$ dan jarak tempuhnya?  
- [Q3] Sebuah benda jatuh bebas selama $3\,\mathrm{s}$. Berapa $v$ dan jarak yang ditempuh?  

---

## 9) Catatan Implementasi untuk PBA/Game
- Update posisi diskret:
  
  ```csharp
  // semi-implicit (symplectic) Euler
  v += a * dt;      // update velocity dulu
  x += v * dt;      // lalu posisi
  ```
- Jangan lupa **dt** kecil dan **konvensi sumbu** konsisten (mis. +y ke atas → g = −9.81).
