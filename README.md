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
        
        EĞER yeni_sayı TEK ise:
            Dizi'ye 0 ekle
        DEĞİLSE:
            Dizi'ye 1 ekle
    DÖNGÜ SONU
    DÖNDÜR Dizi

ANA PROGRAM:
    Girdi: Kullanıcı Tohumu (Seed)
    Sabit: Anahtar Değeri (Key)

    Akış_A = SmartCollatz(Seed)
    Akış_B = SmartCollatz(Key)
    Akış_B = TERS_ÇEVİR(Akış_B)

    Sonuç_Şifresi = Akış_A XOR Akış_B
    
    YAZDIR Sonuç_Şifresi
    HESAPLA İstatistikler (0 ve 1 oranı)

BİTİR
```

# Algoritmanın Akış Şeması
```mermaid
graph TD
    A[Başlat: Tohum ve Anahtar Al] --> B{Sayı Tek mi?}
    B -- Evet --> C[3n+1 İşlemi]
    C --> D[Zorunlu 2'ye Bölme - Atla]
    B -- Hayır --> E[2'ye Bölme]
    D --> F[Yeni Sayı Kontrolü]
    E --> F
    F -->|Sonuç Tek| G[Bit: 0 Ekle]
    F -->|Sonuç Çift| H[Bit: 1 Ekle]
    G --> I{Uzunluk Yeterli mi?}
    H --> I
    I -- Hayır --> B
    I -- Evet --> J[Akış A ve B'yi Oluştur]
    J --> K[Akış B'yi Ters Çevir]
    K --> L[A XOR B İşlemi]
    L --> M[Sonuç Şifresini Yazdır]

 
