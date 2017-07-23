---
layout: post
title: "Python'da Request Post Modülü"
date: 2017-07-20
---

   Request modülü, organik HTTP paketleri göndermeye yarayan python modülüdür.Bu modülü kullandığınızda 
sorgu dizelerini URL'lere manuel olarak eklemenize veya POST verilerinizi manuel olarak biçimlendirmenize gerek kalmaz.
   
   Öncelikle modülü bilgisayara kurmak için aşağıdaki komutu terminale yazıp çalıştırın.
```
   $ pip install requests
```
   Requests GitHub'da geliştirildiğinden, kaynak kodunu GitHub'dan clone etmek için,
   
```
   $ git clone git://github.com/requests/requests.git
```

komutunu çalıştırdıktan sonra modül kurulmuş olur. Geri kalanı için modülü bir projede kullanacağımdan PyCharm geliştirme ortamını kurdum.
PyCharm'ı https://www.jetbrains.com/pycharm/ linkinden indirebilirsiniz.
   Request modülünü projenizde çalıştırabilmeniz için;
```
    import requests
    
```
Kütüphanesini eklemeniz gerekiyor.
Requests get ve post metodları için verileri alacağımız ve göndereceğimiz url'ler gerekli.

``` 

r = requests.get('https://example.com')

```
Böylece web sitesinden ihtiyacımız olan bilgileri artık ``r`` nesnesinden alabiliriz.
Post metodu için de aynı şekilde bir nesne oluşturup veri gönderimi yapabiliriz. Göndereceğimiz veriyi veriyi sözlük şeklinde
belirtip aşağıdaki gibi post isteği oluşturabiliriz.

```

r = requests.post('http://example.org', data = {'key':'value'})

```
Eğer HTTP header eklemek isterseniz header parametresine sözlük olarak bildirmeniz gerekir.
```
headers = {

        'content-type': 'application/json',
        'origin': 'http://XXX.net'

    }

url = 'https://example.com'
r = requests.get(url, headers=headers)
    

```
Bu şekilse get ve post metodlarını kullanarak istek oluşturabilirsiniz.


