# Sınav Sonuç Değerlendirme Programı

Bu program, öğrenci sınav cevaplarını değerlendirerek harf notlarını hesaplayan bir sistemdir. Öğrenci sayısı, soru sayısı ve belirli olasılık değerleri (boş bırakma ve doğru cevaplama ihtimalleri) kullanıcıdan alınarak simüle edilmiş sınav sonuçları oluşturulur.

## 📌 Özellikler
✅ Rastgele cevap anahtarı üretimi  
✅ Öğrencilerin rastgele sınav cevaplarının üretilmesi  
✅ Öğrencilerin cevaplarının değerlendirilmesi  
✅ Sınıf ortalaması ve standart sapmanın hesaplanması  
✅ T-skoru hesaplama ve harf notu ataması  

## 🚀 Kurulum ve Çalıştırma
Program, **Dev-C++ 5.11 TDM-GCC 4.9.2** kullanılarak geliştirilmiştir ve **Windows 10 64-bit** sistemde test edilmiştir. Çalıştırmak için:

1. **GCC veya Dev-C++** kullanarak `main.c` dosyasını derleyin:
   ```sh
   gcc main.c -o sinav
Çalıştırın:
sh
Kopyala
Düzenle
./sinav
Program aşağıdaki bilgileri isteyecektir:
Öğrenci sayısı (1-100 arasında)
Soru sayısı (1-100 arasında)
Boş bırakma olasılığı (0.0 - 1.0 arasında)
Doğru cevaplama olasılığı (0.0 - 1.0 arasında)
Çıktıları ekranda görebilirsiniz.
⚙️ Kullanılan Fonksiyonlar
Fonksiyon	Açıklama
void cevap_anahtari_uret(char cevap_anahtari[], int S);	Rastgele cevap anahtarı üretir.
void sinavi_uygula(char ogrenci_cevaplari[][100], char cevap_anahtari[], int N, int S, double B, double D);	Öğrenci cevaplarını üretir.
void ogrencileri_puanla(char ogrenci_cevaplari[][100], char cevap_anahtari[], double HBN[], int N, int S);	Öğrencileri puanlandırır.
double sinif_ortalamasi_hesapla(double HBN[], int N);	Sınıf ortalamasını hesaplar.
double standart_sapma_hesapla(double ortalama, double HBN[], int N);	Standart sapmayı hesaplar.
void T_skoru_hesapla(double ortalama, double HBN[], int N, double std, double T_skoru[]);	T-skoru hesaplar.
char * harf_notu(double t_puan, double harf_notlari[]);	Harf notu belirler.
📝 Örnek Çıktı
yaml
Kopyala
Düzenle
Ogrenci sayisini giriniz (MAX 100, MIN 1): 5
Soru sayisini giriniz (MAX 100, MIN 1): 10
Herhangi bir sorunun bos birakilma ihtimalini giriniz: (0.0 ~ 1.0): 0.2
Herhangi bir sorunun dogru cevaplanma ihtimalini giriniz: (0.0 ~ 1.0): 0.5

CEVAP ANAHTARI: 
001:A | 002:C | 003:B | 004:D | 005:E | ...

001. Ogrencinin cevaplari: 
001:A | 002:X | 003:C | 004:B | 005:E | ...

Sinif ortalamasi: 65.40, Standart sapma: 10.24
Sinif duzeyi: Cok iyi

Ogrenci notlari:
001. ogrencinin HBN: 72.50, T-skoru: 63.20, harf notu: BB
002. ogrencinin HBN: 55.00, T-skoru: 56.80, harf notu: CC
...
🛠 Gereksinimler
C derleyicisi (GCC veya Dev-C++)
Windows 10 veya Linux uyumlu çalışma ortamı
