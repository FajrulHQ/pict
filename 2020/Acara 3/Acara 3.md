<center> <h1> Modul Praktikum Numerik </h1> </center>
<center> <h2> Acara 3. Interpolasi dan kurva fitting </h2> </center>

> ### Link Modul
> * [Google Drive](https://drive.google.com/drive/folders/1uMaBNZ2VWBWpx080plEPaRVnLfh66UfH?usp=sharing)
> * [Github](https://github.com/FajrulHQ/Prakt-Numerik)
>>  * [Acara 1 (Drive) - Sistem Persamaan Linear simultaneous)](https://drive.google.com/drive/u/0/folders/1183IOE2AyPF-gyQVuzTEYEBTQUtLgtzp)
>>  * [Acara 2 (Drive) - Sistem non linear dan mencari akar](https://drive.google.com/drive/folders/1uMaBNZ2VWBWpx080plEPaRVnLfh66UfH?usp=sharing)
>>  * [Acara 3 (Drive) - Interpolasi dan kurva fitting](https://drive.google.com/drive/folders/1uMaBNZ2VWBWpx080plEPaRVnLfh66UfH?usp=sharing)

---

> ## Interpolasi :
> ### A. Interpolasi Polinomial
> Polinomial orde ke-n digunakan sebagai interpolasi fungsi
<center>
<img src="https://render.githubusercontent.com/render/math?math=f(x)=b_0 %2Bb_1x %2Bb_2x^2 %2Bb_3x^3%2B\cdots%2Bb_nx^n ">
</center><br>

> Contoh :
Estimasi nilai `f(2.2)` dari data dibawah ini!
<center>

| _x_ | _f(x)_ |
|:----:|:----:|
| 1 | 1 |
| 2 | 8 |
| 3 | 27 |
| 4 | 64 |
</center>

Solusi :
Nilai `f(2.2)` diestimasi menggunakan interpolasi polinomial orde kedua:
<center>
<img src="https://render.githubusercontent.com/render/math?math=f(x)=b_0%2Bb_1x%2Bb_2x^2 ">
</center>

---
<img src="https://render.githubusercontent.com/render/math?math= ">

> ## Curve Fitting :
> Data-data yang bersifat diskrit dapat dibuat continuum melalui proses curve-fitting. Curve-fitting merupakan proses data-smoothing, yakni proses pendekatan terhadap kecenderungan data-data dalam bentuk persamaan model matematika.
Misalkan tersedia data-data `y` pada berbagai `x` (sejumlah `n` pasang), maka dapat dicari suatu persamaan `y = f(x)` yang memberikan hubungan `y` dengan `x` yang mendekati data. Proses ini disebut curve fitting.

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture1.png?raw=true">
</center><br>

> Langkah-langkah yang dapat ditempuh untuk menentukan persamaan empirik adalah sebagai berikut: 
>1.	Membuat grafik `y` versus `x` berdasarkan data yang tersedia
>1.	Meramalkan bentuk persamaan yang kira-kira sesuai (mengandung tetapan-tetapan yang belum diketahui), berdasarkan grafik Misal: 
>>  *  Persamaan linier: <img src="https://render.githubusercontent.com/render/math?math=y=ax%20,%20y = a_0 %2B a_1x">
>>  *  Persamaan kuadrat: <img src="https://render.githubusercontent.com/render/math?math=y = a_0%2Ba_1x%2Ba_2x^2"> 
>>  *   Persamaan polinomial berorde-m: <img src="https://render.githubusercontent.com/render/math?math=y = a_0%2Ba_1 x%2Ba_2 x^2%2B... %2B a_{m-1} x^{m-1}%2Ba_m x^m">
>>  *   Persamaan eksponensial: <img src="https://render.githubusercontent.com/render/math?math=y = a e^{bx}"> 
>3.	Mengevaluasi nilai tetapan-tetapan tersebut berdasarkan data yang ada `Æ` regresi Secara garis besar, metode regresi ada 2 macam: __(a) regresi linier__ dan __(b) regresi non-linier__ 
>4.	Mengevaluasi kesesuaian persamaan empirik terhadap data. 

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture2.png?raw=true">
</center><br>

> Cara mengevaluasi nilai-nilai tetapan dalam persamaan empirik: __visual inspection__, __method of average__, dan __metode kuadrat terkecil__ (_least squares_). Metode kuadrat terkecil merupakan metode yang paling banyak digunakan. Pada metode ini, nilai-nilai tetapan terbaik adalah yang memberikan jumlah kuadrat kesalahan/penyimpangan (_sum of squares of errors_, __SSE__) yang terkecil (minimum).

>Bentuk persamaan linier: (1) `y = a x` dan (2) `y = a_0 %2B a_1 x`

---

> ### 1. Bentuk Persamaan: y=ax
> ingin dicari harga a (a biasa disebut sebagai slope)
Untuk pasangan data `xi`, `yi`, maka error-nya adalah:
<center><img src="https://render.githubusercontent.com/render/math?math=R_i=a x_i- y_i	=y_{terhitung }- y_{data}"></center><br>

>> sehingga nilai sum of squares of errors-nya: 
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture3.png?raw=true"><br>
</center>

>> Harga a terbaik adalah yang memberikan SSE minimum. Harga SSE akan minimum jika:
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture4.png?raw=true" >
</center>

>>> Sehingga: 
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture5.png?raw=true" >
</center><br> 
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture6.png?raw=true" >
</center><br>

>>> Atau 
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture7.png?raw=true" >
</center><br>

---

> ### 2.  Bentuk Persamaan: y = a<sub>0</sub> %2B a<sub>1</sub>x
> ingin dicari harga `a_0` dan `a_1` (`a_0` biasa disebut sebagai intercept dan `a_1` sebagai slope). Dengan cara yang sama, untuk pasangan data `xi`, `yi`, maka error-nya adalah:
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture8.png?raw=true" >
</center>

>> Sehingga nilai sum of squares of errors-nya:
<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture9.png?raw=true" >
</center><br>

>> Harga SSE akan minimum jika: 

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture10.png?raw=true" >
</center><br>

>>> Sehingga:

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture11.png?raw=true" >
</center><br>

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture12.png?raw=true" >
</center><br>

>>> Dan 

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture13.png?raw=true" >
</center><br>

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture14.png?raw=true" >
</center><br>

>> Berdasarkan persamaan (11) dan (12), maka harga `a_0` dan `a_1` ¬ dapat ditentukan. Misal, dengan menggunakan __Cramer’s rule__, diperoleh:

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture15.png?raw=true" >
</center><br>

> Maka:

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture16.png?raw=true" >
</center><br>

<center>
<img alt="Acara 3" src = "https://github.com/FajrulHQ/pict/blob/main/Acara%203/Picture17.png?raw=true" >
</center>