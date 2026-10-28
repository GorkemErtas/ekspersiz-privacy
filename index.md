# EksperSiz Gizlilik Politikası

**Son güncelleme: 28 Ekim 2026**

EksperSiz (“Uygulama”), araçların yönetilmesi, bakım ve muayene takibi, araç fotoğraflarından yapay zekâ destekli hasar değerlendirmesi, rapor ve tutanak oluşturulması, araçlarla ilgili AI asistan hizmeti ve yakındaki otomotiv hizmetlerinin bulunması için sunulur.

Bu politika, uygulamanın işleyişinde hangi verilerin, hangi amaçlarla ve hangi hizmet sağlayıcıları aracılığıyla işlenebileceğini açıklar. Kullanılan özelliğe göre işlenen veri türleri değişebilir.

**Özet:** Standart kayıt için ad soyad, e-posta ve şifre istenir; T.C. kimlik numarası, kimlik belgesi veya ödeme kartı numarası istenmez. Araç bilgileri ve görseller kullanıcı tarafından eklenir. **Güncel hasar analizi akışında hassas GPS konumu gereklidir ve koordinatlar inceleme kaydında saklanır.** Hasar görselleri doğrudan Google Gemini ile analiz edilir. Kredi/abonelik işlemleri Google Play ve RevenueCat üzerinden yürütülür.

## 1. İşlenen kişisel veriler

### Hesap ve kimlik doğrulama

- Ad soyad, e-posta adresi ve hesap kimliği.
- Parola ile girişte kimlik doğrulama bilgileri; parolalar düz metin olarak saklanmaz.
- Google ile girişte Google tarafından kimlik doğrulama amacıyla sağlanan temel profil bilgileri.
- Hesap güvenliği, e-posta doğrulaması ve parola sıfırlama için gerekli kayıtlar.

### Araçlar, analizler ve tutanaklar

- Kullanıcının kaydettiği araç bilgileri, kilometre, bakım, muayene ve hatırlatma kayıtları.
- Yüklenen araç fotoğrafları, hasar tespit sonuçları, ilgili raporlar ve tahmini onarım maliyetleri.
- Kullanıcının oluşturduğu hasar değerlendirme tutanaklarındaki olay tarihi, konumu, açıklamaları ve beyan bilgileri.
- Kurumsal hesap kullanılıyorsa şirket, üyelik ve yetki bilgileri ile yetkili üyeler arasında paylaşılan şirket araç ve inceleme kayıtları.

Hasar analizi için kullanıcının sağladığı **genel görünüm ve yakın detay olmak üzere iki farklı araç fotoğrafı** sunucuya yüklenir ve **Google Gemini görsel analiz hizmetine** gönderilir. Görseller uygulamada boyutlandırılıp yeniden JPEG oluşturularak aktarılır; bu işlem orijinal EXIF/GPS metadata bilgisini kaldırır. Ancak fotoğrafın üzerinde görünen kişiler, plakalar, adresler veya çevre ayrıntıları otomatik gizlenmez. Fotoğraflar inceleme geçmişi için saklanabilir. Güncel akışta eski YOLO/ML modeli yerine doğrudan Gemini analizi kullanılır.

Tutanak oluşturulursa **olay tarihi/saati, şehir, isteğe bağlı ilçe ve olay adresi, olay açıklaması ve beyanda bulunan kişinin adı soyadı** kaydedilebilir. Araç kaydı, plaka ve kullanıcı notları kişisel bilgiler içerebilir.

### AI asistan

AI asistana yazdığınız sorular, sağladığınız konuşma bağlamı ve seçtiğiniz araca ait gerekli bilgiler, soruyu anlamak ve yanıt üretmek için işlenebilir. Kullanıcı izin ve yetkileri kapsamında, istenen yanıt için gerekli araç, bakım, hatırlatma veya hasar kayıtlarından sınırlı bilgiler AI yanıt üretim sürecine dahil edilebilir.

AI asistan yanıtları uygulama sunucuları ve **Google Gemini** üzerinden oluşturulabilir; uygulama hakkında bilgi verirken genel RAG bilgi tabanından, güncel otomotiv bilgileri için gerektiğinde Google Search'den yararlanılır. **Kullanıcının kişisel araç verileri genel RAG belgelerine dönüştürülmez.** Yetki kontrolünden geçmiş, yanıt için gerekli sınırlı araç/hatırlatma/hasar bilgileri Gemini'ye sunulan bağlama eklenebilir. Önceki konuşmanın sınırlı bölümü ve işlem/yanıt bilgileri yanıt üretimi ile kullanım haklarının güvenli yönetimi için işlenebilir. Gereksiz kişisel veya hassas bilgileri AI asistan mesajlarına yazmamanızı öneririz.

### Konum ve harita

**Güncel sürümde yeni hasar analizi ekranı açılırken** cihaz konumu kontrol edilir ve gerekirse izin istenir. İzin verilirse **yüksek doğrulukta GPS koordinatları** alınır; koordinatlardan şehir bilgisi belirlenmeye çalışılır. **Şehir, enlem ve boylam verileri sunucuya gönderilerek inceleme kaydıyla birlikte saklanır.** Bu koordinatlar yalnızca şehir düzeyinde olmayıp kişinin bulunduğu noktayı gösterebilir.

Konum, analiz bağlamı ve yakındaki hizmetleri aramak için kullanılır. Coğrafi kodlama, harita ve servis aramasında cihazın ilgili hizmetleri ile **Google Maps/Places** kullanılabilir. Kullanıcı yol tarifi istediğinde başlangıç koordinatları Google Maps bağlantısına eklenebilir. Bu özellikler sürekli arka plan konum takibi için tasarlanmamıştır.

İzinlerinizi cihaz ayarlarından değiştirebilirsiniz; **mevcut sürümde konum izni olmadan yeni hasar analizi oluşturulamaz**.

Tutanak oluştururken kullanıcının girdiği olay konumu ayrıca tutanak kaydının bir parçası olarak saklanabilir.

### Mikrofon ve sesli giriş

Sesli giriş kullanıldığında cihazın mikrofon izni istenebilir. Konuşmanın yazıya dönüştürülmesi için cihazın veya işletim sisteminin konuşma tanıma hizmeti kullanılabilir; bu hizmetin işleyişine bağlı olarak ses verileri ilgili konuşma tanıma sağlayıcısı tarafından işlenebilir. Yazıya dönüştürülen metin, kullanıcı tarafından AI asistana gönderildiğinde yukarıda açıklanan AI asistan veri işleme sürecine girer. Sesli giriş kullanılmadığında bu özellik için mikrofon erişimine gerek yoktur.

### Bildirimler ve teknik bilgiler

Hatırlatmalar ve uygulama bildirimleri için cihaz bildirim belirteçleri (push token) ve bildirimle ilişkili kayıtlar işlenebilir. Hizmetin güvenliği, hata ayıklama ve teknik işleyişi için sınırlı bağlantı, istek ve hata kayıtları işlenebilir.

### Kredi, abonelik ve satın alma

Kişisel ve Business hesaplar için kredi bakiyesi, satın alınan kredi paketleri, kredi kullanım hareketleri, ürün kimlikleri, işlem/sipariş kimlikleri, satın alma ortamı ve durumu, iade/iptal olayları, abonelik planı, yenileme/bitiş tarihleri ve AI erişim hakları işlenebilir. Satın alma ve abonelik yönetiminde **Google Play Billing** ve **RevenueCat** kullanılır. EksperSiz kredi/banka kartı numarası veya CVV kodlarını doğrudan toplamaz veya saklamaz. Ödeme sağlayıcılarının kendi veri işleme kuralları ayrıca uygulanır.

## 2. Verilerin kullanım amaçları

Veriler yalnızca ilgili hizmetin sunulması ve işletilmesi kapsamında; hesap oluşturma ve güvenliği, araç ve şirket hesaplarının yönetimi, fotoğraf analizi, AI yanıt ve rapor üretimi, tutanak oluşturma, bakım ve muayene hatırlatmaları, yakındaki hizmetlerin gösterimi, abonelik ve kullanım hakkı doğrulaması, müşteri desteği, sistem güvenliği ve yasal yükümlülükler için işlenebilir.

Veriler kullanıcı formları, seçilen fotoğraflar, izin verilmiş cihaz özellikleri, giriş/ödeme sağlayıcılarının yanıtları ve teknik servis kayıtları üzerinden elektronik ortamda toplanabilir. İlgili işleme faaliyetine göre 6698 sayılı Kanun'un 5. maddesindeki **sözleşmenin kurulması veya ifası için gereklilik, hukuki yükümlülük, bir hakkın tesisi/kullanılması/korunması ve şartları mevcutsa meşru menfaat** hukuki sebepleri değerlendirilebilir. Açık rıza gerektiren durumlarda bu şart ayrıca sağlanmalıdır; cihazın izin ekranı bütün veri işleme faaliyetleri için sınırsız açık rıza anlamına gelmez.

AI hasar analizi ve onarım maliyeti sonuçları tahmin niteliğindedir; profesyonel veya resmî ekspertiz incelemesinin yerini almaz.

## 3. Üçüncü taraf hizmetler ve veri aktarımı

İşlevin gerektirdiği ölçüde aşağıdaki hizmetler kullanılabilir:

- **Google Sign-In:** Google hesabıyla giriş ve kimlik doğrulama.
- **Firebase Cloud Messaging:** Cihazlara bildirim gönderimi.
- **Google Maps / Places:** Harita, konum ve yakındaki işletme aramaları.
- **Google Gemini:** İki araç fotoğrafından doğrudan hasar analizi, AI asistan soru/bağlamı, tahmini onarım maliyeti için gerekli içeriklerin işlenmesi.
- **Google Search (Gemini aracılığıyla):** Gerektiğinde genel otomotiv bilgileri ve onarım fiyatı araştırması.
- **RevenueCat ve Google Play:** Abonelik, satın alma doğrulaması ve erişim hakları.
- **Brevo:** Hesap doğrulama ve hesapla ilgili e-posta iletileri.
- **Railway ve uygulamanın barındırma altyapısı:** Backend, AI servisleri, veritabanı ve dosya işlemleri.

Kullanılan özelliğe göre veriler bu sağlayıcıların altyapısında, Türkiye dışında bulunan sistemler dahil, işlenebilir. Her sağlayıcının kendi gizlilik koşulları da uygulanabilir. Kişisel verileri satmayız.

## 4. Saklama ve güvenlik

Hesap, araç, fotoğraf, analiz, tutanak, kredi ve abonelik kayıtları ilgili hizmetin yürütülmesi ve gerekli işlem kayıtlarının yönetilmesi süresince saklanabilir. Hesap silme işlemi başarıyla tamamlandığında kullanıcıya bağlı kişisel kayıtların silinmesi yürütülür; fotoğraf dosyalarının temizliği **veritabanı işleminin ardından** yapılır.

**Satın alma/iade mutabakatı, işlemlerin tekrarlanmasını önleme, güvenlik veya geçerli mali ve yasal yükümlülükler** için sınırlı teknik ve işlem kayıtları hesap silinse de gerekli ölçüde kalabilir. Business çalışma alanının ortak kayıtları, kişisel hesap silme işleminden etkilenmez. Harici hizmet sağlayıcılarının kendi saklama ve silme süreçleri ayrıca geçerlidir.

Verilerin korunması için erişim kontrolü, kimlik doğrulama ve uygun teknik/organizasyonel güvenlik önlemleri uygulanır. Hiçbir elektronik sistemin mutlak güvenlik garantisi yoktur.

## 5. Cihaz izinleri ve kullanıcı tercihleri

Uygulama, internet bağlantısı ve kullanılan özelliklere bağlı olarak bildirim, yaklaşık/hassas konum ve mikrofon/konuşma tanıma izinlerini kullanabilir. **Konum izni güncel sürümde yeni hasar analizi için gereklidir.** Mikrofon izni yalnızca kullanıcı sesli soru girişini başlattığında istenebilir. Araç fotoğrafları için cihazın medya seçme/kamera olanaklarından yararlanılır. İzinlerinizi cihaz ayarlarından yönetebilirsiniz; bazı özellikler ilgili izin olmadan çalışmayabilir.

## 6. Verilerin paylaşılması

Kullanıcı verileri satılmaz. Veriler, hizmetin sunulması için gerekli teknik sağlayıcılarla, kurumsal hesaplarda yetkili üyelerle, kullanıcı tarafından başlatılan paylaşım işlemlerinde seçilen alıcılarla veya hukuken gerekli olduğunda yetkili mercilerle, ilgili amaçla sınırlı olarak paylaşılabilir.

## 7. Hesap ve veri silme

Uygulama içinden **Profil → Hesabımı Sil** yolunu izleyerek hesabınızı silme işlemini başlatabilirsiniz. Uygulamaya erişemiyorsanız kayıtlı e-posta adresinizden **ekspersiz123@gmail.com** adresine silme talebi gönderebilirsiniz; hesabın size ait olduğunu doğrulamak için ek bilgi istenebilir.

Kişisel hesap silindiğinde hesaba bağlı kişisel araçlar, incelemeler ve ilgili uygulama kayıtları silinir; yüklenen fotoğrafların dosya temizliği de gerçekleştirilir. Şirket hesabındaki ortak veriler diğer kullanıcıları etkileyebileceğinden kişisel hesap silme işlemiyle otomatik olarak silinmez. Şirket üyelerinin önce üyeliklerini sonlandırmaları, şirket sahiplerinin ise sahiplik ilişkisini çözmeleri gerekir.

Yasal, güvenlik veya mali yükümlülükler ile satın alma/iade işlemlerinin mutabakatı için tutulması gereken sınırlı kayıtlar, ilgili gereklilik devam ettiği sürece saklanabilir. Harici sağlayıcıların kendi saklama/silme süreçleri ayrıca geçerlidir. **Hesap silmek Google Play aboneliğini otomatik olarak iptal etmeyebilir; aktif abonelikler ayrıca Google Play üzerinden yönetilmelidir.**

Ayrıntılı bilgi: [EksperSiz Hesap Silme](./account-deletion/).

## 8. Kişisel verilerinize ilişkin haklarınız

6698 sayılı Kanun'un 11. maddesi kapsamında şartları oluştuğunda kişisel verilerinizin işlenip işlenmediğini öğrenme, işleme amacı ve aktarım yapılan üçüncü kişiler hakkında bilgi isteme, hatalı/eksik verilerin düzeltilmesini veya silinmesini talep etme, gerekli bildirimlerin yapılmasını isteme, yalnızca otomatik sistemlerle yapılan analizlere itiraz etme ve kanuna aykırı işleme nedeniyle uğranan zararın giderilmesini talep etme haklarına sahip olabilirsiniz.

Başvurularınız için **ekspersiz123@gmail.com** adresinden iletişime geçebilirsiniz. Yetkisiz veri erişimini engellemek için hesap sahipliğini doğrulamak gerekebilir.

## 9. Çocukların gizliliği

EksperSiz çocuklara yönelik tasarlanmamıştır. Bilerek çocuklardan kişisel bilgi toplamayı amaçlamayız.

## 10. Politika değişiklikleri

Hizmetlerimiz veya yasal gereklilikler değiştiğinde bu politika güncellenebilir. Güncel sürüm bu sayfada yayımlanır ve son güncelleme tarihi değiştirilir.

## 11. İletişim

**EksperSiz — Geliştirici ve veri sorumlusu: Görkem Ertaş**

**E-posta:** ekspersiz123@gmail.com
