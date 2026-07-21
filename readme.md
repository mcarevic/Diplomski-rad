# Prilagodba sučelja MillenniumOS & Custom Post Processor

**Diplomski rad** – Marko Carević  
Fakultet informatike u Puli, Sveučilište Jurja Dobrile u Puli  
Mentor: doc. dr. sc. Sandi Baressi Šegota  
2026.

---

Ovaj repozitorij sadrži dva odvojena, ali povezana praktična doprinosa diplomskog rada:

1. **Custom Post Processor** za HSMWorks Ultimate → MillenniumOS  
2. **Prilagodba MillenniumOS DWC plugina** (custom slike za probing sučelje)

Oba rješenja su open source i namijenjena korisnicima Millennium Machines Milo v1.5.

---

## 1. Custom Post Processor za HSMWorks Ultimate

### Problem
Službeni post procesor za MillenniumOS postoji samo za **Autodesk Fusion 360**.  
Korisnici koji rade u **HSMWorks Ultimate** (SolidWorks) nisu mogli generirati ispravan G-kod zbog razlika u verziji Autodesk post enginea.

### Rješenje
Prilagođen post procesor razvijen kroz **7 iterativnih verzija**:

| Verzija | Što je riješeno |
|---------|-----------------|
| v1 – v2 | Osnovna kompatibilnost + shimovi za nepodržane API funkcije |
| v3 – v4 | G2/G3 lukovi (selektivna linearizacija) + M4005 (tool description) |
| v5 – v6 | Radni koordinatni sustavi (G54–G59) + tool change logika + testiranje na stroju |
| **v7 (konačna)** | Stabilna verzija – pouzdano radi sa svim relevantnim operacijama |

### Ključne prilagodbe
- Kompatibilnostni shimovi između Fusion 360 i HSMWorks enginea
- Selektivna linearizacija lukova
- Potpuna podrška za **M4005** (tool description)
- Ispravno upravljanje tool change i tool length compensation
- Podrška za probing i radne koordinate

### Testirano na
- 2D / 3D glodanje
- Adaptivno glodanje
- Bušenje i navoji
- Probing operacije
- Više radnih koordinatnih sustava
- Kombinirane operacije
### 📁 MillenniumOS

- `MillenniumOS-MOS_V1.zip`
- `MillenniumOS-MilleniumOs-MC V2.zip`
- `MillenniumOS-MilleniumOs-MC V3.zip`
- `MillenniumOS-MilleniumOs-MC V4.zip`
- `MillenniumOS-MilleniumOs-MC v5.zip`
- `MillenniumOS-0.5.0-MC V6.zip`

## Screenshots

| Slika 1 | Slika 2 |
|:-------:|:-------:|
| ![Slika 1](Images/slika%201.png) | ![Slika 2](Images/slika%202.png) |

| Slika 3 | Slika 4 |
|:-------:|:-------:|
| ![Slika 3](Images/slika%203.png) | ![Slika 4](Images/slika%204.png) |

## Autor

**Marko Carević**  

Diplomski rad, Fakultet informatike u Puli (FIPU), 2026.  

Mentor: doc. dr. sc. Sandi Baressi Šegota
