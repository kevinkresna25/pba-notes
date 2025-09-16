# 📘 Physically Based Animation – Week 3 Notes
### Topik: Projectile Motion (Gerak Parabola)

---

## 1. Gambaran Umum
- **Gerak parabola** = kombinasi:
  - **GLB** di sumbu-x (kecepatan konstan)
  - **GLBB** di sumbu-y (ada gravitasi)
- Sumbu-x dan sumbu-y **independen**.

---

## 2. Persamaan Dasar

**Komponen awal kecepatan:**

$$
v_{0x} = v_0 \cos\theta, \quad v_{0y} = v_0 \sin\theta
$$

**Sumbu-x (GLB):**

$$
a_x = 0, \quad v_x = v_{0x}, \quad s_x = s_{0x} + v_{0x} t
$$

**Sumbu-y (GLBB):**

$$
a_y = g, \quad v_y = v_{0y} + g t, \quad s_y = s_{0y} + v_{0y} t + \tfrac{1}{2} g t^2
$$

---

## 3. Rumus Cepat

- **Waktu ke puncak:**

$$
t_\text{up} = \frac{v_{0y}}{|g|}
$$

- **Tinggi maksimum:**

$$
h_\text{max} = \frac{v_{0y}^2}{2|g|}
$$

- **Waktu total (mendarat, jika tinggi awal = akhir):**

$$
t_\text{flight} = \frac{2 v_{0y}}{|g|}
$$

- **Jangkauan mendatar (range):**

$$
R = v_{0x} \cdot t_\text{flight} = \frac{v_0^2 \sin(2\theta)}{|g|}
$$

- **Di puncak:**

$$
v_y = 0, \quad v_x = v_{0x}, \quad a_x = 0, \quad a_y = g
$$

---

## 4. Contoh Soal dari Slide

### Exercise 1
**Dik:** $v_0 = 10 \,\mathrm{m/s}, \; \theta = 45^\circ, \; g = -10$  
**Dit:** $h_\text{max}$, $t_\text{flight}$, $R$, $v_y$ di puncak  

---

### Exercise 2
**Dik:** $v_0 = 20 \,\mathrm{m/s}, \; \theta = 37^\circ, \; g = -10$  
**Dit:** Tinggi maksimum, waktu mendarat, jarak mendatar, $v_y$ di puncak, percepatan (x & y) di puncak  

---

### Exercise 3
**Dik:** Pesawat dengan: $v = 360 \,\mathrm{km/h} = 100 \,\mathrm{m/s}, \; s_{0y} = 500 \,\mathrm{m}, \; v_{0y} = 0$  
**Dit:** Jarak mendatar bom saat jatuh  

---

### Exercise 4 (Challenge)
**Dik:** $v_0 = 20 \,\mathrm{m/s}, \; \theta = 45^\circ, \; g = -10$  
Target dummy di 40 m, radius ledak 2 m  
**Dit:** Waktu di udara, jarak ledak, apakah mengenai target  

---

## 5. Catatan Implementasi (PBA/Game)

```csharp
// Komponen awal
float v0x = v0 * Mathf.Cos(theta);
float v0y = v0 * Mathf.Sin(theta);

// Update per frame
vx = v0x;               // konstan (GLB)
vy = v0y + g * t;       // GLBB
sx = s0x + v0x * t;
sy = s0y + v0y * t + 0.5f * g * t * t;
```
