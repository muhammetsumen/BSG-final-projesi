#### Bu dosyada algoritma 2-101 arasındaki 100 sayı ile üzerinde denenmiş ve sonuçlar paylaşılmıştır.

##### Devamında da algoritma bazı özel sayılar üzerinde denenerek istatistik sonuçları paylaşılmıştır.


### PROJE TEST SONUÇLARI ÖZETİ

| Test Grubu | Toplam Test | Başarılı (Dengeli) | Başarısız (Dengeli Değil) | Başarı Oranı |
| :--- | :---: | :---: | :---: | :---: |
| **Genel (2-101)** | 100 | 68 | 32 | **%68** |
| **Asal Sayılar** | 26 | 20 | 6 | **%76.9** |
| **2'nin Kuvvetleri** | 10 | 6 | 4 | **%60** |
| **Mersenne Sayıları** | 8 | 6 | 2 | **%75** |

**Genel Değerlendirme:** Algoritma asal sayılarda ve Mersenne sayılarında yüksek performans gösterirken, 60-80 aralığındaki sayılarda entropi kaybı yaşamıştır.



### Sonuçların Değerlendirilmesi:

Gözlem: 62-81 aralığında başarı oranında ciddi bir düşüş (%45) gözlemlendi. Özellikle Seed: 68 gibi sayılarda %90 oranında '0' üretildi.

Olası Sebep: Kullanılan 'Tohum' ve 'Tohum+1' (Anahtar) yöntemi, bazı sayı aralıklarında Collatz yörüngelerinin çok hızlı birleşmesine (convergence) veya paralel gitmesine neden oluyor olabilir. XOR işlemi benzer bitleri '0'a çevirdiği için, birbirine çok benzeyen yörüngeler aşırı '0' üretilmesine yol açmaktadır. İleride 'Tohum+1' yerine daha karmaşık bir anahtar türetme fonksiyonu (örneğin Seed * 3 + 7) kullanılması bu sorunu çözebilir."

Collatz Canavarı (27 Sayısı) Hakkında Not

"Not: Literatürde en uzun yörüngelerden birine sahip olan 27 sayısı, beklenenin aksine dengesiz bir dağılım vermiştir. Bu durum, Collatz yolunun uzunluğunun tek başına şifreleme kalitesini garantilemediğini, XOR işlemine giren iki sayının (27 ve 28) bit düzeyindeki ilişkisinin de kritik olduğunu göstermektedir."


### Aralık Bazlı Başarı Grafiği

```text
2-21   : [████████████████ ] %80
22-41  : [██████████████   ] %70
42-61  : [█████████████████] %85
62-81  : [█████████        ] %45 (Kritik Düşüş)
82-101 : [████████████     ] %60
```

# Log değerleri ve ara hesaplamalar:

aşağıda log değerleri, her 20 sayıda bir ara hesaplamalar ve bazı özel sayıların log değerleri ve başarı oranları verilmiştir.



Tohum Değeri Girin: 2



--- RAPOR (Tohum: 2 | Otomatik Anahtar: 3) ---

Şifre Dizisi: 10011100111001110011100111001110

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 3



--- RAPOR (Tohum: 3 | Otomatik Anahtar: 4) ---

Şifre Dizisi: 00100110110010011011001001101100

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 4



--- RAPOR (Tohum: 4 | Otomatik Anahtar: 5) ---

Şifre Dizisi: 11011101110111011101110111011101

0 Sayısı: 8 (%25.0)

1 Sayısı: 24 (%75.0)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 5



--- RAPOR (Tohum: 5 | Otomatik Anahtar: 6) ---

Şifre Dizisi: 11110010100111110010100111110010

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 6



--- RAPOR (Tohum: 6 | Otomatik Anahtar: 7) ---

Şifre Dizisi: 11010101111111100010110110001100

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 7



--- RAPOR (Tohum: 7 | Otomatik Anahtar: 8) ---

Şifre Dizisi: 11110110101010000000111001101100

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 8



--- RAPOR (Tohum: 8 | Otomatik Anahtar: 9) ---

Şifre Dizisi: 10011110101101111001100000001010

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 9



--- RAPOR (Tohum: 9 | Otomatik Anahtar: 10) ---

Şifre Dizisi: 00010111100100110110001001101100

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 10



--- RAPOR (Tohum: 10 | Otomatik Anahtar: 11) ---

Şifre Dizisi: 11101110001110111000111011100011

0 Sayısı: 12 (%37.5)

1 Sayısı: 20 (%62.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 11



--- RAPOR (Tohum: 11 | Otomatik Anahtar: 12) ---

Şifre Dizisi: 11001100101110001011100100000000

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 12



--- RAPOR (Tohum: 12 | Otomatik Anahtar: 13) ---

Şifre Dizisi: 00101010010101001010100101010010

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 13



--- RAPOR (Tohum: 13 | Otomatik Anahtar: 14) ---

Şifre Dizisi: 10110101110011011111000110000101

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 14



--- RAPOR (Tohum: 14 | Otomatik Anahtar: 15) ---

Şifre Dizisi: 01101110100101101110100101101110

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 15



--- RAPOR (Tohum: 15 | Otomatik Anahtar: 16) ---

Şifre Dizisi: 01101001100101101001100101101001

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 16



--- RAPOR (Tohum: 16 | Otomatik Anahtar: 17) ---

Şifre Dizisi: 10000101010110110011010000000011

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 17



--- RAPOR (Tohum: 17 | Otomatik Anahtar: 18) ---

Şifre Dizisi: 10010000001100110011000001110100

0 Sayısı: 20 (%62.5)

1 Sayısı: 12 (%37.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 18



--- RAPOR (Tohum: 18 | Otomatik Anahtar: 19) ---

Şifre Dizisi: 00100010110100001000101101000010

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 19



--- RAPOR (Tohum: 19 | Otomatik Anahtar: 20) ---

Şifre Dizisi: 00111000110011000100000110111011

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 20



--- RAPOR (Tohum: 20 | Otomatik Anahtar: 21) ---

Şifre Dizisi: 01100101100101100101100101100101

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 21



--- RAPOR (Tohum: 21 | Otomatik Anahtar: 22) ---

Şifre Dizisi: 00010110111100100001110101001111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------





### 2-21 arasındaki 20 tohum değeri algoritma kullanıldı 16 tanesi dengeli şekilde şifrelendi. Başarı oranı %80 olarak hesaplandı.



### !!!82-101 arasındaki değerlere kıyasla başarı oranı %20 YÜKSELDİ.!!!



Tohum Değeri Girin: 22



--- RAPOR (Tohum: 22 | Otomatik Anahtar: 23) ---

Şifre Dizisi: 11000010110110000101101100001011

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 23



--- RAPOR (Tohum: 23 | Otomatik Anahtar: 24) ---

Şifre Dizisi: 01001110101101001100101110000100

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 24



--- RAPOR (Tohum: 24 | Otomatik Anahtar: 25) ---

Şifre Dizisi: 10111000010101111011100001010111

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 25



--- RAPOR (Tohum: 25 | Otomatik Anahtar: 26) ---

Şifre Dizisi: 11101111000110001110111100011000

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 26



--- RAPOR (Tohum: 26 | Otomatik Anahtar: 27) ---

Şifre Dizisi: 11111111110011110111110011101100

0 Sayısı: 8 (%25.0)

1 Sayısı: 24 (%75.0)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 27



--- RAPOR (Tohum: 27 | Otomatik Anahtar: 28) ---

Şifre Dizisi: 00000100100100101010101101011000

0 Sayısı: 20 (%62.5)

1 Sayısı: 12 (%37.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 28



--- RAPOR (Tohum: 28 | Otomatik Anahtar: 29) ---

Şifre Dizisi: 11000110101011100011010101110001

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 29



--- RAPOR (Tohum: 29 | Otomatik Anahtar: 30) ---

Şifre Dizisi: 00001010101010000101010101000010

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 30



--- RAPOR (Tohum: 30 | Otomatik Anahtar: 31) ---

Şifre Dizisi: 00011101010001000101100111010011

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 31



--- RAPOR (Tohum: 31 | Otomatik Anahtar: 32) ---

Şifre Dizisi: 11010100101100111001000110100111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 32



--- RAPOR (Tohum: 32 | Otomatik Anahtar: 33) ---

Şifre Dizisi: 10011110001010000011010100011110

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 33



--- RAPOR (Tohum: 33 | Otomatik Anahtar: 34) ---

Şifre Dizisi: 00111011111111001100000001001100

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 34



--- RAPOR (Tohum: 34 | Otomatik Anahtar: 35) ---

Şifre Dizisi: 11000110011100011001110001100111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 35



--- RAPOR (Tohum: 35 | Otomatik Anahtar: 36) ---

Şifre Dizisi: 00100110001111000101110011111100

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 36



--- RAPOR (Tohum: 36 | Otomatik Anahtar: 37) ---

Şifre Dizisi: 01111111011111101111111011111101

0 Sayısı: 5 (%15.6)

1 Sayısı: 27 (%84.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 37



--- RAPOR (Tohum: 37 | Otomatik Anahtar: 38) ---

Şifre Dizisi: 11111111011110111111111011110111

0 Sayısı: 4 (%12.5)

1 Sayısı: 28 (%87.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 38



--- RAPOR (Tohum: 38 | Otomatik Anahtar: 39) ---

Şifre Dizisi: 01000000111001110010100101011100

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 39



--- RAPOR (Tohum: 39 | Otomatik Anahtar: 40) ---

Şifre Dizisi: 10010000010111000000000111110101

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 40



--- RAPOR (Tohum: 40 | Otomatik Anahtar: 41) ---

Şifre Dizisi: 10010101011010111111111110101100

0 Sayısı: 11 (%34.4)

1 Sayısı: 21 (%65.6)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 41



--- RAPOR (Tohum: 41 | Otomatik Anahtar: 42) ---

Şifre Dizisi: 01100101010111101001010000101100

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------





### 22-41 arasındaki 20 tohum değeri üzerinde algoritma kullanıldı 14 tanesi dengeli şekilde şifrelendi. Başarı oranı %70 olarak hesaplandı.
 

### !!!2-21 Arasındaki değerlere kıyasla başarı oranı %10 DÜŞTÜ.!!!



Tohum Değeri Girin: 42



--- RAPOR (Tohum: 42 | Otomatik Anahtar: 43) ---

Şifre Dizisi: 11110010010111101001101100001101

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 43



--- RAPOR (Tohum: 43 | Otomatik Anahtar: 44) ---

Şifre Dizisi: 00111110011000000111001000011000

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 44



--- RAPOR (Tohum: 44 | Otomatik Anahtar: 45) ---

Şifre Dizisi: 11111101100111111101100111111101

0 Sayısı: 7 (%21.9)

1 Sayısı: 25 (%78.1)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 45



--- RAPOR (Tohum: 45 | Otomatik Anahtar: 46) ---

Şifre Dizisi: 10101110100110101110100110101110

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 46



--- RAPOR (Tohum: 46 | Otomatik Anahtar: 47) ---

Şifre Dizisi: 00010111111110111111111100110110

0 Sayısı: 9 (%28.1)

1 Sayısı: 23 (%71.9)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 47



--- RAPOR (Tohum: 47 | Otomatik Anahtar: 48) ---

Şifre Dizisi: 00101111000101011001011001110111

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 48



--- RAPOR (Tohum: 48 | Otomatik Anahtar: 49) ---

Şifre Dizisi: 00111101010010010101010011000001

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 49



--- RAPOR (Tohum: 49 | Otomatik Anahtar: 50) ---

Şifre Dizisi: 01100010110100111011000101101001

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 50



--- RAPOR (Tohum: 50 | Otomatik Anahtar: 51) ---

Şifre Dizisi: 10010110110110111100101101101101

0 Sayısı: 12 (%37.5)

1 Sayısı: 20 (%62.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 51



--- RAPOR (Tohum: 51 | Otomatik Anahtar: 52) ---

Şifre Dizisi: 00000111000000101110110010110110

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 52



--- RAPOR (Tohum: 52 | Otomatik Anahtar: 53) ---

Şifre Dizisi: 11001100111001100111001100111001

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 53



--- RAPOR (Tohum: 53 | Otomatik Anahtar: 54) ---

Şifre Dizisi: 11010100001110011001100011011010

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 54



--- RAPOR (Tohum: 54 | Otomatik Anahtar: 55) ---

Şifre Dizisi: 00000011111001100110011111001000

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 55



--- RAPOR (Tohum: 55 | Otomatik Anahtar: 56) ---

Şifre Dizisi: 00000111110011001001111101100111

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 56



--- RAPOR (Tohum: 56 | Otomatik Anahtar: 57) ---

Şifre Dizisi: 00101111111001101011010101000101

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 57



--- RAPOR (Tohum: 57 | Otomatik Anahtar: 58) ---

Şifre Dizisi: 11110010101011000010011111110001

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 58



--- RAPOR (Tohum: 58 | Otomatik Anahtar: 59) ---

Şifre Dizisi: 11111001001001000011000010010100

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 59



--- RAPOR (Tohum: 59 | Otomatik Anahtar: 60) ---

Şifre Dizisi: 01011001000111011110010011011000

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 60



--- RAPOR (Tohum: 60 | Otomatik Anahtar: 61) ---

Şifre Dizisi: 10110000110000101100001100001011

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 61



--- RAPOR (Tohum: 61 | Otomatik Anahtar: 62) ---

Şifre Dizisi: 11100011110100110101101001001100

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------





### 42-61 arasındaki 20 tohum değeri algoritma kullanıldı 17 tanesi dengeli şekilde şifrelendi. Başarı oranı %85 olarak hesaplandı.

 

### !!!22-41 arasındaki değerlere kıyasla başarı oranı %15 YÜKSELDİ.!!!



Tohum Değeri Girin: 62



--- RAPOR (Tohum: 62 | Otomatik Anahtar: 63) ---

Şifre Dizisi: 00100001010010100101001011000100

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 63



--- RAPOR (Tohum: 63 | Otomatik Anahtar: 64) ---

Şifre Dizisi: 11011000010111111110000111111011

0 Sayısı: 11 (%34.4)

1 Sayısı: 21 (%65.6)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 64



--- RAPOR (Tohum: 64 | Otomatik Anahtar: 65) ---

Şifre Dizisi: 01011000010001000000101010001110

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 65



--- RAPOR (Tohum: 65 | Otomatik Anahtar: 66) ---

Şifre Dizisi: 00001000011111100110000100001111

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 66



--- RAPOR (Tohum: 66 | Otomatik Anahtar: 67) ---

Şifre Dizisi: 11110101010111100111111010101011

0 Sayısı: 10 (%31.2)

1 Sayısı: 22 (%68.8)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 67



--- RAPOR (Tohum: 67 | Otomatik Anahtar: 68) ---

Şifre Dizisi: 10011110011100000110010111010000

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 68



--- RAPOR (Tohum: 68 | Otomatik Anahtar: 69) ---

Şifre Dizisi: 01000000000010000000000100000000

0 Sayısı: 29 (%90.6)

1 Sayısı: 3 (%9.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 69



--- RAPOR (Tohum: 69 | Otomatik Anahtar: 70) ---

Şifre Dizisi: 00000010110000000101100000001011

0 Sayısı: 23 (%71.9)

1 Sayısı: 9 (%28.1)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 70



--- RAPOR (Tohum: 70 | Otomatik Anahtar: 71) ---

Şifre Dizisi: 00111001010010101011000001100011

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 71



--- RAPOR (Tohum: 71 | Otomatik Anahtar: 72) ---

Şifre Dizisi: 01011111100110111100011110101011

0 Sayısı: 11 (%34.4)

1 Sayısı: 21 (%65.6)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 72



--- RAPOR (Tohum: 72 | Otomatik Anahtar: 73) ---

Şifre Dizisi: 01011100011001100100010101011111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 73



--- RAPOR (Tohum: 73 | Otomatik Anahtar: 74) ---

Şifre Dizisi: 11111010101001110110011000111111

0 Sayısı: 11 (%34.4)

1 Sayısı: 21 (%65.6)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 74



--- RAPOR (Tohum: 74 | Otomatik Anahtar: 75) ---

Şifre Dizisi: 10001111111100011010001010010100

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 75



--- RAPOR (Tohum: 75 | Otomatik Anahtar: 76) ---

Şifre Dizisi: 00101001010100101000111111100110

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 76



--- RAPOR (Tohum: 76 | Otomatik Anahtar: 77) ---

Şifre Dizisi: 11101111111101011110111111110101

0 Sayısı: 6 (%18.8)

1 Sayısı: 26 (%81.2)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 77



--- RAPOR (Tohum: 77 | Otomatik Anahtar: 78) ---

Şifre Dizisi: 00010001000110000100000010100110

0 Sayısı: 23 (%71.9)

1 Sayısı: 9 (%28.1)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 78



--- RAPOR (Tohum: 78 | Otomatik Anahtar: 79) ---

Şifre Dizisi: 11001011111011111111011111001011

0 Sayısı: 8 (%25.0)

1 Sayısı: 24 (%75.0)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 79



--- RAPOR (Tohum: 79 | Otomatik Anahtar: 80) ---

Şifre Dizisi: 01101100111011100001100101101100

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 80



--- RAPOR (Tohum: 80 | Otomatik Anahtar: 81) ---

Şifre Dizisi: 10011001011000111001100101100011

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 81



--- RAPOR (Tohum: 81 | Otomatik Anahtar: 82) ---

Şifre Dizisi: 00100000010011111010001101101100

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------





### 62-81 arasındaki 20 tohum değeri algoritma kullanıldı 9 tanesi dengeli şekilde şifrelendi. Başarı oranı %45 olarak hesaplandı.
  

### !!!42-61 arasındaki değerlere kıyasla başarı oranı %40 DÜŞTÜ!!!


Tohum Değeri Girin: 82



--- RAPOR (Tohum: 82 | Otomatik Anahtar: 83) ---

Şifre Dizisi: 11010000111010011001011100001111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 83



--- RAPOR (Tohum: 83 | Otomatik Anahtar: 84) ---

Şifre Dizisi: 00011100001101011111100011110100

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 84



--- RAPOR (Tohum: 84 | Otomatik Anahtar: 85) ---

Şifre Dizisi: 11000001110000011100000111000001

0 Sayısı: 20 (%62.5)

1 Sayısı: 12 (%37.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 85



--- RAPOR (Tohum: 85 | Otomatik Anahtar: 86) ---

Şifre Dizisi: 11000100011100000010111100101010

0 Sayısı: 18 (%56.2)

1 Sayısı: 14 (%43.8)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 86



--- RAPOR (Tohum: 86 | Otomatik Anahtar: 87) ---

Şifre Dizisi: 00010000000001011010000010000000

0 Sayısı: 26 (%81.2)

1 Sayısı: 6 (%18.8)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 87



--- RAPOR (Tohum: 87 | Otomatik Anahtar: 88) ---

Şifre Dizisi: 01110110010100010001111100001111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 88



--- RAPOR (Tohum: 88 | Otomatik Anahtar: 89) ---

Şifre Dizisi: 10101100010110001000100010001011

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 89



--- RAPOR (Tohum: 89 | Otomatik Anahtar: 90) ---

Şifre Dizisi: 11000101000100011011101000110000

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 90



--- RAPOR (Tohum: 90 | Otomatik Anahtar: 91) ---

Şifre Dizisi: 01110011011000010110111110111000

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 91



--- RAPOR (Tohum: 91 | Otomatik Anahtar: 92) ---

Şifre Dizisi: 10000001111100100110011011101001

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 92



--- RAPOR (Tohum: 92 | Otomatik Anahtar: 93) ---

Şifre Dizisi: 01000010101010100001010101010000

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 93



--- RAPOR (Tohum: 93 | Otomatik Anahtar: 94) ---

Şifre Dizisi: 11011101010000100101100111100011

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 94



--- RAPOR (Tohum: 94 | Otomatik Anahtar: 95) ---

Şifre Dizisi: 00011000011100000000111000111000

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 95



--- RAPOR (Tohum: 95 | Otomatik Anahtar: 96) ---

Şifre Dizisi: 11010010101100110001000110000111

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 96



--- RAPOR (Tohum: 96 | Otomatik Anahtar: 97) ---

Şifre Dizisi: 11000111100111101011111111111110

0 Sayısı: 8 (%25.0)

1 Sayısı: 24 (%75.0)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 97



--- RAPOR (Tohum: 97 | Otomatik Anahtar: 98) ---

Şifre Dizisi: 11001011111000111001111000010110

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 98



--- RAPOR (Tohum: 98 | Otomatik Anahtar: 99) ---

Şifre Dizisi: 00110100101000100100110100101000

0 Sayısı: 20 (%62.5)

1 Sayısı: 12 (%37.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 99



--- RAPOR (Tohum: 99 | Otomatik Anahtar: 100) ---

Şifre Dizisi: 00010101110011100100010101110011

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 100



--- RAPOR (Tohum: 100 | Otomatik Anahtar: 101) ---

Şifre Dizisi: 11001111110001100111001111110001

0 Sayısı: 12 (%37.5)

1 Sayısı: 20 (%62.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 101



--- RAPOR (Tohum: 101 | Otomatik Anahtar: 102) ---

Şifre Dizisi: 10001111111010100110001111111010

0 Sayısı: 12 (%37.5)

1 Sayısı: 20 (%62.5)

DURUM: Dengesiz

---------------------------------------------





### 82-101 arasındaki 20 tohum değeri algoritma kullanıldı 12 tanesi dengeli şekilde şifrelendi. Başarı oranı %60 olarak hesaplandı.



### !!!62-81 arasındaki değerlere kıyasla başarı oranı %15 YÜKSELDİ.!!!



### 2-101 arasındaki 100 tohum değerinin 68 tanesi dengeli şekilde şifrelendi.  Başarı oranı %68 olarak hesaplandı.







# ALGORİTMANIN BAZI ÖZEL SAYILAR ÜZERİNDEKİ BAŞARI ORANLARI 


# Asal sayılar: 


### !!!2-101 arasındaki 26 asal sayının 20 tanesi dengeli bir dağılım göstererek başarılı oldu. Asal sayılar üzerinde başarı oranı %76,9 olarak hesaplandı!!!





# 2nin katları olan sayılar:


### bu sayılar sürekli ikiye bölünerek çok hızlı şekilde 1 değerine ulaşır ve hep çift sayı üretirler. Bu sayıları başarılı şekilde şifreleyebilirse algoritmayı başarılı sayabilirim.



Tohum Değeri Girin: 2



--- RAPOR (Tohum: 2 | Otomatik Anahtar: 3) ---

Şifre Dizisi: 10011100111001110011100111001110

0 Sayısı: 13 (%40.6)

1 Sayısı: 19 (%59.4)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 4



--- RAPOR (Tohum: 4 | Otomatik Anahtar: 5) ---

Şifre Dizisi: 11011101110111011101110111011101

0 Sayısı: 8 (%25.0)

1 Sayısı: 24 (%75.0)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 8



--- RAPOR (Tohum: 8 | Otomatik Anahtar: 9) ---

Şifre Dizisi: 10011110101101111001100000001010

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 16



--- RAPOR (Tohum: 16 | Otomatik Anahtar: 17) ---

Şifre Dizisi: 10000101010110110011010000000011

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 32



--- RAPOR (Tohum: 32 | Otomatik Anahtar: 33) ---

Şifre Dizisi: 10011110001010000011010100011110

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 64



--- RAPOR (Tohum: 64 | Otomatik Anahtar: 65) ---

Şifre Dizisi: 01011000010001000000101010001110

0 Sayısı: 21 (%65.6)

1 Sayısı: 11 (%34.4)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 128



--- RAPOR (Tohum: 128 | Otomatik Anahtar: 129) ---

Şifre Dizisi: 00101101011100101011010011111010

0 Sayısı: 14 (%43.8)

1 Sayısı: 18 (%56.2)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 256



--- RAPOR (Tohum: 256 | Otomatik Anahtar: 257) ---

Şifre Dizisi: 01011111111011000111110000101011

0 Sayısı: 12 (%37.5)

1 Sayısı: 20 (%62.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 512



--- RAPOR (Tohum: 512 | Otomatik Anahtar: 513) ---

Şifre Dizisi: 01010101100100001010000110001010

0 Sayısı: 20 (%62.5)

1 Sayısı: 12 (%37.5)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 1024



--- RAPOR (Tohum: 1024 | Otomatik Anahtar: 1025) ---

Şifre Dizisi: 10101010011000011101100010101110

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------





### 10 değerin 6 tanesi dengeli bir dağılımla şifreledi. Başarı oranı %60 olarak hesaplandı.





# Mersenne sayılar(Binarysi sadece 1 olan sayılar):



Tohum Değeri Girin: 15



--- RAPOR (Tohum: 15 | Otomatik Anahtar: 16) ---

Şifre Dizisi: 01101001100101101001100101101001

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 31



--- RAPOR (Tohum: 31 | Otomatik Anahtar: 32) ---

Şifre Dizisi: 11010100101100111001000110100111

0 Sayısı: 15 (%46.9)

1 Sayısı: 17 (%53.1)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 63



--- RAPOR (Tohum: 63 | Otomatik Anahtar: 64) ---

Şifre Dizisi: 11011000010111111110000111111011

0 Sayısı: 11 (%34.4)

1 Sayısı: 21 (%65.6)

DURUM: Dengesiz

---------------------------------------------



Tohum Değeri Girin: 127



--- RAPOR (Tohum: 127 | Otomatik Anahtar: 128) ---

Şifre Dizisi: 11110101000000100110110101100011

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 255



--- RAPOR (Tohum: 255 | Otomatik Anahtar: 256) ---

Şifre Dizisi: 01111110100010011010011000010001

0 Sayısı: 17 (%53.1)

1 Sayısı: 15 (%46.9)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 511



--- RAPOR (Tohum: 511 | Otomatik Anahtar: 512) ---

Şifre Dizisi: 11111011010100100010010001000111

0 Sayısı: 16 (%50.0)

1 Sayısı: 16 (%50.0)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 1023



--- RAPOR (Tohum: 1023 | Otomatik Anahtar: 1024) ---

Şifre Dizisi: 11011111100000000001000010100011

0 Sayısı: 19 (%59.4)

1 Sayısı: 13 (%40.6)

DURUM: >> DENGELİ << (Başarılı)

---------------------------------------------



Tohum Değeri Girin: 2047



--- RAPOR (Tohum: 2047 | Otomatik Anahtar: 2048) ---

Şifre Dizisi: 11111111111100111111001100101010

0 Sayısı: 9 (%28.1)

1 Sayısı: 23 (%71.9)

DURUM: Dengesiz

---------------------------------------------

### 8 değerin 6 tanesi dengeli bir dağılımla şifreledi. Başarı oranı %75 olarak hesaplandı.
























































