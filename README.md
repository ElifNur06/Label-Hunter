# Etiket Dedektifi (Label Hunter) 🥗🔍

Etiket Dedektifi, gıda ürünlerinin içeriklerini analiz eden, yapay zeka ile sağlık puanlaması yapan ve kişisel diyet hassasiyetlerinize uygun (vegan, glüten, laktoz vb.) beslenme tavsiyeleri sunan akıllı bir sağlık asistanıdır.

## 🚀 Temel Özellikler

- **Gelişmiş Barkod Tarama:** `simple_barcode_scanner` ile taranan ürünlerin bilgilerini OpenFoodFacts API üzerinden anlık çekme.
- **Optik Karakter Tanıma (OCR):** Google ML Kit ile gıda etiketlerinin fotoğraflarından "İçindekiler" metnini dijitalleştirme.
- **Kişiselleştirilmiş Diyet Filtreleri:** Glüten, Laktoz, Vegan, Helal, Şeker ve Protein gibi hassasiyetleri analiz sürecine dahil etme.
- **AI Destekli Sağlık Skoru:** Google Gemini 2.0 Flash API ile ürün içeriğinin 0-100 arası sağlık puanının hesaplanması.
- **Akıllı Alternatif Önerileri:** Analiz edilen ürün "Riskli" kategorideyse, kullanıcıya sağlıklı ve uygun alternatifler sunma.
- **Dijital Kiler (Geçmiş):** Taranan tüm ürünleri `SharedPreferences` ile yerel bellekte saklama ve geçmişe dönük listeleme.

## 🛠 Teknik Altyapı (Tech Stack)

| Kategori | Teknoloji / Kütüphane |
| :--- | :--- |
| **Framework** | Flutter (Dart) |
| **Optik Tanıma (OCR)** | Google ML Kit Text Recognition |
| **Yapay Zeka (LLM)** | Google Gemini API (gemini-2.0-flash) |
| **Barkod & Veritabanı** | Simple Barcode Scanner, OpenFoodFacts API |
| **Veri Kalıcılığı** | SharedPreferences (JSON Encoding) |
| **Ağ ve Medya** | HTTP, Image Picker |

## 🧠 Sistem Mimarisi ve Veri Akışı
Veri Yakalama: Uygulama, barkod ID'si veya OCR ile elde edilen metni ham veri olarak alır.

Prompt Mühendisliği (Injection): Kullanıcının seçtiği diyet filtreleri, AI'ya gönderilecek prompt içerisine dinamik olarak eklenir.

LLM Değerlendirmesi: Gemini API, ürünü kullanıcı profiline göre analiz eder ve "SKOR, ALTERNATİF, RAPOR" şablonunda çıktı döndürür.

UI Entegrasyonu: Dönen veri split() metotlarıyla ayrıştırılır ve sağlık skoruna göre UI renkleri (Yeşil-Sarı-Kırmızı) dinamik olarak güncellenir.

## Görseller
<img width="339" height="596" alt="image" src="https://github.com/user-attachments/assets/6c1628f3-6e51-4301-9a69-b57f5a9fb461" />
<img width="337" height="594" alt="image" src="https://github.com/user-attachments/assets/c40b737f-8cbf-400d-ba79-553e2ffd0f47" />
<img width="338" height="598" alt="image" src="https://github.com/user-attachments/assets/f475033c-579b-408c-ba44-49c865d43402" />
<img width="334" height="595" alt="image" src="https://github.com/user-attachments/assets/231f8ce2-da91-40e4-98ab-ecd55b276e5b" />
<img width="333" height="595" alt="image" src="https://github.com/user-attachments/assets/34ef2a49-0ea2-4f37-8d9a-1fce77ca7b00" />
<img width="337" height="596" alt="image" src="https://github.com/user-attachments/assets/f06768d2-929c-4e04-b37a-ec2f43f0858f" />

Etiket Dedektifi - Ne Yediğini Bil, Sağlıklı Yaşa.
