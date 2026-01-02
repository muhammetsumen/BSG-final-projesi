# BSG-final-projesi
Collatz yanılgısı kullanılarak dengeli ve çözülmesi zor bir rastgele sayı üreteci algoritması tasarlıyorum
Proje Başlığı: Collatz Cipher (CC-Encryption)

Özet: Bu proje, matematiksel bir problem olan Collatz (3n+1) dizisini kullanarak rastgele sayı üretimi (PRNG) ve şifreleme anahtarı oluşturmayı amaçlar. Standart Collatz dizisindeki "tahmin edilebilirlik" (tek sayıdan sonra çift gelme zorunluluğu) ve "bit dengesizliği" sorunları, özel bir algoritma ve XOR manipülasyonu ile çözülmüştür.

Algoritma Mantığı:
   Zorunlu Adım Atlama (Skip Logic): Collatz dizisinde  $n$  tek ise  ($3n+1$)  sonuç daima çifttir. Bu, şifrede %100 tahmin edilebilirlik yaratır. Algoritmamız, tek sayı işleminden sonraki zorunlu çift adımı atlayarak entropiyi artırır.
   
Çift Akış (Dual Stream): 
   Akış A: Kullanıcının girdiği tohumdan üretilir.
   Akış B: Gizli bir anahtar sayıdan üretilir ve ters çevrilir.
   
Karıştırma (Diffusion): İki akış XOR işlemine sokularak bitlerin homojen dağılması (0 ve 1 dengesi) sağlanır.
