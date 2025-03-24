/// Metro Ağı Projesi Bu proje, bir metro ağındaki istasyonlar ve hatlar arasındaki bağlantıları modelleyerek, en az aktarmalı ve en hızlı rotayı bulma işlevselliklerini sağlamaktadır. Python kullanarak, BFS (Breadth-First Search) ve A (A-star)* algoritmalarını kullanarak iki farklı rota bulma yöntemi geliştirilmiştir.

Proje Yapısı Bu proje, aşağıdaki temel sınıfları ve işlevleri içerir:

1 ) Istasyon: Bir metro istasyonunun bilgilerini (isim, hat, komşu istasyonlar) saklar.

2 ) MetroAgi: Metro ağını modelleyen sınıf. İstasyonlar ve hatlar arasındaki bağlantıları yönetir ve rotaları hesaplar.

istasyon_ekle: Yeni bir istasyon ekler.

baglanti_ekle: İki istasyon arasında bağlantı ekler.

en_az_aktarma_bul: BFS algoritmasını kullanarak, başlangıç ve hedef istasyonu arasındaki en az aktarmalı rotayı bulur.

en_hizli_rota_bul: A* algoritmasını kullanarak, başlangıç ve hedef istasyonu arasındaki en hızlı rotayı bulur.

Algoritmalar

BFS (Breadth-First Search) BFS, graf üzerindeki en kısa yolu bulmak için kullanılan bir algoritmadır. Bu projede, en az aktarma ile rotayı bulmak için BFS kullanılmıştır. BFS, her istasyonu sırayla keşfeder ve en kısa yolu bulur.

A* (A-star) A* algoritması, en hızlı rotayı bulmak için kullanılan gelişmiş bir algoritmadır. A* algoritması, hedefe en hızlı ulaşan yolu bulmak için bir "öncelik kuyruğu" kullanır. Bu algoritma, toplam süreyi dikkate alarak daha verimli bir rota bulur.

Kullanım

MetroAgi Sınıfını Kullanma Metro ağını oluşturmak için MetroAgi sınıfından bir nesne oluşturabilirsiniz. İstasyonlar eklemek için istasyon_ekle, istasyonlar arasındaki bağlantıları eklemek için ise baglanti_ekle fonksiyonlarını kullanabilirsiniz. /// metro = MetroAgi()
Kırmızı Hat'tan istasyonlar ekleme
metro.istasyon_ekle("K1", "Kızılay", "Kırmızı Hat") metro.istasyon_ekle("K2", "Ulus", "Kırmızı Hat") metro.istasyon_ekle("K3", "Demetevler", "Kırmızı Hat") metro.istasyon_ekle("K4", "OSB", "Kırmızı Hat")

Bağlantılar ekleme
metro.baglanti_ekle("K1", "K2", 4) metro.baglanti_ekle("K2", "K3", 6) metro.baglanti_ekle("K3", "K4", 8)

/// 2. Rota Bulma İki farklı rota bulma yöntemi mevcuttur:

En Az Aktarmalı Rota (BFS): Başlangıç ve hedef istasyonları arasındaki en az aktarmalı rotayı bulmak için en_az_aktarma_bul fonksiyonu kullanılabilir. /// rota = metro.en_az_aktarma_bul("M1", "K4") if rota: print("En az aktarmalı rota:", " -> ".join(i.ad for i in rota)) /// En Hızlı Rota (A*): Başlangıç ve hedef istasyonları arasındaki en hızlı rotayı bulmak için en_hizli_rota_bul fonksiyonu kullanılabilir. /// sonuc = metro.en_hizli_rota_bul("M1", "K4") if sonuc: rota, sure = sonuc print(f"En hızlı rota ({sure} dakika):", " -> ".join(i.ad for i in rota)) /// Test Senaryoları Proje, üç farklı senaryoya göre rota hesaplamalarını test eder:

AŞTİ'den OSB'ye: Mavi Hat ve Kırmızı Hat kullanılarak en az aktarmalı ve en hızlı rotalar bulunur.

Batıkent'ten Keçiören'e: Turuncu Hat kullanılarak en az aktarmalı ve en hızlı rotalar bulunur.

Keçiören'den AŞTİ'ye: Turuncu Hat ve Mavi Hat kullanılarak en az aktarmalı ve en hızlı rotalar bulunur.

Kurulum ve Gereksinimler Gereksinimler Bu projeyi çalıştırmak için Python 3.x gereklidir. Ayrıca, projenin çalışması için herhangi bir ek kütüphane gereksinimi yoktur, çünkü sadece Python'un standart kütüphaneleri kullanılmıştır.

Çalıştırma

Python 3.x'i sisteminize yükleyin.

Proje dosyalarını indirin.

Aşağıdaki komutla projeyi çalıştırın: /// python metro_agi.py

/// Bu komut, örnek kullanım ve test senaryolarıyla birlikte metro ağına dair hesaplamaları yapacak ve sonuçları ekrana yazdıracaktır.

Katkı Sağlama Eğer bu projeye katkıda bulunmak isterseniz, aşağıdaki adımları takip edebilirsiniz:

Bu projeyi kendi GitHub hesabınıza fork'layın.

Yeni bir branch oluşturun.

Yapmak istediğiniz değişiklikleri yapın.

Pull request gönderin. ///
