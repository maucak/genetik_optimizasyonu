**GENETİK ALGORİTMA PROJESİ - SENARYO 0**



Ad Soyad: Mehmet Ali Uçak Okul Numarası: 2312721050 Ders: BLG307 Yapay Zeka Sistemleri Dönem: 2025-2026 Güz



**PROJE TANIMI**

Bir lojistik firması, yeni akıllı deposunda raf yerleşim sistemini optimize etmek istiyor. Amaç, hem maliyeti 

düşürmek hem de taşıma verimini artırmak.



Problemde belirlenen amaç fonksiyonu şudur: y = 4x1 + 3x2 - 0.5x1x2



**KISITLAR VE CEZA YÖNTEMİ (PENALTY FUNCTION)** 

Problemin çözümünde bazı fiziksel sınırlar vardır. Kodlama yaparken bu sınırları aşan bireyleri tamamen elemek yerine, sınırdan ne kadar uzaklaştıklarına bağlı olarak puan kırılmıştır.



Toplam Alan Kısıtı: x1 + x2 değeri en fazla 8 olabilir. Eğer birey bu toplamı aşarsa, aştığı miktar 50 katsayısı ile çarpılıp puandan düşülür.



Derinlik Kısıtı: x2 değeri 1.5 metreden küçük olamaz. Eğer küçükse, aradaki fark yine 50 ile çarpılıp ceza olarak yansıtılır.



Bu yöntem sayesinde algoritma, sınırların dışına çıksa bile ceza sistemi ile tekrar belirtilen sınıra girmeyi öğrenir.



**ALGORİTMA DETAYLARI VE PARAMETRELER** 

Proje Python dilinde geliştirilmiştir. Numpy, Matplotlib ve Random kütüphaneleri kullanılmıştır.



Popülasyon Büyüklüğü: 50 birey.



Nesil Sayısı (İterasyon): 100 döngü.



Seçilim Yöntemi: Turnuva Seçimi . Rastgele seçilen 3 birey arasından en iyisi ebeveyn olarak seçilir.



Çaprazlama (Crossover): İki ebeveynin genlerinin ağırlıklı ortalaması alınarak yeni bireyler üretilir.



Mutasyon: Bireylerin genlerine -0.3 ile +0.3 arasında rastgele değerler eklenerek çeşitlilik sağlanır. Numpy clip fonksiyonu ile değerlerin \[2,6] ve \[1,4] aralığında kalması garanti edilir.



Elitizm: Her neslin en iyi bireyi hiç bozulmadan bir sonraki nesle doğrudan aktarılır.



**KODUN ÇALIŞTIRILMASI**

Kodun sonunda optimum x1 ve x2 değerleri ekrana yazdırılacak ve fitness değerinin değişimini gösteren bir grafik çizdirilecektir.



**SONUÇ** 

Algoritma çalıştırıldığında 100 nesil sonunda kısıtlara uygun en yüksek verim puanı elde edilmektedir. Grafik incelendiğinde fitness değerinin nesiller ilerledikçe arttığı ve belirli bir noktada en iyi çözüme yaklaştığı görülmektedir.

