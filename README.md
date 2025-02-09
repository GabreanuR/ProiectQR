# **Proiect QR - Scan Gogh**

## **Echipă**
- **Gabreanu Răzvan-George** - grupa 134, seria 13
- **Săpunaru Maia** - grupa 134, seria 13
- **Mocanu Ruxandra-Ioana** - grupa 134, seria 13

---

## **Descriere**
Proiectul implementează un sistem pentru generarea și citirea codurilor QR. Acesta include un meniu principal, care oferă două funcționalități principale:
1. **Generarea unui cod QR**
2. **Citirea unui cod QR**

---

## **Generarea unui cod QR**
Procesul de creare a unui cod QR se desfășoară în următorii pași:

1. Preluăm șirul de caractere introdus de utilizator.
2. Convertim șirul într-un șir binar.
3. Aplicăm secvențele inițiale și finale asupra șirului binar.
4. Împărțim șirul binar în blocuri, în funcție de numărul de caractere.
5. Adăugăm codurile pentru corecția erorilor (**ECC - Error Correction Code**).
6. Reorganizăm biții conform ordinii necesare unui cod QR valid.
7. Construim o matrice QR (reprezentată prin `0` și `1`, corespunzând alb și negru).
8. Aplicăm formatul QR, adăugând colțurile și liniile rezervate.
9. Introducem șirul de biți în matricea QR.
10. Aplicăm cele 8 măști posibile și selectăm cea mai potrivită conform criteriilor de optimizare.
11. Aplicăm formatul final.
12. Convertim matricea QR într-un fișier **PNG**.

---

## **Citirea unui cod QR**
Procesul de citire a unui cod QR include următorii pași:

1. Redimensionăm imaginea astfel încât fiecare pixel să poată fi accesat corect.
2. Construim o matrice formată doar din valori `0` și `1` (**alb/negru**).
3. Determinăm masca aplicată utilizând biții de decizie.
4. Identificăm versiunea codului QR pentru a decripta corect datele.
5. Eliminăm masca aplicată asupra codului QR.
6. Parcurgem biții în ordine **zig-zag** pentru a extrage datele.
7. Convertim șirul de biți într-un **string** final decodificat.

---

## **Bibliografie**

### **Ghiduri generale despre QR Codes:**
- [Creating a QR Code - Nayuki](https://www.nayuki.io/page/creating-a-qr-code-step-by-step)

### **Generarea fișierelor PNG din matrice binară:**
- [Pillow - Convert to PNG](https://stackoverflow.com/questions/78913551/python-using-pillow-to-convert-any-format-to-png-any-way-to-speed-the-process)
- [GeeksforGeeks - Convert Numpy to Image](https://www.geeksforgeeks.org/convert-a-numpy-array-to-an-image/)

### **Generarea codurilor de corecție a erorilor (ECC):**
- [Reed-Solomon Codec](https://pypi.org/project/reedsolo/#basic-usage-with-high-level-rscodec-class)

### **Informații despre formatul QR Code:**
- [Format și versiune QR Code](https://www.thonky.com/qr-code-tutorial/format-version-information)

### **Citirea pixelilor din imagini:**
- [StackOverflow - RGB pixel values](https://stackoverflow.com/questions/138250/how-to-read-the-rgb-value-of-a-given-pixel-in-python)
- [YouTube - Reading Image Pixels](https://www.youtube.com/watch?v=6Hk5KyiEktI)

### **Structura și formatarea datelor în QR Codes:**
- [YouTube - Timing & Alignment Patterns](https://www.youtube.com/watch?v=pamazHwk0hg)
- [GeeksforGeeks - Convert Binary to String](https://www.geeksforgeeks.org/convert-binary-to-string-using-python/)

### **Detectarea măștii optime pentru un QR Code:**
- [Reddit - How to Read QR Codes](https://www.reddit.com/r/LearnUselessTalents/comments/esidvc/the_simplest_guide_to_read_qr_codes/)
- [Exemplu de analiză a măștilor QR](https://imgur.com/a/FvtpZ2o)

---

Acest document oferă o descriere clară a procesului de generare și citire a codurilor QR, împreună cu referințele necesare pentru implementare. 

