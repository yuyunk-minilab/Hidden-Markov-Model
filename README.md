# Hidden Markov Model (HMM)

Repository ini berisi implementasi dan contoh pembelajaran **Hidden Markov Model (HMM)** menggunakan Python. Materi mencakup konsep dasar HMM, perhitungan probabilitas observasi, **Forward Algorithm**, dan **Viterbi Algorithm** untuk menentukan hidden state yang paling mungkin.

## 📌 About

**Hidden Markov Model (HMM)** adalah model probabilistik yang digunakan untuk memodelkan sistem yang memiliki **state tersembunyi (hidden states)** yang menghasilkan serangkaian observasi.

Dalam HMM, terdapat dua jenis variabel utama:

* **Hidden State** — kondisi sistem yang tidak dapat diamati secara langsung.
* **Observation** — data yang dapat diamati dan dihasilkan oleh hidden state.

HMM banyak digunakan dalam berbagai bidang, seperti:

* Speech Recognition
* Natural Language Processing
* Pattern Recognition
* Time Series Analysis
* Bioinformatics
* Activity Recognition
* Artificial Intelligence

---

## 🎯 Learning Objectives

Setelah mempelajari repository ini, pengguna diharapkan mampu:

1. Memahami konsep dasar Hidden Markov Model.
2. Memahami hubungan antara hidden state dan observation.
3. Menentukan probabilitas awal (*initial state probability*).
4. Menentukan probabilitas transisi (*transition probability*).
5. Menentukan probabilitas emisi (*emission probability*).
6. Menghitung probabilitas suatu sequence menggunakan **Forward Algorithm**.
7. Menentukan urutan hidden state yang paling mungkin menggunakan **Viterbi Algorithm**.
8. Mengimplementasikan HMM menggunakan Python dan library `hmmlearn`.

---

## 🧩 Components of HMM

Sebuah Hidden Markov Model terdiri dari beberapa komponen utama.

### 1. Initial State Probability

Menunjukkan probabilitas sistem berada pada masing-masing hidden state pada waktu awal.

Contoh:

```text
State 0 = 0.6
State 1 = 0.4
```

atau:

$$
\pi = [0.6, 0.4]
$$

### 2. Transition Probability

Menunjukkan probabilitas perpindahan dari satu hidden state ke hidden state lainnya.

Contoh:

$$
A =
\begin{bmatrix}
0.7 & 0.3 \\
0.4 & 0.6
\end{bmatrix}
$$

Artinya:

* State 0 → State 0 = 0.7
* State 0 → State 1 = 0.3
* State 1 → State 0 = 0.4
* State 1 → State 1 = 0.6

### 3. Emission Probability

Menunjukkan probabilitas suatu hidden state menghasilkan observasi tertentu.

Contoh:

| State   | Clean | Walk | Shop |
| ------- | ----: | ---: | ---: |
| State 0 |   0.1 |  0.4 |  0.5 |
| State 1 |   0.6 |  0.3 |  0.1 |

---

## 🔢 Example

Misalkan terdapat tiga jenis observasi:

```text
clean
walk
shop
```

Observasi kemudian dikonversi menjadi:

```text
clean = 0
walk  = 1
shop  = 2
```

Contoh sequence:

```text
clean → clean → walk → walk → shop
```

Model kemudian digunakan untuk menjawab dua pertanyaan utama:

### Probability of Observation Sequence

Berapa probabilitas model menghasilkan sequence:

```text
clean → clean → walk → walk → shop
```

Perhitungan dilakukan menggunakan **Forward Algorithm**.

### Most Likely Hidden State Sequence

Hidden state apa yang paling mungkin menghasilkan sequence tersebut?

Perhitungan dilakukan menggunakan **Viterbi Algorithm**.

Contoh hasil:

```text
Observation : clean → clean → walk → walk → shop
               ↓       ↓       ↓      ↓       ↓
State        :  1   →   1   →   0  →  0   →   0
```

Sehingga hidden state sequence yang paling mungkin adalah:

```text
[1, 1, 0, 0, 0]
```




## 🚀 Applications

Hidden Markov Model dapat diterapkan pada berbagai permasalahan, antara lain:

* **Activity Recognition**
  Mendeteksi aktivitas berdasarkan sequence sensor.

* **Speech Recognition**
  Memodelkan hubungan antara suara yang diamati dan state fonetik tersembunyi.

* **Natural Language Processing**
  Part-of-Speech tagging dan sequence labeling.

* **Pattern Recognition**
  Mengenali pola berdasarkan data sequence.

* **Game AI**
  Memodelkan perilaku pemain atau kondisi lingkungan yang tidak dapat diamati secara langsung.

---

## 👩‍💻 Author

**Yuyun Khairunisa**

Lecturer & Researcher in Computer Science, Digital Games, Artificial Intelligence, and Interactive Media.

---

## 📄 License

This repository is intended for educational and research purposes.
