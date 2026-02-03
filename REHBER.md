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

git add . ile bulunulan dizindeki ve alt dizinlerdeki tüm değişikleri ekleriz.
git add -A ile ise dizin farketmeksizin repodaki tüm değişikleri tamamen ekleyebiliriz.


#Lokal Repoya kaydetme işlemi (Staging are --> Local Repo)

git commit -m "Commit Mesajı"


#Son oluşturduğum commit'i görmek için

git show   komutu kullanılır.


#Tüm commitleri görmek için

git log   komutu kullanılır. Ayrıca git log --oneline ile daha temiz ve düzenli bir
kayıt geçmişi görmek mümkün.


#Son 2 commiti görmek için , 

git log -p -2    ile son 2 commit geçmişini görebiliriz.




#Staging area’daki bir dosyayı tekrar çalışma dizinine almak (unstage yapmak)

git restore --staged dosya_adi


#Çalışma dizinindeki değişiklikleri geri almak (değişiklikleri silmek)

git restore dosya_adi


#Yapılan Commit'i iptal etme (Hatalı committe yapılan işlemin tam tersini yapan bir commit oluşturuyor. )

git revert commit_id



#Reset Yöntemleri(soft,mixed,hard)

soft  : tüm commitler iptal oluyor tekrar staging areaya atıyor.
mixed : lokal repodaki commit leri iptal edip working directorye atarım diyor.
hard(RİSKLİ!!) :  bütün commitleri siler hiçbir yere koymaz direkt yok eder. geri erişilemez.



#Branch Konusu : ana koddan bağımsız olarak farklı bir çalışma alanı açarak orada özel olarak görev çalışmaları yapılabilir. ve buradaki çalışmaları yaparken ana kodu(main) branchini bozmadan çalışmaya imkan tanır. daha sonra da istenirse çalışma branchindeki yenilikler main branch e eklenebilir.

#Yeni branch oluşturmak 

git branch yeni_branch

#Yeni branch'e geçiş yapmak

git checkout yeni_branch

#Branchleri ve bizim hangi branchde olduğumuzu görmek için

git branch -a


#Branchi merge etmek için

git merge yeni_branch