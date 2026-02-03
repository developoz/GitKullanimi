#Git Kullanım Rehberi

#Temel Kavramlar#

Repository : Projenin tüm dosyalarının ve geçmişlerinin tutulduğu yerdir.

Commit : Kodun anlık durumunun kaydını almaktır. Commitler o an içinde kimin ne üzerinde değişiklik yaptığı bilgisini tutar. Ayrıca değişiklikerin tarih ve zaman bilgisini de tutar.

Branch : Ana Kodun bulunduğu hattan ayrı bir çalışma alanı oluşturmamızı sağlar. Bu sayede kodun ana halini bozmamızı engeller. Farklı özellikler ekleneceği zaman yeni branchlar açılıp orada çalışılabilir.

Merge : Farklı branchlardaki değişikliklerin main branch'e eklenemesi , değişiklikerin birleştirilmesi işlemidir.

*****
Olayı anlamak için projeyi iki parçala bölüyoruz. Lokal taraf ve Remote taraf. Lokal taraf bizim cihazımızdaki çalıştığımız kısımdır. Bu lokal kısmı da ikiye ayırabiliriz. Wokring Directory ve Lokal Repo. bu ikisi arasında ise Staging area var. Bu geçiş katmanı değişiklikleri commitlemeden önce eklediğimiz geçici alandır.
*****


#KOMUTLAR#

git init  ile lokal repo oluşturuyoruz.

git status ile dosyalarımız takip ediliyor mu bunu öğreniyoruz. staging area ya atılmış mı yoksa sadece workin directoryde  mı ona bakıyoruz.

git add <dosyaismi> veya git add . ile dosyaları working directory'den --> staging areaya göndermiş oluyoruz.


#Lokal Repoya kaydetme işlemi (Staging are --> Local Repo)

git commit -m "Commit Mesajı"