# Sesli Notlandırıcı — Speech to Grade

Bu proje Excel'e not girme işlemini kolaylaştırmak, elle arama yapıp hücreyi seçerek not girme işleminin yerine yalnızca sesli okuyarak tabloyu doldurabilmek için geliştirilmektedir.

---

## User Manual

### What You Need

- İnternet tarayıcısı. İdealde tüm tarayıcılarda çalışması beklense de açık şekilde en iyi çalışma **Chrome** tarayıcısında görülmüştür. Stabil çalışma için şimdilik onu kullanmanızı tavsiye ediyoruz. (Safari üzerinde test edilmedi.)
- Mikrofon.
- Herhangi bir kurulum gerektirmemektedir.

### Nasıl çalıştırılır?

https://alpaslantavukcu.github.io/speech_to_grade/ bağlantısından doğrudan en güncel halini kullanmaya başlayabilirsiniz.

Doğruda kendi bilgisayarınıza indirip çalıştırmak isterseniz yalnızca `index.html` dosyasını indirip çalıştırmanız yeterlidir.

---

### Yeni Bir Oturum Oluşturmak

#### Öğrencileri Ekleyin

**Seçenek 1 — Excel'den kopyala:**
1. Excel'deki isim sütunundan isimleri kopyalayın.
2. **"İsim Listesi Yapıştır"** butonuna tıklayın.
3. Yapıştırın ve onaylayın.

**Option 2 — Dosyadan Al:**
**"Dosyadan İsim Al"** butonuna tıklayın ve herbir satırda bir isim olan metin dosyasından(txt) isimleri alın.

**Option 3 — Elle Ekleyin:**
Boş isim hücresine tıklayın ve ismi ekleyin.

#### Not Sütunu/Sütunları Ekleyin

**"+ Sütun Ekle"** butonuna tıklayın ve sütunu ekleyin.
Sütun başlığına tıklayarak yeniden isimlendirebilirsiniz.

---

### Sesle Not Girişi
1. Mikrofon butonuna ya da "space" tuşuna basın ve ilgili onayları verin.
2. Öğrenci ismini ve devamında notunu söyleyin. 
    - Örneğin: **"Alpaslan yetmiş beş"** → Alpaslan için 75 girdiğini görün.
3. Uygulama eşleşen satırı işaretler, yeşil yüksek güvenirlikle tespit edildiğini gösterir, sarı ve kırmızı daha düşük güven değerlerine işaret eder ve daha dikkatli olunmalıdır.


#### Birden Fazla Sütuna Ardışık Not Girişi (Daha çok test edilmesi gerekiyor. Dikkatli kullanın!)

**"Hepsi"** butonuna tıklayarak birden fazla sütuna ardışık bir şekilde not girebilirsiniz.

1. **"Hepsi"** butonuna tıklayın.
2. İsmi söyleyin, devamında her bir notu **"artı"** (plus) diyerek okuyun.
    - Örneğin: **"Alpaslan yirmi beş artı on beş"** → ilk sütuna 25 değerini ikinci sütuna da 15 değerini kaydettiğini görün.

#### Dil Desteği

**Turkish (tr-TR)** ve **English (en-US)** desteklenmektedir, arayüzden seçebilirsiniz.

---

### Hata Düzeltme

- **Undo:** Geri Al butonuna tıklayın ya da `Ctrl+Z`.
- Uygulama oturumdaki son 50 aksiyonu tutmaktadır.

Ayrıca tablodaki herhangi bir hücreye tıklayarak düzenleyebilir, silme işaretine tıklayarak silebilirsiniz.

---

### Oturumu Kaydetme ve Yeniden Yükleme

#### Oturumu Kaydedin

**"Kaydet"** butonuna tıklayın. Kayıt yerini seçin, uygulama `.json` formatında oturumdaki bilgileri kaydedecektir.

Uygulama her değişiklikte (not girişi, öğrenci ekleme, sütun ekleme vb.) tarayıcıya otomatik kaydeder. Sayfayı yenilesen de veriler kaybolmaz. Ancak bu kayıt yalnızca aynı tarayıcıda geçerlidir. En güvenli yol, oturumu bitirmeden önce **"Kaydet"** ile `.json` dosyasına kaydetmektir.

#### Oturumu Yeniden Açın

**"Aç"** butonuna tıklayın ve daha önce kaydettiğiniz `.json` dosyasını seçerek açın.

#### Yeni Oturum

**"Yeni"** butonuna tıklayarak, temiz yeni bir oturum başlatabilirsiniz.

---

### Notları Dışarı Aktarma

- **CSV:** **"CSV İndir"** butonuna tıklayarak ve tabloyu `.csv` formatında indirebilirsiniz.
- **Excel:**  **"Excel'e Kopyala"** butonuna tıklayarak tabloyu `tab` ile ayrışmış veri şeklinde kopyalayabilir ve böylece doğrudan Excel'e aktarabilirsiniz.

---

### `Log` Penceresi

Mikronun üzerindeki `log` penceresi uygulamanın aksiyonlarını, yaptığı başarılı ve başarısız girişimleri göstermektedir. 

---