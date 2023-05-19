# Machine_learning_basic_test

# Proje Amacı Genel Bilgi
- ilk hedef olarak basit makine öğrenmesi projeleri geliştirmeye çalışıyorum amacım en basit örnekleri yaparak makine öğrenmesinin temmellerini öğrenmek
- Bu konu hakkındaki ilk çalışmam olduğunu belirtebilrim. Hiç bir şey bilmediğimi yazdığım şeylerin tamamen mantıksız olabileceğini kabul ediyor ve bu konuyla yeni ilgileniyorsanız yazacağım şeyleri kronolojik sırası ile inceleyeniz. Zaman içerisinde güncellenen bir repo olacaktır. Yazdıklarımın tamamen mantıksız olsa dahi yeni başlayanların düşeceği yanılgılar ve yanlışlarla dolu olabilir . Kronolojik sıra ile bu yanlışları tek tek belirteceğim. Böyle bir durumda yeni başlayanlar için belirli bir zaman sonra çok iyi bir kaynak olacağını düşünüyorum. 

# Modeller
## The Sequential model
Karşılaşacağım en basit model denilebilir.
Olayı gayet basit bir şekilde kurgulanabilir olmasıdır.
Bu model çeşidinde modelin implementasyonu basittir. Bir modelin basit olması için:
- Birden farklı input kaynağının olmaması
- Çoklu output hedeflerine sahip olmaması
- Katmanları tekrar tekrar kullanmaması (reusability)
Gerekir. Buna göre bir modelin inputu tek bir yerden geliyorsa, outputu tek bir yere gidiyorsa, katmanlar başka modellerde kullanılmıyorsa o model basittir diyebiliriz.
!!!! https://www.datasciencearth.com/keras-model-wars-sequential-vs-functional/ sitesinden alınan bilgiler
#### Katmanlarda kullanabileceğimiz fonksiyonlar
- belirli bir zaman sonra listeleyeceğim
#### Genel yapı
- Input layer
- Hidden layers
- Output layer

Genel yapı bu şekilde oluşur

# Yapılmış Uygulamalar
## Sayi tahmini
Sequantial model kullanılmıştır
1 input 1 output
Basit bir derin sinir ağları kullanan bir model oluşturmak. Sayı tahmin ettirmeye çalıştığım basit bir uygulama . Bu uygulamada görülen şey basit bir doğrusal veri çeşitlerinde başarılı denebilecek seviyede sonuçlar elde edilebilior ilk denememde 0 ile 100 arasındaki 1000 sayı ile modeli eğittiğimde 0 ile 100 arasındaki bir sayıyı tahmin etmesini istediğimde bana yüzde 0.1 in altındaki hata payı ile doğru çıktıları verebiliyor.
## 2 Sayının ortalamasını tahmin ettirme
2 input 1 output
Sequantial model kullanılmıştır
Sayi tahimini programının üzerine inşa edilmiş olup çok boyutlu inputlarda nasıl bir farklılık olduğunu göstermeyi amaçlar.
## 2 input 2 output
- Layerlarla daha ilk kez çalıştığım için bu gibi bilgiler benim için yeni. Normalde Sequantial modelde böyle bir şey yapmazsınız
- Çok basit bir şekilde tek göstermek istediğim 2 input ve 2 output nasıl verilir.

# Hedef Proje
En son yapmak istediğim proje. 3 Boyutlu bir düzlemde rasgele dağılmış X hedef noktaya minumum Y kabul noktası kullanarak birbirine bağlamak.
Bu projede ödül sistemi kullanmayı hedeflemekteyim.
Anlatacağım projeyi normal cpp kodu ile yapmış olduğumun altını çizmek isterim. Bu yazdığım kod Naive bir algoritma kullanır durumda bu algoritma ile bir veri seti oluşturmayı hedefliyorum. Bu kod daha sonra paylaşıcaktır. Hedef projeye başlandığı zaman.

## Bilmediklerim
- Bir model oluştururken nelere dikat etmeliyim.
- Bir veri seti oluşturuken nelere dikat etmeliyim.
- Hangi algoritmaları kullanabilirim.
- Hazır model kullanmak istersem var olan hazır modelleri nasıl bulabilrim ?
- Çok fazla başlık var. Hiç bir şey bilmediğini kabul edebilenlere selam olsun :)
 ## Kurallar
- Bir kabul noktası en fazla 3 hedef noktaya bağlanabilir.
- Bir kabul noktası bir hedef noktası ile aralarındaki mesafe maksimum 30 ise bağlanabilir
- Bir kabul noktası ile bağlanabileceği bir hedef noktası arasındaki mesafe ne kadar kısa ise o kadar yüksek bir puana sahip olacaktır.
- Daha az kabul noktası kullanmak her zaman daha yüksek puana sahip olacaktır.

# Kaynaklar
- https://keras.io/api/models/
- https://keras.io/api/layers/
- https://chat.openai.com/ (verdiği bilgiler her zaman doğru mu diye kontrol edilir yada edilecektir. Çok sıkı bir şekilde kullanılır her zaman yorumdan uzak net bilgiler sorulmaya özen gösterilir)

# İletişim
Her zaman ilk başta ana kaynak olan Kerasın dökümanları kullanılmalı
Projelerde bana destek olup bu repoyu herkesin yararlanabileceği bir repo haline getirmek ve bana bu yolculuğumda yardım etmek isterseniz lütfen iletişime geçin

Gmail: yildirimsamet051@gmail.com


# ENGLISH 
# Project Purpose and General Information
- As a first goal, I am trying to develop simple machine learning projects to learn the basics of machine learning.
- I would like to mention that this is my first venture into this subject. I acknowledge that I know nothing, and what I write may be completely nonsensical.
- If you are new to this topic, please review what I write in chronological order. Over time, this repository will be updated.
- Although what I write may seem completely illogical, it may be filled with misconceptions and mistakes that beginners will encounter. In such a case, I believe it will be a valuable resource for beginners after a certain time. 

# Models
## The Sequential Model
This can be considered the simplest model I will encounter.
The main advantage of this model is its simplicity in implementation. For a model to be simple, it requires:
- Not having multiple input sources
- Not having multiple output targets
- Not reusing layers (reusability) in other models
If the input comes from a single source, the output goes to a single destination, and the layers are not used in other models, we can say that the model is simple.
!!!! Information taken from https://www.datasciencearth.com/keras-model-wars-sequential-vs-functional/

#### Functions to Use in Layers
- I will list them later.

#### General Structure
- Input layer
- Hidden layers
- Output layer

This is the general structure.

# Implemented Applications
## Number Prediction
Sequential model is used.
1 input, 1 output.
Creating a model using simple deep neural networks. It is a simple application where I try to predict numbers. In this application, what is observed is that reasonably accurate results can be obtained in simple linear data types. In my first attempt, when I trained the model with 1000 numbers between 0 and 100 and asked it to predict a number between 0 and 100, it could provide accurate results with an error margin below 0.1%.

## Predicting the Average of 2 Numbers
2 inputs, 1 output.
Sequential model is used.
It is built on top of the Number Prediction program and aims to demonstrate the difference in multidimensional inputs.

## 2 inputs, 2 outputs
- Since I'm just starting to work with layers, this kind of information is new to me. Normally, you don't do something like this in a Sequential model.
- I just want to show in a very simple way how to provide 2 inputs and 2 outputs.

# Target Project
The latest project I want to work on is connecting randomly scattered X target points to a minimum of Y acceptance points on a 3D plane.
In this project, I aim to use a reward system.
I want to emphasize that the code I wrote is a Naive algorithm. I aim to create a dataset using this algorithm. This code will be shared later. When the target project starts.

## Things I Don't Know
- What should I pay attention to when creating a model?
- What should I pay attention to when creating a dataset?
- Which algorithms can I use?
- If I want to use a pre-trained model, how can I find existing pre-trained models?
- There are many topics. Greetings to those who can admit that they know nothing :)
 
## Rules
- One acceptance point can connect to a maximum of 3 target points.
- An acceptance point can be connected to a target point if the distance between them is a maximum of 30.
- The shorter the distance between an acceptance point and a target point, the higher the score.
- Using fewer acceptance

# Resources
- https://keras.io/api/models/
- https://keras.io/api/layers/
- https://chat.openai.com/ (Information obtained from here should always be verified for accuracy. It is used rigorously and precise questions are asked, avoiding ambiguity.)
# Contact
Always start by referring to the official documentation of Keras.
If you would like to support the projects and help turn this repository into a resource that everyone can benefit from, please feel free to contact me.
Gmail: yildirimsamet051@gmail.com

