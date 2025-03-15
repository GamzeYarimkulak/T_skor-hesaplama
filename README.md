 # Sınav Not Değerlendirme Sistemi

Bu proje, öğrencilerin sınav sonuçlarını analiz eden bir C programıdır. Öğrencilerin cevaplarını rastgele oluşturarak sınav sonuçlarını değerlendirir ve başarı durumlarını hesaplar.

## Özellikler
- **Cevap Anahtarı Üretme:** Rastgele bir cevap anahtarı oluşturur.
- **Öğrenci Cevapları Üretme:** Öğrencilerin cevaplarını belirli ihtimallere göre simüle eder.
- **Sınav Puanlama:** Öğrencilerin doğru, yanlış ve boş cevaplarına göre puan hesaplar.
- **Sınıf Ortalaması ve Standart Sapma Hesaplama:** Sınıfın genel başarı durumunu analiz eder.
- **Harf Notu Hesaplama:** Öğrencilerin T-skoruna dayalı harf notlarını belirler.

## Kurulum ve Çalıştırma

### Gereksinimler
- **C Derleyicisi:** GCC veya Dev-C++ gibi bir derleyici
- **İşletim Sistemi:** Windows, Linux veya macOS

### Derleme ve Çalıştırma
1. **Kaynak kodunu klonlayın:**
   ```sh
   git clone https://github.com/GamzeYarimkulak/SinavDegerlendirme.git
   cd SinavDegerlendirme
   ```
2. **Programı derleyin:**
   ```sh
   gcc -o sinav main.c -lm
   ```
3. **Programı çalıştırın:**
   ```sh
   ./sinav
   ```

## Kullanım
Program çalıştırıldığında kullanıcıdan şu bilgileri ister:
- **Öğrenci Sayısı**: 1 ile 100 arasında bir değer girilmelidir.
- **Soru Sayısı**: 1 ile 100 arasında bir değer girilmelidir.
- **Boş bırakma ihtimali**: 0.0 ile 1.0 arasında bir oran.
- **Doğru cevaplama ihtimali**: 0.0 ile 1.0 arasında bir oran.

Öğrencilerin cevapları rastgele oluşturulduktan sonra program:
- Cevap anahtarını ekrana yazdırır.
- Her öğrencinin cevaplarını listeler.
- Puanları hesaplayarak öğrencilerin notlarını gösterir.
- Sınıf ortalaması ve başarı durumunu analiz eder.

## Örnek Çıktı
```
Ogrenci sayisini giriniz (MAX 100, MIN 1): 5
Soru sayisini giriniz (MAX 100, MIN 1): 10
Herhangi bir sorunun bos birakilma ihtimalini giriniz: (0.0 ~ 1.0): 0.2
Herhangi bir sorunun dogru cevaplanma ihtimalini giriniz: (0.0 ~ 1.0): 0.7

CEVAP ANAHTARI:
001:A | 002:C | 003:B | 004:D | 005:A | 006:E | 007:C | 008:B | 009:D | 010:E |

001. Ogrencinin HBN: 85.00 T-skoru: 60.5, harf notu: BB
002. Ogrencinin HBN: 72.50 T-skoru: 57.2, harf notu: CC
...
```

## Dosya Yapısı
```
📂 SinavDegerlendirme
 ├── 📄 main.c        # Programın ana dosyası
 ├── 📄 README.md     # Proje açıklaması
 ├── 📄 LICENSE       # Lisans bilgileri
```
