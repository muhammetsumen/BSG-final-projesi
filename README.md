# BSG-final-projesi

# Algoritma Mantığının Açıklaması  
Collatz yanılgısı kullanılarak dengeli ve çözülmesi zor bir rastgele sayı üreteci algoritması tasarlıyorum
Proje Başlığı: Collatz Cipher (CC-Encryption)

Özet: Bu proje, matematiksel bir problem olan Collatz (3n+1) dizisini kullanarak rastgele sayı üretimi (PRNG) ve şifreleme anahtarı oluşturmayı amaçlar. Standart Collatz dizisindeki "tahmin edilebilirlik" (tek sayıdan sonra çift gelme zorunluluğu) ve "bit dengesizliği" sorunları, özel bir algoritma ve XOR manipülasyonu ile çözülmüştür.

Algoritma Mantığı:
   Zorunlu Adım Atlama (Skip Logic): Collatz dizisinde  $n$  tek ise  ($3n+1$)  sonuç daima çifttir. Bu, şifrede %100 tahmin edilebilirlik yaratır. Algoritmamız, tek sayı işleminden sonraki zorunlu çift adımı atlayarak entropiyi artırır.
   
Çift Akış (Dual Stream): 
   Akış A: Kullanıcının girdiği tohumdan üretilir.
   Akış B: Gizli bir anahtar sayıdan üretilir ve ters çevrilir.
   
Anahtar Değer: Algoritmada anahtar değer önceden seçilen bir değer değildir. Girilen tohum değeri $n$ ise $n+1$ değeri anahtar değer olacaktır.  
   
Karıştırma (Diffusion): İki akış XOR işlemine sokularak bitlerin homojen dağılması (0 ve 1 dengesi) sağlanır.


# Algoritmanın Sözde (Pseudo) Kodu

```text
BAŞLA

FONKSİYON SmartCollatz(sayı, uzunluk):
    Dizi = []
    DÖNGÜ (Dizi uzunluğu < hedef_uzunluk) VE (sayı > 1):
        EĞER sayı TEK ise:
            sayı = (3 * sayı) + 1
            sayı = sayı / 2  (Zorunlu adımı atla)
        DEĞİLSE (sayı ÇİFT ise):
            sayı = sayı / 2
        
        EĞER yeni_sayı TEK ise: Dizi'ye 0 ekle
        DEĞİLSE: Dizi'ye 1 ekle
    
    EĞER Dizi kısa kaldıysa:
        Dizi'yi başa sararak doldur (Cyclic Padding)
    
    DÖNDÜR Dizi

ANA PROGRAM:
    Girdi: Kullanıcı Tohumu (Seed)
    
    // Çığ Etkisi (Avalanche Effect) için Anahtar türetimi
    Hesapla: Anahtar (Key) = Seed + 1

    Akış_A = SmartCollatz(Seed)
    Akış_B = SmartCollatz(Key)
    Akış_B = TERS_ÇEVİR(Akış_B)

    Sonuç_Şifresi = Akış_A XOR Akış_B
    
    YAZDIR Sonuç_Şifresi
    HESAPLA İstatistikler

BİTİR
```

# Algoritmanın Akış Şeması

```mermaid
graph TD
    A[Başlat: Kullanıcıdan Tohum Al] --> B[Otomatik Anahtar Hesapla: Key = Seed + 1]
    B --> C{Sayı Tek mi?}
    C -- Evet --> D[3n+1 İşlemi]
    D --> E[Zorunlu 2'ye Bölme - Atla]
    C -- Hayır --> F[2'ye Bölme]
    E --> G[Yeni Sayı Kontrolü]
    F --> G
    G -->|Sonuç Tek| H[Bit: 0 Ekle]
    G -->|Sonuç Çift| I[Bit: 1 Ekle]
    H --> J{Uzunluk Yeterli mi?}
    I --> J
    J -- Hayır --> C
    J -- Evet --> K[Akış A Tohum ve Akış B Anahtar Oluştur]
    K --> L[Akış B'yi Ters Çevir]
    L --> M[A XOR B İşlemi]
    M --> N[Sonuç Şifresini ve İstatistikleri Yazdır]
 
