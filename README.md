# Klasifikasi Alzheimer Empat Kelas Berdasarkan Data MRI Otak Menggunakan Model DenseNet169, ResNet50, dan VGG16

Penggunaan deep learning untuk analisis citra medis makin meningkat, terutama untuk citra MRI otak. Deep learning mampu melakukan klasifikasi pada citra tersebut sehingga membantu 
diagnosis untuk suatu penyakit tertentu, termasuk Alzheimer. 

Ada berbagai penelitian yang menggunakan deep learning untuk klasifikasi Alzheimer. Dalam pengujian ini, dilakukan klasifikasi Alzheimer empat kelas, yaitu Moderate Demented, Mild Demented, Very Mild Demented, dan Nondementedatau normal. Data untuk pengujian ini didapatkan dari kaggle. Data tersebut sudah cukup banyak tetapi sangat tidak seimbang sehingga perlu augmentasi, terutama untuk kelas dengan data yang masih sangat sedikit. 

Terdapat tiga model yang diuji dan dibandingkan, yaitu DenseNet169, ResNet50, dan VGG16. Pengujian menunjukan bahwa ketiga modelsudah memberikan performa yang cukup baik dalam hal akurasi dan nilai AUC dengan nilai akurasi dari ketiganya berturut-turut sebesar 97.16%, 94.67%, 98.89%. Secara umum, model VGG16 memberikan performa yang terbaik dari berbagai sisi. Namun, dibanding dua model lainnya, waktu training model VGG16 tiga kali lebih lamasehingga dapat menjadi pertimbangan tersendiri.

---

Data yang digunakan di sini adalah data MRI untuk **Alzheimer 4 kelas (MildDemented, ModerateDemented, NonDemented, VeryMildDemented)** yang didapatkan dari [kaggle](https://www.kaggle.com/tourist55/alzheimers-dataset-4-class-of-images). 

**Data tersebut sudah cukup banyak, namun sangat tidak seimbang**. Karenanya, perlu dilakukan augmentasi terutama untuk kelas yang datanya masih sedikit. Data tersebut juga sudah dibagi menjadi "train" dan "test", namun pembagiannya kurang uniform. Karenanya, datanya dibagi ulang menjadi tiga ("train", "val", "test") dengan cara acak agar bisa lebih uniform.

**Pengujian dilakukan dengan tiga model** untuk membandingkan performanya. Untuk setiap model, parameter dan layer tambahannya dibuat mirip namun juga disesuaikan agar lebih optimal untuk model itu sendiri. 

Yang diukur dalam pengujian ini adalah **loss value, akurasi, presisi, recall, dan AUC**. Dibuat pula plot antara parameter ukur itu terhadap epochs sehingga dapat terlihat perkembangannya. 

Ada berbagai referensi yang digunakan dalam pengerjaan ini, yang utama adalah [kode](https://www.kaggle.com/brycesmith/smith-burns-cosmas-99-testaccuracy/comments) dari **Bryce Smith dan koleganya**
