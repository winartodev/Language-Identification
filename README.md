# Language-Identification
Language Identification adalah salah satu project Machine Learning yang berfokus pada
pemrosesan bahasa alami (Natural Language Processing) pada project kali ini saya
menggunakan 2 algoritma yakni algoritma N-Gram dan algoritma Naive Bayes Classification. 

## N-Gram 
N-Gram adalah model probabilistik yang awalnya dirancang oleh ahli matematika dari rusia pada awal abad ke-20
dan kemudian dikembangkan untuk memprediksi item berikutnya dalam urutan item. Item bisa berupa huruf / karakter, kata atau yang lain sesuai dengan aplikasi. salah satunya n-gram yang berbasis kata di gunakan utnuk memprediksi kata berikutnya dengan urutan kata tertentu. <br>

## Naive Bayes Classifier
Naïve Bayes Classifier merupakan sebuah metoda klasifikasi yang berakar pada teorema Bayes . Metode pengklasifikasian dg menggunakan metode probabilitas dan statistik yg dikemukakan oleh ilmuwan Inggris Thomas Bayes , yaitu memprediksi peluang di masa depan berdasarkan pengalaman di masa sebelumnya sehingga dikenal sebagai Teorema Bayes. <br>
Menurut Olson Delen (2008) menjelaskan Naïve Bayes unt setiap kelas keputusan, menghitung probabilitas dg syarat bahwa kelas keputusan adalah benar, mengingat vektor informasi obyek. Algoritma ini mengasumsikan bahwa atribut obyek adalah independen. Probabilitas yang terlibat dalam memproduksi perkiraan akhir dihitung sebagai jumlah frekuensi dr ” master ” tabel keputusan.

## Penggunaan Project Language Identification 
Project ML ini bisa di gunakan ke berbagai platfrom project baik itu web, android ataupun desktop. cara penggunaannya bisa di lihat di bawah ini 
1. Clone project: <br>
```
    git clone https://github.com/winartodev/Language-Identification.git
```
2. Akses folder <a href="https://github.com/winartodev/Language-Identification/tree/main/joblib_model"> joblib_model </a> kemudan copy `count_vectorizer.joblib` dan `model.joblib` setelah itu letakkan file tersebut kedalam project yang ingin anda bangun 

3. Kemudian ketika ingin menggunakan ke-2 file tersebut anda bisa membuat file baru `model_joblib.py` 
```
from joblib import load
import numpy as np
from sklearn.preprocessing import LabelBinarizer

def model(): 
    count_vectorizer = load('your_path\count_vectorizer.joblib')
    model = load('your_path\model.joblib')

    lb = LabelBinarizer()
    word = 'Saya Mau Makan'
    result = model.predict(count_vectorizer.transform(np.array([word])))

    return result
```
 