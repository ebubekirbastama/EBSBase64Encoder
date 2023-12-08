 

# Base64 Kodlama Algoritması
<p>Base64, metin dışı verilerin güvenli bir şekilde taşınması için yaygın olarak kullanılan bir kodlama algoritmasıdır. Bu makalede, Base64'ün nasıl çalıştığına dair ayrıntılı bir anlatım bulacaksınız. 

Ayrıca, C# programlama dilini kullanarak basit bir Base64 dönüşümü gerçekleştiren bir sınıfın nasıl oluşturulacağını adım adım öğreneceksiniz.</p>

<p>Base64, 8 bitlik bilgi gruplarını ASCII karakter setinde temsil edilebilen 6 bitlik gruplara dönüştürerek veriyi sıkıştırmak ve metin dışı verileri metin tabanlı sistemlerde taşımak için kullanılan bir kodlama algoritmasıdır. Bu yazı, Base64'ün çalışma prensiplerini anlamak isteyenler ve C# ile nasıl uygulanacağını öğrenmek isteyen geliştiriciler için bir rehber niteliği taşımaktadır.</p>



# Base64 Nedir?
Base64, her biri 6 bitlik bilgi gruplarına dönüştürülen 8 bitlik bloklarla çalışan bir kodlama sistemidir. Bu dönüşüm, metin dışı verilerin (resimler, ses dosyaları) metin tabanlı iletişimlerde güvenli bir şekilde taşınmasına yardımcı olur. Her 6 bitlik blok, 64 farklı karakteri temsil edebilen bir ASCII karakterine dönüştürülerek şifrelenmiş veri elde edilir.

# Base64 Mantığı Nedir?
<p>Base64 dönüşümünü bir örnek ile anlatalım  "123" kelimesinin adımları şu şekildedir:

İlk olarak, "123" ifadesi ASCII karakterlerine dönüştürülür. ASCII değerleri şu şekildedir:

'1' => 49 (binary: 00110001)
'2' => 50 (binary: 00110010)
'3' => 51 (binary: 00110011)

Bu ASCII değerleri 8 bitlik bloklara ayrılır:

'1' => 00110001
'2' => 00110010
'3' => 00110011

Bu 8 bitlik bloklar, Base64 için 6 bitlik bloklara dönüştürülür. Bu dönüşüm şu şekilde olur:

001100 => 12 (decimal)
100100 => 18 (decimal)
100011 => 19 (decimal)

Bu 6 bitlik bloklar, Base64 karakter setindeki karşılıklarıyla değiştirilir. Örneğin:

12 => M
18 => S
19 => T

Bu adımlar sonucunda "123" ifadesi Base64 ile şifrelenmiş olarak "MTIz" şeklinde elde edilir. Bu, her karakterin 6 bitlik bloklara dönüştürülüp daha sonra Base64 karakter setine karşılıklarıyla ifade edilmesiyle oluşan bir şifreleme örneğidir.

 Base64 Karakter Seti Tablosu

</p>

| Base64 Karakter | Ondalık Değer |
| --- | --- |
| A | 0 |
| B | 1 |
| C | 2 |
| D | 3 |
| E | 4 |
| F | 5 |
| G | 6 |
| H | 7 |
| I | 8 |
| J | 9 |
| K | 10 |
| L | 11 |
| M | 12 |
| N | 13 |
| O | 14 |
| P | 15 |
| Q | 16 |
| R | 17 |
| S | 18 |
| T | 19 |
| U | 20 |
| V | 21 |
| W | 22 |
| X | 23 |
| Y | 24 |
| Z | 25 |
| a | 26 |
| b | 27 |
| c | 28 |
| d | 29 |
| e | 30 |
| f | 31 |
| g | 32 |
| h | 33 |
| i | 34 |
| j | 35 |
| k | 36 |
| l | 37 |
| m | 38 |
| n | 39 |
| o | 40 |
| p | 41 |
| q | 42 |
| r | 43 |
| s | 44 |
| t | 45 |
| u | 46 |
| v | 47 |
| w | 48 |
| x | 49 |
| y | 50 |
| z | 51 |
| 0 | 52 |
| 1 | 53 |
| 2 | 54 |
| 3 | 55 |
| 4 | 56 |
| 5 | 57 |
| 6 | 58 |
| 7 | 59 |
| 8 | 60 |
| 9 | 61 |
| + | 62 |
| / | 63 |

C# İle Base64 Uygulaması:
Aşağıda, C# programlama dilini kullanarak basit bir Base64 dönüşümü gerçekleştiren bir sınıf örneği bulunmaktadır. Bu örnek, verilen bir metni Base64'e dönüştüren temel bir sınıfı içermektedir.
**Makalenin Devamı ve Örnek Kod İçin:**
[https://www.csharpegitimi.com.tr/2023/12/sifirdan-base64-algoritmasi.html](https://www.csharpegitimi.com.tr/2023/12/sifirdan-base64-algoritmasi.html)

