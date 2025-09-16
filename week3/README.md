\# 📘 Physically Based Animation – Week 3 Notes

\### Topik: Projectile Motion (Gerak Parabola)



---



\## 1) Gambaran Umum

\- \*\*Gerak parabola\*\* = kombinasi:

&nbsp; - \*\*GLB\*\* di sumbu-x (kecepatan konstan)

&nbsp; - \*\*GLBB\*\* di sumbu-y (ada gravitasi)

\- Sumbu-x dan sumbu-y \*\*independen\*\*.



---



\## 2) Persamaan Dasar

\*\*Komponen awal kecepatan:\*\*

\\\[

v\_{0x} = v\_0 \\cos\\theta, \\quad v\_{0y} = v\_0 \\sin\\theta

\\]



\*\*Sumbu-x (GLB):\*\*

\\\[

a\_x = 0, \\quad v\_x = v\_{0x}, \\quad s\_x = s\_{0x} + v\_{0x} t

\\]



\*\*Sumbu-y (GLBB):\*\*

\\\[

a\_y = g, \\quad v\_y = v\_{0y} + g t, \\quad s\_y = s\_{0y} + v\_{0y} t + \\tfrac{1}{2} g t^2

\\]



---



\## 3) Rumus Cepat

\- \*\*Waktu ke puncak:\*\*  

\\\[

t\_\\text{up} = \\frac{v\_{0y}}{|g|}

\\]



\- \*\*Tinggi maksimum:\*\*  

\\\[

h\_\\text{max} = \\frac{v\_{0y}^2}{2|g|}

\\]



\- \*\*Waktu total (mendarat, jika tinggi awal = akhir):\*\*  

\\\[

t\_\\text{flight} = \\frac{2 v\_{0y}}{|g|}

\\]



\- \*\*Jangkauan mendatar (range):\*\*  

\\\[

R = v\_{0x} \\cdot t\_\\text{flight} = \\frac{v\_0^2 \\sin(2\\theta)}{|g|}

\\]



\- \*\*Di puncak:\*\*  

\\\[

v\_y = 0, \\quad v\_x = v\_{0x}, \\quad a\_y = g, \\quad a\_x = 0

\\]



---



\## 4) Contoh Soal dari Slide



\### Exercise 1  

\*\*Dik:\*\* \\(v\_0 = 10\\,\\mathrm{m/s}, \\theta = 45^\\circ, g = -10\\).  

\*\*Dit:\*\* \\(h\_\\text{max}\\), \\(t\_\\text{flight}\\), \\(R\\), \\(v\_y\\) di puncak.



\### Exercise 2  

\*\*Dik:\*\* \\(v\_0 = 20\\,\\mathrm{m/s}, \\theta = 37^\\circ, g = -10\\).  

\*\*Dit:\*\* tinggi maksimum, waktu mendarat, jarak mendatar, \\(v\_y\\) di puncak, percepatan (x \& y) di puncak.



\### Exercise 3  

\*\*Dik:\*\* pesawat \\(v = 360\\,\\mathrm{km/h} = 100\\,\\mathrm{m/s}\\), tinggi \\(s\_{0y} = 500\\,\\mathrm{m}\\), \\(v\_{0y}=0\\).  

\*\*Dit:\*\* jarak mendatar bom saat jatuh.



\### Exercise 4 (Challenge)  

\*\*Dik:\*\* granat \\(v\_0 = 20\\,\\mathrm{m/s}, \\theta = 45^\\circ, g = -10\\), target dummy 40 m, radius 2 m.  

\*\*Dit:\*\* waktu di udara, jarak ledak, apakah mengenai target.



---



\## 5) Catatan Implementasi (PBA/Game)



```csharp

// Komponen awal

float v0x = v0 \* Mathf.Cos(theta);

float v0y = v0 \* Mathf.Sin(theta);



// Update per frame

vx = v0x;               // konstan

vy = v0y + g \* t;       // GLBB

sx = s0x + v0x \* t;

sy = s0y + v0y \* t + 0.5f \* g \* t \* t;

```



