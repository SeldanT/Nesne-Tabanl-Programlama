Nesne Tabanlı Programlama
Proje 1: Araç Kiralama Sistemi
DOSYA AMACI
Bu dosya, araç kiralama sisteminin ana arayüzünü oluşturur. Kullanıcıların araçları listelemesi, araç kiralaması, yeni araç eklemesi ve araç çıkarması gibi temel işlemler bu dosya üzerinden gerçekleştirilir. Uygulama arayüzü Python’un tkinter kütüphanesi ile geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
ARAC SINIFI
•	Her bir araca ait ID, model, fiyat ve kiralama durumu bilgilerini tutar.
•	arac_durumu_guncelle() metodu ile aracın kiralanma durumu ve kiralayan müşteri bilgisi güncellenir.
MUSTERI SINIFI
•	Müşterinin ID, adı ve soyadı bilgilerini tutar.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi oluşturur ve başlık ile boyut ayarlamalarını yapar.
•	Label: Kullanıcıya hoş geldiniz mesajı gösterir.
•	Button: "Araç Kirala", "Araç Ekle", "Araç Çıkar" işlemleri için üç buton kullanılmıştır.
•	Listbox: İki ayrı liste kutusu ile kiralanabilir ve kiralanmış araçlar ayrı ayrı gösterilir.
________________________________________
FONKSİYONLAR
KIRALAMA_YAP
•	Kullanıcıdan müşteri bilgileri ve kiralamak istediği aracın ID’si alınır.
•	Girilen ID’ye göre araç listesi kontrol edilir ve uygun araç varsa kiralanır.
•	Araç zaten kiralanmışsa veya ID geçersizse hata mesajı gösterilir.
ARAC_EKLE
•	Kullanıcıdan yeni araç bilgileri alınarak araclar listesine eklenir.
•	Liste güncellenir.
ARAC_CIKAR
•	Kullanıcıdan çıkarmak istediği aracın ID’si alınır.
•	Eşleşen araç varsa listeden silinir ve liste güncellenir.
ARAC_LISTESI_GOSTER
•	İki listbox temizlenir.
•	Araçlar kiralanma durumuna göre listbox’lara yazdırılır.
________________________________________
KULLANILAN VERİ YAPILARI
•	araclar: Tüm araç nesnelerinin tutulduğu liste.
•	musteriler: Kiralama yapan müşterilerin tutulduğu liste.
•	listbox, listbox2: Müsait ve kiralanmış araçları ayırmak için kullanılan liste kutuları.

Proje 2: Hastane Randevu Sistemi
DOSYA AMACI
Bu dosya, bir hastane için basit bir randevu yönetim sistemi arayüzünü içermektedir. Kullanıcılar sisteme hasta kaydı ekleyebilir, doktorlardan randevu alabilir ve daha önce alınan randevuları iptal edebilir. Program, Python dilinde tkinter kütüphanesi kullanılarak görsel arayüz ile geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
HASTA SINIFI
•	Hasta adına, TC kimlik numarasına ve randevu geçmişine ait bilgileri tutar.
•	randevu_gecmisi listesi, hastanın geçmiş randevularını içerir.
DOKTOR SINIFI
•	Doktorun adı, uzmanlık alanı ve müsaitlik durumu bilgilerini barındırır.
•	musaitlik özelliği randevu alındığında False yapılır.
RANDEVU SINIFI
•	Randevunun tarihi, hangi doktora ve hangi hastaya ait olduğu bilgilerini içerir.
•	aktif alanı ile randevunun geçerli olup olmadığı kontrol edilir.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencere oluşturulmuştur. Başlık ve boyut ayarlanmıştır.
•	Label: Giriş mesajı gösterir.
•	Button: "Hasta Ekle", "Randevu Al", "Randevu İptal" işlemleri için üç ayrı buton kullanılmıştır.
•	Listbox: Hasta listesi, doktor listesi ve randevu listesi için üç farklı liste kutusu kullanılmıştır.
________________________________________
FONKSİYONLAR
HASTA_EKLE
•	Kullanıcıdan hasta ismi ve TC kimlik numarası alınarak Hasta nesnesi oluşturulur ve hastalar listesine eklenir.
•	hasta_listesi_goster() fonksiyonu çağrılarak arayüz güncellenir.
RANDEVU_AL
•	TC girilerek hasta bulunur. Ardından doktor ismi alınır.
•	Eğer doktor müsaitse tarih alınır ve Randevu nesnesi oluşturulur.
•	Doktorun müsaitliği kapatılır, randevu hasta ve genel listeye eklenir.
•	Bilgilendirme mesajı gösterilir ve liste güncellenir.
RANDEVU_IPTAL
•	TC ve doktor ismine göre randevu bulunur.
•	Randevu aktif = False yapılır ve doktorun müsaitliği tekrar açılır.
•	Liste güncellenir.
HASTA_LISTESI_GOSTER
•	Tüm hastalar listbox üzerinde sıralanır.
DOKTOR_LISTESI_GOSTER
•	doktorlar listesindeki tüm doktor bilgileri listbox1 üzerinde gösterilir.
RANDEVU_LISTESI_GOSTER
•	randevular listesindeki tüm randevular listbox2 ile gösterilir.
•	Aktif olmayan (iptal edilen) randevular da iptal bilgisiyle birlikte yazdırılır.
________________________________________
KULLANILAN VERİ YAPILARI
•	hastalar: Tüm hasta nesnelerinin tutulduğu liste.
•	doktorlar: Tanımlı doktor nesnelerinin tutulduğu liste.
•	randevular: Alınan randevuların tutulduğu genel liste.
•	listbox, listbox1, listbox2: Hasta, doktor ve randevu bilgilerini görsel olarak listeleyen kutular.

Proje 3: Kütüphane Yönetim Sistemi
DOSYA AMACI
Bu dosya, temel bir kütüphane yönetim sistemi arayüzünü içermektedir. Kullanıcılar yeni üyeler ve kitaplar ekleyebilir, ödünç alma ve iade işlemlerini gerçekleştirebilir. Arayüz, Python programlama dilinde tkinter kütüphanesi ile geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
KITAP SINIFI
•	Kitabın ID, adı ve yazar bilgilerini tutar.
•	durum alanı kitabın “Müsait” ya da “Ödünç Alındı” olduğunu gösterir.
•	durum_guncelle() fonksiyonu kitap durumunu günceller.
UYE SINIFI
•	Üye ID, adı ve soyadı bilgilerini tutar.
•	Üyenin ödünç aldığı kitaplar odunc_alinan_kitaplar listesinde saklanır.
•	odunc_al() ve iade_et() fonksiyonları ile kitap ödünç alma ve iade işlemleri yapılır.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi oluşturur. Başlık ve boyut ayarlanır.
•	Label: Sisteme hoş geldiniz mesajı verir.
•	Button: “Üye Ekle”, “Kitap Ekle”, “Ödünç Al”, “İade Et” işlemleri için dört buton yer alır.
•	Listbox: Üyeler ve kitaplar ayrı ayrı listbox bileşenlerinde listelenir.
________________________________________
FONKSİYONLAR
UYE_EKLE
•	Kullanıcıdan ID, ad ve soyad bilgileri alınarak yeni bir üye oluşturulur.
•	Üye uyeler listesine eklenir.
•	uye_listesi_goster() fonksiyonu ile liste güncellenir.
KITAP_EKLE
•	Kullanıcıdan kitap ID, adı ve yazar bilgisi alınarak yeni kitap oluşturulur.
•	Kitap kitaplar listesine eklenir.
•	kitap_listesi_goster() fonksiyonu çağrılır.
ODUNC_AL
•	Üye ID’ye göre üye bulunur.
•	Kitap ID’ye göre kitap bulunur.
•	Üyenin odunc_al() fonksiyonu çalıştırılır.
•	Başarılı işlem sonrası kitap durumu güncellenir ve liste yenilenir.
IADE_ET
•	Üye ID’ye göre üye bulunur.
•	Kitap ID’ye göre kitap bulunur.
•	Üyenin iade_et() fonksiyonu çalıştırılır.
•	Kitap durumu "Müsait" olarak güncellenir ve liste yenilenir.
UYE_LISTESI_GOSTER
•	Üyeler listbox üzerinde listelenir.
KITAP_LISTESI_GOSTER
•	Kitaplar listbox1 üzerinde listelenir.
•	Kitap durumu (müsait/ödünç alındı) da gösterilir.
________________________________________
KULLANILAN VERİ YAPILARI
•	kitaplar: Tüm kitap nesnelerinin tutulduğu liste.
•	uyeler: Sisteme kayıtlı tüm üyelerin tutulduğu liste.
•	listbox, listbox1: Üye ve kitap bilgilerini kullanıcıya göstermek için kullanılır.
Proje 4: Etkinlik Yönetim Sistemi
DOSYA AMACI
Bu dosya, etkinlikler ve katılımcılar arasında bilet işlemlerinin yönetildiği bir etkinlik yönetim sistemi arayüzünü içermektedir. Kullanıcılar yeni katılımcı ve etkinlik ekleyebilir, bilet satın alabilir ve listeleri görüntüleyebilir. Uygulama arayüzü Python programlama dili kullanılarak tkinter kütüphanesi ile geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
ETKINLIK SINIFI
•	Etkinlik ID, adı, tarihi ve katılımcı listesini tutar.
•	Her etkinlik bir veya birden fazla katılımcıyı içerebilir.
KATILIMCI SINIFI
•	Katılımcı ID, adı ve soyadı bilgilerini tutar.
•	Katılımcının katıldığı etkinlikler etkinlikler listesi içinde yer alır.
BILET SINIFI
•	Bilet ID, ilişkili etkinlik ve katılımcı bilgilerini tutar.
•	bilet_al() fonksiyonu ile bilet alma işlemi yapılır ve ilişkili veriler güncellenir.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi oluşturur, başlık ve boyut ayarlanır.
•	Label: Sisteme hoş geldiniz mesajı verir.
•	Button: “Katılımcı Ekle”, “Etkinlik Ekle”, “Bilet Al” işlemleri için butonlar eklenmiştir.
•	Listbox: Katılımcılar, etkinlikler ve biletler için üç ayrı liste kutusu kullanılmıştır.
________________________________________
FONKSİYONLAR
KATILIMCI_EKLE
•	Kullanıcıdan katılımcı ID, ad ve soyadı alınır.
•	Yeni Katilimci nesnesi oluşturularak katilimcilar listesine eklenir.
•	katilimci_listesi_goster() fonksiyonu ile liste güncellenir.
ETKINLIK_EKLE
•	Kullanıcıdan etkinlik ID, adı ve tarihi alınır.
•	Yeni Etkinlik nesnesi etkinlikler listesine eklenir.
•	Liste güncellenir.
BILET_AL
•	Katılımcı ID’si ile katılımcı bulunur.
•	Etkinlik ID’si ile etkinlik bulunur.
•	Yeni bilet oluşturulur ve bilet_al() metodu çağrılarak katılımcı ve etkinlik nesneleri güncellenir.
•	Bilet biletler listesine eklenir.
KATILIMCI_LISTESI_GOSTER
•	katilimcilar listesindeki tüm katılımcılar listbox üzerinde gösterilir.
ETKINLIK_LISTESI_GOSTER
•	etkinlikler listesindeki tüm etkinlikler listbox1 üzerinde gösterilir.
BILET_LISTESI_GOSTER
•	biletler listesindeki her bilet, ilişkili etkinlik ve katılımcı bilgisiyle listbox2 üzerinde gösterilir.
________________________________________
KULLANILAN VERİ YAPILARI
•	etkinlikler: Sistemdeki tüm etkinlikleri tutan liste.
•	katilimcilar: Sisteme kayıtlı tüm katılımcıların listesi.
•	biletler: Oluşturulan tüm biletleri içeren liste.
•	listbox, listbox1, listbox2: Katılımcı, etkinlik ve bilet bilgilerini kullanıcıya gösteren görsel liste bileşenleri.
 Proje 5: Online Eğitim Platformu
DOSYA AMACI
Bu dosya, bir online eğitim platformu arayüzü üzerinden kurs ve öğrenci yönetimi yapılmasına olanak sağlar. Kullanıcılar kurs ve eğitmen bilgilerini sisteme ekleyebilir, öğrenci tanımlayabilir ve öğrencilerin kurslara kaydolma işlemlerini gerçekleştirebilir. Arayüz, Python’un tkinter kütüphanesi kullanılarak tasarlanmıştır.
________________________________________
KULLANILAN SINIFLAR
KURS SINIFI
•	Kursa ait ID, ad, eğitmen ve içerik bilgilerini tutar.
•	ogrenciler listesiyle kursa kayıtlı öğrenciler saklanır.
EGITMEN SINIFI
•	Eğitmenin adı ve uzmanlık alanı bilgilerini içerir.
•	Her kurs, bir Egitmen nesnesi ile ilişkilidir.
OGRENCI SINIFI
•	Öğrenci ID, isim ve e-posta bilgilerini tutar.
•	Öğrencinin kayıtlı olduğu kurslar kurslar listesinde saklanır.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi oluşturur, başlık ve pencere boyutları ayarlanır.
•	Label: Giriş mesajı gösterir.
•	Button: Kullanıcıya "Kurs Ekle", "Öğrenci Ekle" ve "Kursa Kaydol" olmak üzere üç işlem sunar.
•	Listbox: Öğrencileri ve kursları ayrı ayrı listelemek için iki liste kutusu kullanılır.
________________________________________
FONKSİYONLAR
KURS_EKLE
•	Kullanıcıdan kurs ID, adı, eğitmen adı, eğitmen uzmanlığı ve içerik bilgisi alınır.
•	Yeni Kurs nesnesi oluşturularak kurslar listesine eklenir.
•	kurs_listesi_goster() fonksiyonu ile arayüz güncellenir.
OGRENCI_EKLE
•	Öğrenci ID, ad ve e-posta bilgisi alınarak Ogrenci nesnesi oluşturulur.
•	ogrenciler listesine eklenir ve liste güncellenir.
KURSA_KAYDOL
•	Girilen öğrenci ID’si ile öğrenci bulunur.
•	Girilen kurs ID’si ile kurs bulunur.
•	Öğrenci ve kurs nesneleri birbirine bağlanarak kayıt işlemi tamamlanır.
•	Bilgilendirme mesajı verilir ve kurs listesi güncellenir.
OGRENCI_LISTESI_GOSTER
•	Öğrenciler listbox üzerinde ID, ad ve e-posta bilgileriyle listelenir.
KURS_LISTESI_GOSTER
•	Kurslar listbox1 üzerinde ID, ad, eğitmen adı ve içerik bilgisiyle listelenir.
________________________________________
KULLANILAN VERİ YAPILARI
•	kurslar: Sistemdeki tüm kursların tutulduğu liste.
•	ogrenciler: Tanımlı öğrenci nesnelerinin yer aldığı liste.
•	listbox, listbox1: Öğrenci ve kurs bilgilerini kullanıcıya görsel olarak sunar.

Proje 6: Yemek Tarifi Uygulaması
DOSYA AMACI
Bu dosya, kullanıcıların yemek tarifleri oluşturup görüntüleyebileceği bir tarif uygulamasını içerir. Kullanıcılar tarif adı, malzemeler ve içerik bilgisi girerek yeni tarifler ekleyebilir; mevcut tarifleri arayabilir ve tüm tarifleri listeleyebilir. Uygulama arayüzü Python dilinde tkinter kütüphanesi kullanılarak geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
TARIF SINIFI
•	Tarifin adı, malzemeleri ve açıklama içeriğini tutar.
•	Malzemeler, her biri Malzeme sınıfından nesnelerden oluşan bir listedir.
MALZEME SINIFI
•	Her malzeme için ad ve miktar bilgisi tutulur.
•	Malzeme nesneleri Tarif sınıfında bir liste olarak kullanılır.
KULLANICI SINIFI
•	Kullanıcı adı ve şifre bilgilerini tutar.
•	Bu sınıf, ileride giriş yapma veya kullanıcı bazlı tarif yönetimi gibi işlemler için temel oluşturur. Bu sürümde yalnızca tanımlanmıştır.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencere oluşturulmuştur. Başlık ve pencere boyutu belirlenmiştir.
•	Label: Hoş geldiniz mesajı içerir.
•	Button: “Tarif Ekle”, “Tarif Ara” ve “Tarif Listesi Göster” işlemleri için üç ayrı buton tanımlanmıştır.
•	Listbox: Eklenen tüm tariflerin görüntülenmesi için kullanılır.
________________________________________
FONKSİYONLAR
TARIF_EKLE
•	Kullanıcıdan tarif adı, malzeme adı, miktarı ve içerik bilgisi alınır.
•	Yeni Malzeme ve Tarif nesneleri oluşturularak tarifler listesine eklenir.
TARIF_ARA
•	Kullanıcıdan aramak istediği tarif adı alınır.
•	Eğer ad eşleşirse ilgili tarifin tüm bilgileri bilgi kutusunda gösterilir.
•	Tarif bulunamazsa hata mesajı gösterilir.
TARIF_LISTESI_GOSTER
•	Uygulamada kayıtlı olan tüm tarifler listbox üzerinde sıralanır.
•	Her tarif için adı, malzemeleri ve içerik bilgisi gösterilir.
________________________________________
KULLANILAN VERİ YAPILARI
•	tarifler: Sisteme eklenen tüm tariflerin saklandığı liste.
•	kullanicilar: Uygulamada tanımlanmış kullanıcıların tutulduğu liste (bu sürümde kullanılmamaktadır).
•	listbox: Tarifleri görsel olarak listelemek için kullanılır.

Proje 7: Spor Takip Uygulaması
DOSYA AMACI
Bu dosya, sporculara özel antrenman programları oluşturulmasına ve ilerlemelerin takibine olanak sağlayan bir spor takip sistemini içermektedir. Kullanıcılar sporcu ve antrenman bilgisi ekleyebilir, kişisel programlar oluşturabilir ve ilerlemeleri sisteme kaydederek daha sonra raporlayabilir. Arayüz, Python programlama dili kullanılarak tkinter kütüphanesi ile geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
SPORCU SINIFI
•	Sporcu adı ve yaptığı spor dalı bilgilerini tutar.
•	Sporcuya ait program ve ilerleme bilgileri listeler içinde saklanır.
ANTRENMAN SINIFI
•	Her antrenmanın adı ve açıklayıcı detay bilgileri bulunur.
•	Programlara dahil edilmek üzere Antrenman nesneleri oluşturulur.
TAKIP SINIFI
•	Her bir takip nesnesi; sporcu, antrenman ve ilerleme notu bilgilerini içerir.
•	Sistemdeki ilerleme kayıtları bu sınıf üzerinden oluşturulur ve saklanır.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi oluşturur ve başlık ile boyut ayarları yapılır.
•	Label: Uygulama başlığı kullanıcıya gösterilir.
•	Button: "Sporcu Ekle", "Antrenman Ekle", "Program Oluştur", "İlerleme Kaydet", "Rapor Al" olmak üzere beş farklı işlem için butonlar tanımlanmıştır.
________________________________________
FONKSİYONLAR
SPORCU_EKLE
•	Kullanıcıdan sporcu adı ve spor dalı bilgileri alınarak yeni bir Sporcu nesnesi oluşturulur.
•	Bu nesne sporcular listesine eklenir.
ANTRENMAN_EKLE
•	Antrenman adı ve detay bilgileri kullanıcıdan alınır.
•	Antrenman nesnesi oluşturularak antrenmanlar listesine eklenir.
PROGRAM_OLUSTUR
•	Kullanıcıdan bir sporcu adı ve eklenecek antrenman adı alınır.
•	Eşleşme sağlanırsa, antrenman ilgili sporcunun programına eklenir.
ILERLEME_KAYDET
•	Kullanıcıdan sporcu adı, antrenman adı ve ilerleme bilgisi alınır.
•	Eşleşme sağlanırsa, yeni bir Takip nesnesi oluşturularak takipler listesine eklenir.
RAPOR_AL
•	Kullanıcıdan bir sporcu adı alınır.
•	Bu sporcuya ait tüm takip kayıtları terminal ekranına yazdırılır.
•	(Not: Raporlar şu an için sadece print() ile konsola yazdırılmaktadır.)
________________________________________
KULLANILAN VERİ YAPILARI
•	sporcular: Sistemdeki tüm sporcuların tutulduğu liste.
•	antrenmanlar: Tanımlı tüm antrenmanları içeren liste.
•	takipler: Sporcu-antrenman-ilerleme eşleşmelerinin kayıtlarını tutan liste.

Proje 8: Stok Takip Sistemi

DOSYA AMACI
Bu dosya, bir işletmenin ürün stoklarını ve sipariş işlemlerini takip edebileceği basit bir stok yönetim sistemi sunar. Kullanıcılar yeni ürün ve sipariş ekleyebilir, ürünlerin stok miktarlarını güncelleyebilir ve hem ürün hem de sipariş listelerini görüntüleyebilir. Uygulama arayüzü Python programlama dili ile tkinter kütüphanesi kullanılarak geliştirilmiştir.
________________________________________
KULLANILAN SINIFLAR
URUN SINIFI
•	Ürün adı ve mevcut stok miktarını tutar.
•	stok_miktari değeri kullanıcı isteğine göre güncellenebilir.
SIPARIS SINIFI
•	Her siparişin bir numarası ve detay bilgisi bulunur.
•	Siparişler, oluşturuldukları sırayla siparisler listesine eklenir.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	Tk(): Ana pencereyi başlatır, başlık ve boyut bilgileri belirlenmiştir.
•	Label: Hoş geldiniz mesajı kullanıcıya gösterilir.
•	Button: Kullanıcıya "Ürün Ekle", "Sipariş Oluştur", "Stok Güncelle", "Ürün Listesi Göster", "Sipariş Listesi Göster" işlemleri için beş farklı buton sunulmuştur.
•	Listbox: Ürünler ve siparişler için iki ayrı liste kutusu kullanılmıştır.
________________________________________
FONKSİYONLAR
URUN_EKLE
•	Kullanıcıdan ürün adı ve başlangıç stok miktarı alınır.
•	Yeni Urun nesnesi oluşturularak urunler listesine eklenir.
SIPARIS_OLUSTUR
•	Kullanıcıdan sipariş numarası ve detayları alınır.
•	Yeni Siparis nesnesi siparisler listesine eklenir.
STOK_GUNCELLE
•	Kullanıcıdan güncellenmek istenen ürün adı istenir.
•	Eşleşen ürün bulunursa stok miktarı yeni değerle değiştirilir.
•	Bilgilendirme mesajı gösterilir.
URUN_LISTESI_GOSTER
•	urunler listesi kullanılarak her ürün listbox üzerinde görüntülenir.
SIPARIS_LISTESI_GOSTER
•	siparisler listesi kullanılarak her sipariş listbox1 üzerinde listelenir.
________________________________________
KULLANILAN VERİ YAPILARI
•	urunler: Tüm ürünlerin nesne olarak saklandığı liste.
•	siparisler: Sisteme kaydedilen tüm siparişleri içeren liste.
•	listbox, listbox1: Ürün ve sipariş bilgilerini kullanıcıya listeleyen arayüz bileşenleri.
Proje 9: Seyahat Planlama Uygulaması
DOSYA AMACI
Bu dosya, kullanıcıların seyahat ve rota planlaması yapabileceği sekmeli bir arayüz sunar. Uygulama, tur ve ulaşım seçeneklerini yönetmek için iki sekmeli (tab) yapı içerir. Kullanıcılar istedikleri tur ve ulaşım araçlarını seçebilir, inceleyebilir, seçimi iptal edebilir veya değiştirebilir. Arayüz, PyQt5 kütüphanesi ile tasarlanmıştır.
________________________________________
ANA YAPILAR
SINIF: SEYAHATPLANLAMAUYGULAMASI (QWidget)
Uygulamanın ana penceresini tanımlar. İki sekmeden oluşur:
•	Seyahat Planlama Sekmesi: Tur seçimleri ve işlemleri.
•	Rota Planlama Sekmesi: Ulaşım aracı seçimleri ve işlemleri.
________________________________________
ARAYÜZ ÖZELLİKLERİ
SEYAHAT PLANLAMA SEKME BİLEŞENLERİ
•	QCheckBox: Mavi Tur, Avrupa Turu, Asya Turu
•	QPushButton: Tur İncele, Tur Seç, Tur İptal
•	QLabel: Seçilen veya iptal edilen turların bilgisini kullanıcıya gösterir.
ROTA PLANLAMA SEKME BİLEŞENLERİ
•	QCheckBox: Uçak, Tren, Otomobil, Otobüs
•	QPushButton: Araç Seç, Araç İncele, Araç Değiştir
•	QLabel: Seçilen araçlar veya güncellemelerle ilgili bilgi verir.
________________________________________
VERİ ALANLARI
•	tur_sec, tur_incele, tur_iptal: Tur seçimleri için kullanılan listeler.
•	arac_sec, arac_incele, arac_degistir: Araç seçimleri için kullanılan listeler.
________________________________________
FONKSİYONLAR
tur_secildi(self, state)
•	Tur onay kutularının işaretlenmesiyle seçilen tur tur_sec listesine eklenir ya da çıkarılır.
tur_incele_clicked(self)
•	Seçilen turlar label_tur_secildi üzerinde görüntülenir.
tur_sec_clicked(self)
•	Seçilen turlar doğrulanır ve kullanıcıya bildirilir.
tur_iptal_clicked(self)
•	Seçilen turlar tur_iptal listesine alınır ve seçimler temizlenir.
________________________________________
arac_secildi(self, state)
•	Araç onay kutuları aracılığıyla arac_sec listesi güncellenir.
arac_incele_clicked(self)
•	Seçilen araçlar ekranda kullanıcıya gösterilir.
arac_sec_clicked(self)
•	Kullanıcının seçtiği araçlar etiket üzerinde yazdırılır.
arac_degistir_clicked(self)
•	Seçilen araçlar arac_degistir listesine aktarılır ve mevcut seçim temizlenir.
________________________________________
UYGULAMA AKIŞI
1.	main bloğunda uygulama başlatılır.
2.	QApplication örneği oluşturulur ve arayüz başlatılır.
3.	Kullanıcı sekmeler arası geçiş yaparak tur ve araç seçimi işlemlerini yapabilir.

Proje 10: Müşteri İlişkileri Yönetimi (CRM)
DOSYA AMACI
Bu uygulama, müşteri yönetimi, ürün satışı ve destek taleplerini kapsayan üç ayrı modülden oluşur. Kullanıcıların müşteri bilgilerini girmesi, satış işlemleri yapması ve destek başvurularını yönetmesi için bütünleşik bir grafik arayüz sunar. Proje, PyQt5 kullanılarak geliştirilmiş ve OOP prensiplerine göre bölümlendirilmiştir.
________________________________________
ANA MODÜLLER
1. MUSTERI YONETIMI
Sınıf: MusteriYonetimi
•	Müşteri bilgileri (ad, soyad, TC, telefon, ürün ID) girilir ve sisteme kaydedilir.
•	Müşteriye ait ürünler ayrı olarak eklenebilir.
•	Eklenen müşteriler tabloya yansıtılır ve her bir satıra tıklanarak detaylı bilgiler görüntülenebilir.
Sınıf: Musteri
•	Her müşteri için ürün listesi dahil olmak üzere temel kimlik ve iletişim bilgileri tutulur.
•	urun_ekle() ve urunleri_listele() metodlarıyla ürün ilişkisi yönetilir.
________________________________________
2. SATIS YONETIMI
Sınıf: Satis
•	Ürün bilgileri (kod, ad, marka, adet, tarih) girilerek tabloya kaydedilir.
•	Satış ekranında görüntülenen ürünler ayrı bir listede tutulur.
•	Ek olarak, verilen ürün ID’ye göre bu ürünü almış olan müşteriler listelenebilir.
Fonksiyon: urun_id_alan_musterileri_goster(urun_id)
•	MusteriYonetimi içindeki müşteri listesinden, belirli bir ürün ID’ye sahip olanları filtreleyip gösterir.
________________________________________
3. DESTEK MODÜLÜ
Sınıf: Destek
•	Kullanıcı adı, e-posta, destek nedeni ve sistem tarafından belirlenmiş destek hattı bilgisi girilerek destek talebi oluşturulur.
•	“Gönder” butonuna basıldığında, destek talebi alındığına dair bilgi gösterilir.
________________________________________
ARAYÜZ ÖZELLİKLERİ
Her modül bağımsız bir QWidget penceresinde çalışır ve aşağıdaki bileşenleri içerir:
•	QTabWidget: Müşteri ve satış modüllerinde sekmeli yapı.
•	QTableWidget: Verileri tablo halinde kullanıcıya sunar.
•	QLineEdit, QPlainTextEdit, QLabel: Form bileşenleri.
•	QPushButton: İşlem butonları.
________________________________________
VERİ YAPILARI
•	musteri_listesi: Tüm müşterilerin bulunduğu liste.
•	urunler: Her müşteriye ait ürünlerin tutulduğu bireysel listeler.
•	QTableWidget: Dinamik olarak güncellenen müşteri ve ürün tabloları.
________________________________________
PROGRAM AKIŞI
1.	Program başlatıldığında üç pencere açılır:
o	Müşteri Yönetimi
o	Satış Yönetimi
o	Destek
2.	Kullanıcı önce müşteri bilgilerini ve ürünleri girer.
3.	Satış sekmesinde ürün kaydı yapılabilir ve satışa göre müşteri takibi yapılabilir.
4.	Destek penceresi üzerinden kullanıcıdan destek talebi alınabilir.
________________________________________
KULLANILAN KÜTÜPHANELER
•	PyQt5.QtWidgets: Arayüz oluşturmak için tüm görsel bileşenler.
•	sys: Qt uygulamasını başlatmak için gerekli sistem modülü.

Proje 11: Müzik Enstrümanı Dükkanı Yönetimi
DOSYA AMACI
Bu uygulama, bir müzik enstrümanları dükkanında stok takibi ve satış yönetimini kolaylaştırmak amacıyla geliştirilmiştir. PyQt5 kullanılarak oluşturulan arayüzde kullanıcılar; enstrüman ekleyebilir, satış girişi yapabilir ve geçmiş işlemleri listeleyebilir.
________________________________________
MODÜL BİLEŞENLERİ
1. Enstruman Sınıfı
Her bir müzik aleti için:
•	adi: Enstrüman adı
•	fiyat: Fiyat bilgisi
•	stok: Stok miktarı
2. Satis Sınıfı
Satış işlemleri için:
•	siparis_no: Sipariş numarası
•	siparis_tarih: Sipariş tarihi
•	satilan_enstruman: Satılan enstrüman adı
•	teslimat_adresi: Alıcının teslimat adresi
3. SatisEkleDialog (QDialog)
Satış işlemi yapmak için açılan popup arayüzdür. Kullanıcıdan sipariş bilgilerini alır ve ana pencereye aktarır.
4. EnstrumanDukkani (Ana Arayüz - QWidget)
Uygulamanın ana penceresidir. Hem enstrüman hem de satış işlemleri burada yönetilir.
________________________________________
ARAYÜZ BİLEŞENLERİ
•	QLineEdit: Kullanıcıdan metin bilgisi alınır.
•	QPushButton: İşlem butonları (ekle, popup aç)
•	QTableWidget: Enstrümanlar ve satışlar tablo formatında listelenir.
•	QMessageBox: Tıklanan tablo satırlarına dair detaylı bilgi popup olarak gösterilir.
•	QDialog: Satış ekleme işlemi için ayrı bir pencere.
________________________________________
ÖZELLİKLER VE İŞLEVLER
enstruman_ekle()
•	Arayüzden alınan bilgilerle yeni enstrüman oluşturur.
•	Listeye ekler ve tabloyu günceller.
ac_satis_ekle_dialog()
•	SatisEkleDialog adında bir pencere açar.
•	Girilen bilgiler satis_ekle() fonksiyonuna gönderilir.
satis_ekle(...)
•	Yeni bir satış nesnesi oluşturur ve listeye ekler.
•	Satış tablosuna satır olarak eklenir.
enstruman_bilgisi_goster(...)
•	Tablodan seçilen enstrümana ait tüm bilgileri QMessageBox ile gösterir.
satis_bilgisi_goster(...)
•	Tablodan seçilen satışın detaylarını popup şeklinde kullanıcıya gösterir.
________________________________________
KOD AKIŞI
1.	Uygulama başlatılır (main bloğunda).
2.	Kullanıcı enstrüman veya satış bilgisi girer.
3.	Tablolar otomatik olarak güncellenir.
4.	Tablodaki bir hücreye tıklandığında detay bilgisi gösterilir.
________________________________________
KULLANILAN KÜTÜPHANELER
•	sys: Uygulama başlatma ve çıkış için.
•	PyQt5.QtWidgets: Tüm görsel bileşenler (butonlar, kutular, diyaloglar)
•	PyQt5.QtCore: Slot tanımlamaları için.
Proje 12: Kişisel Sağlık Takip Uygulaması

UYGULAMA AMACI
Bu uygulama, bireylerin kişisel sağlık bilgilerini takip edebilmesini, temel sağlık verilerini girmesini ve sistem üzerinden şikayetine göre uygun egzersiz önerileri alabilmesini amaçlamaktadır. Arayüz, PyQt5 kütüphanesi kullanılarak hazırlanmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. Kullanici Sınıfı
Kullanıcıya ait temel bilgileri tutar:
•	adi
•	soyadi
•	yas
•	cinsiyet
•	telefon_no
•	sikayet
2. SaglikBilgileri Sınıfı
Boy, kilo ve sağlık durumu bilgilerini içerir:
•	boy
•	kilo
•	kan_grubu
•	seker_durumu
•	tansiyon_durumu
3. Egzersiz Sınıfı
Üç farklı egzersiz seviyesini barındıran bir sınıftır:
•	seviye1
•	seviye2
•	seviye3
________________________________________
ANA ARAYÜZ: Arayuz Sınıfı
SEKME 1: Kullanıcı Bilgileri
•	Ad, soyad, yaş, cinsiyet ve telefon numarası alınır.
•	Şikayet seçimi yapılır (Baş, Boyun, Kol, Göğüs, Bacak).
•	“Ekle” butonu ile kullanıcı bilgisi kaydedilir.
•	Kaydın ardından otomatik olarak sağlık bilgileri sekmesine geçilir.
SEKME 2: Sağlık Bilgileri
•	Boy ve kilo (maksimum 300 sınırı ile) alınır.
•	Kullanıcı kan grubu, şeker ve tansiyon durumunu girer.
•	“Güncelle” butonu ile bilgiler kaydedilir ve egzersiz sekmesine yönlendirilir.
SEKME 3: Egzersiz Bilgilendirmesi
•	Seviye 1-2-3 seçilebilir.
•	“Başla” butonuna basıldığında, kullanıcının şikayetine göre önerilen egzersiz bilgisi QMessageBox ile gösterilir.
Proje 13: Etkinlik ve Bilet Satış Platformu

UYGULAMA AMACI
Bu uygulama, kullanıcıların giriş yaparak kitap listesi oluşturabildiği, kitaplara yorum yapabildiği, okuma ilerlemesini takip edebildiği ve yalnızca okunan kitaplara puan verebildiği bir dijital kitap okuma ve değerlendirme sistemidir.
________________________________________
KULLANILAN KÜTÜPHANE
•	PyQt5: Arayüz tasarımı ve kullanıcı etkileşimleri için kullanılmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. User
Kullanıcı bilgilerini saklar.
•	username: Kullanıcı adı
•	password: Şifre
2. Book
Kitapla ilgili tüm temel verileri barındırır.
•	title: Kitap başlığı
•	author: Yazar adı
•	publisher: Yayınevi
•	comments: Yorumlar listesi
•	rating: Puan bilgisi
•	progress: Okuma yüzdesi (0-100)
Metot:
•	add_comment(comment): Yorumu listeye ekler.
________________________________________
ANA ARAYÜZ: BookReadingPlatform
1. Kitap Listesi
•	Giriş yapılmadan liste yalnızca görüntülenir.
•	Liste, her kitap için puan bilgisi içerir.
2. Giriş Sistemi
•	Kayıtlı kullanıcılar (öğretmen, öğrenci) giriş yapabilir.
•	Başarılı giriş sonrası “Kitap Ekle” butonu görünür hale gelir.
3. Kitap Ekleme
•	Kitap adı, yazar ve yayınevi bilgisi istenir.
•	Eklenen kitap listeye dahil edilir.
4. Kitap Detayları
Kitap adına tıklanınca:
•	Yazar ve yayınevi görüntülenir.
•	Kitaba yapılan yorumlar listelenir.
•	Kullanıcı yeni yorum ekleyebilir veya yorum silebilir.
•	Kullanıcı okuma ilerlemesi belirtip kitap tamamlandıysa puan verebilir.
Proje 14: İş Takip ve Yönetim Sistemi

PROJE AMACI
Bu sistem, kullanıcıların birden fazla proje oluşturup, her projeye özel görev atayabildiği ve görevlerin ilerleme durumlarını güncelleyebildiği bir proje yönetim paneli sunar. Proje takibi, görev sorumluluğu ve ilerleme kontrolü merkezi olarak yönetilebilir.
________________________________________
KULLANILAN SINIFLAR
1. Project
•	name: Proje adı
•	start_date: Başlangıç tarihi
•	end_date: Bitiş tarihi
•	tasks: Görev listesi
•	Metot: add_task(task)
2. Task
•	name: Görev adı
•	responsible: Görevli kişi
•	progress: Görev ilerleme yüzdesi (0–100)
3. Employee (Şu an kullanılmıyor ama genişletilebilir yapıdır.)
•	name: Çalışan adı
•	tasks: Üzerindeki görevler listesi
4. ProjectManagementSystem
•	projects: Tüm projeleri saklar
•	Metotlar:
o	add_project()
o	add_task_to_project()
o	update_task_progress()
Proje 15: Çevrimiçi Kitap Okuma ve Paylaşım Platformu

UYGULAMA AMACI
Bu uygulama, kullanıcıların giriş yaparak kitap listesi oluşturabildiği, kitaplara yorum yapabildiği, okuma ilerlemesini takip edebildiği ve yalnızca okunan kitaplara puan verebildiği bir dijital kitap okuma ve değerlendirme sistemidir.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Arayüz tasarımı ve kullanıcı etkileşimleri için kullanılmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. User
Kullanıcı bilgilerini saklar.
•	username: Kullanıcı adı
•	password: Şifre
________________________________________
2. Book
Kitapla ilgili tüm temel verileri barındırır.
•	title: Kitap başlığı
•	author: Yazar adı
•	publisher: Yayınevi
•	comments: Yorumlar listesi
•	rating: Puan bilgisi
•	progress: Okuma yüzdesi (0-100)
Metot:
•	add_comment(comment): Yorumu yorum listesine ekler.
________________________________________
3. BookReadingPlatform (QMainWindow)
Uygulamanın ana arayüzünü oluşturur. Kullanıcı girişi, kitap ekleme, detay gösterme, yorum yapma ve puan verme işlevlerini içerir.
Temel Bileşenler ve Fonksiyonlar:
•	login(): Giriş penceresi açar, kullanıcı doğrulaması yapar.
•	show_add_book_button(): Girişten sonra "Kitap Ekle" butonunu gösterir.
•	add_book_dialog(): Kitap bilgilerini alacak formu gösterir.
•	add_book(): Yeni kitap nesnesi oluşturup listeye ekler.
•	update_book_list(): Kitap listesini günceller.
•	show_book_details(item): Seçilen kitabın detaylarını gösteren dialog açar.
•	add_comment(book): Kitaba yorum ekler.
•	remove_comment(book): Seçilen yorumu siler.
•	rate_book(book): Okuma ilerlemesi %100 olan kitaplara puan verir.
•	read_book(book): Kitabın okuma yüzdesini kullanıcıdan alır.
Proje 16: Film ve Dizi İzleme Servisi

UYGULAMA AMACI
Bu uygulama, kullanıcıların film ve dizi ekleyebildiği, izleme listeleri oluşturabildiği, izleme durumlarını güncelleyebildiği ve izleme geçmişini takip edebildiği bir dijital izleme servisidir.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Arayüz tasarımı ve kullanıcı etkileşimlerini gerçekleştirmek amacıyla kullanılmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. Film
Film verilerini tutar.
•	ad: Filmin adı
•	yonetmen: Yönetmen adı
•	tur: Film türü
•	izleme_durumu: İzlenme yüzdesi (0–100)
________________________________________
2. Kullanici
Kullanıcı bilgilerini ve izleme geçmişini tutar.
•	kullanici_adi: Kullanıcının kullanıcı adı
•	sifre: Şifre
•	izleme_gecmisi: İzlenen filmlerin listesi
________________________________________
3. FilmServisi (QWidget)
Uygulamanın ana arayüzünü oluşturur ve işlevselliği yönetir.
Temel Fonksiyonlar:
•	film_ekle_dialog_ac(): Film ekleme penceresini açar
•	film_ekle(): Yeni bir film nesnesi oluşturur ve listeye ekler
•	filmleri_listele(): Tüm filmleri bir listede gösterir
•	izlemeye_basla(item): Seçilen filmin izleme durumunu günceller
•	izleme_listesi_olustur(): Çoklu seçimle izleme listesi oluşturur
•	izleme_listesi_kaydet(model): Seçilen filmleri izleme geçmişine ekler
•	izleme_gecmisi_goster(): Kullanıcının izlediği filmleri ve izlenme oranlarını gösterir

Proje 17: Eğitim Materyali Paylaşım Platformu
UYGULAMA AMACI
Bu uygulama, öğretmenlerin farklı dersler için konu anlatımı yükleyebildiği ve öğrencilerin bu anlatımları görüntüleyebildiği basit bir eğitim içerik paylaşım platformudur. Kullanıcılar öğrenci ya da öğretmen olarak giriş yapar.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Arayüz bileşenlerini oluşturmak ve kullanıcı etkileşimlerini sağlamak için kullanılmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. LoginWindow
Kullanıcının giriş yapmasını sağlar.
•	student_credentials: Öğrencilere ait örnek kullanıcı verileri
•	teacher_credentials: Öğretmenlere ait örnek kullanıcı verileri
•	login(): Girilen bilgileri kontrol eder, yetkili kullanıcıya göre ilgili menüyü açar
________________________________________
2. StudentWindow
Öğrencilerin ders seçip konu anlatımlarını görüntüleyebildiği ekran.
•	cmb_subjects: Öğrencinin seçeceği dersler (Matematik, Geometri, Fizik)
•	view_material(): Seçilen dersin anlatımı varsa görüntüler
•	logout(): Oturumu kapatır ve giriş ekranına döner
________________________________________
3. TeacherWindow
Öğretmenin konu anlatımı ekleyebileceği arayüzdür.
•	materials: Sınıf değişkeni olarak tüm derslere ait içerikleri saklar
•	upload(): Seçilen dersin anlatım metnini materials sözlüğüne kaydeder
•	logout(): Oturumu kapatır ve giriş ekranına döner
________________________________________
TEMEL İŞLEYİŞ
1.	Kullanıcı giriş yaptıktan sonra, kullanıcı rolüne göre uygun pencere açılır.
2.	Öğretmen, konu anlatımını yazar ve yükler.
3.	Öğrenci, dersi seçerek öğretmenin daha önce yüklediği anlatımı görüntüleyebilir.
4.	Kullanıcılar "Çıkış Yap" butonuyla oturumu sonlandırabilir.

Proje 18: Tarihçi - Tarihi Olaylar Veritabanı

UYGULAMA AMACI
Bu uygulama, kullanıcıların önemli tarihi olayları seçip detaylı hikâyelerini okuyabildiği, olayla ilişkili kişileri görebildiği ve yeni olaylar ekleyebildiği bir interaktif bilgi platformudur. Eğitim ve tarih bilincini artırma amaçlı geliştirilmiştir.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Arayüz elemanları, kullanıcı etkileşimi ve pencere yönetimi için kullanılmıştır.
________________________________________
SINIFLAR ve GÖREVLERİ
1. TarihOlaylariUygulamasi
Ana arayüzü oluşturur ve olaylarla ilgili bilgileri gösterir.
•	event_combo: Olayların listelendiği açılır menü
•	story_text: Seçilen olayın hikayesini gösterir
•	person_combo: Olayla ilişkili kişileri listeler
•	person_info_text: Seçilen kişinin açıklamasını gösterir
•	extra_info_text: Olayın hikaye + kişi bilgilerini topluca sunar
•	add_event_button: Yeni olay ekleme penceresini açar
Ana metodlar:
•	show_story(): Seçilen olayın hikayesini ve kişilerini yükler
•	load_people(): Olayla ilgili kişileri person_combo içine ekler
•	show_person(): Seçilen kişi hakkında detaylı bilgi gösterir
•	show_extra_info(): Olayın tüm verilerini (hikaye + kişiler) biçimlendirerek gösterir
•	add_event(): Yeni olay ekleme arayüzünü açar

Proje 19: Restoran Sipariş ve Yönetim Sistemi
UYGULAMA AMACI
Bu uygulama, kullanıcıların yemek ve içecekleri menüden seçerek sipariş verebildiği, stok kontrolü yapılan, ödeme tipi ve müşteri bilgisi ile birlikte siparişi tamamlayan bir dijital restoran sipariş yönetim sistemidir.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Arayüz elemanlarının yönetimi, kullanıcı etkileşimi ve pencere işlemleri için kullanılmıştır.
________________________________________
TEMEL ÖZELLİKLER
•	Yemek ve içecek menüsü
•	Stok takibi
•	Ürün adet seçme ve silme
•	Sipariş özeti ve toplam tutar
•	Müşteri bilgi girişi (Ad, soyad, telefon, adres, ödeme tipi)
•	Geçerli telefon formatı kontrolü
•	Sipariş tamamlama ve teşekkür bildirimi
________________________________________
SINIF VE METOTLAR
1. RestaurantApp(QMainWindow)
Ana uygulama arayüzünü kontrol eden sınıftır.
Özellikler:
•	menu_items: Yemeklerin fiyat ve stok bilgisi
•	drink_items: İçeceklerin fiyat ve stok bilgisi
•	selected_items: Seçilen ürünlerin takibini yapar
Arayüz Elemanları:
•	QPushButton: Yemekler, içecekler ve sipariş verme için
•	QLabel: Karşılama mesajları
•	QDialog: Ürün adeti girme, müşteri bilgisi alma, menü gösterimi
•	QLineEdit, QComboBox: Bilgi girişi ve seçim için
Ana Metotlar:
•	populate_menu(items, layout): Menüdeki ürünleri butonlar ve stok bilgisi ile birlikte gösterir
•	add_item(item): Ürün adeti seçimi penceresini açar
•	add_to_selected(item, quantity, dialog): Seçilen ürünleri sepete ekler ve stoktan düşer
•	remove_from_selected(item, quantity, dialog): Seçili ürünü sepetten çıkarır ve stoğa ekler
•	place_order(): Sipariş özetini kullanıcıya sunar ve onay alır
•	get_customer_info(total_price): Siparişe dair müşteri bilgilerini alır
•	process_order(customer_info): Siparişi işleme alır ve kullanıcıya bilgi verir
•	show_drinks() / show_foods(): Ürün kategorilerini ayrı pencerede listeler
________________________________________
KULLANICI DENEYİMİ AKIŞI
1.	Kullanıcı uygulamayı açar ve karşılama mesajlarını görür
2.	“Yemekler” veya “İçecekler” menüsünden ürünleri seçer
3.	Seçilen ürünlerin miktarını girerek sepete ekler
4.	Gerekirse yanlış ürünleri çıkarabilir
5.	“Sipariş Ver” butonuna basarak özet ve toplam tutarı görüntüler
6.	Onay sonrası müşteri bilgilerini girerek siparişi tamamlar
7.	Sipariş alındı bildirimi ile işlem sonlanır
Proje 20: Video Oyun Koleksiyonu Yönetimi
UYGULAMA AMACI
Bu uygulama, oyuncuların kendi oyun koleksiyonlarını yönetmelerine, oyunlara yıldız puanı vererek favori listelerini oluşturmalarına ve her oyun için yorum yapmalarına olanak tanıyan bir dijital oyun koleksiyonu yönetim sistemidir.
________________________________________
KULLANILAN KÜTÜPHANE
PyQt5: Kullanıcı arayüzünün oluşturulması, diyalog pencereleri ve etkileşimli bileşenler için kullanılmıştır.
________________________________________
ÖNE ÇIKAN ÖZELLİKLER
•	Oyun koleksiyonuna oyun ekleme
•	Her oyun için tür ve platform bilgisi tanımlama
•	Oyunlara yıldız puanı verme (0–5 arası)
•	Favori oyunların otomatik sıralanması
•	Yorum ekleyebilme ve yorumları listeleme
•	Kaydırmalı puanlama ve dinamik arayüz güncellenmesi
________________________________________
SINIFLAR ve GÖREVLERİ
1. Oyun
Bir video oyununun bilgilerini içerir.
•	adi: Oyun adı
•	turu: Oyun türü
•	platformu: Oyun platformu
•	yorum: Kullanıcının yazdığı yorum
•	yildiz: 0–5 arasında kullanıcı puanı
________________________________________
2. Koleksiyon
Oyunları liste halinde saklar ve yönetir.
•	oyun_ekle(oyun): Koleksiyona oyun ekler
•	oyun_listele(): Konsola oyunları listeler (yalnızca terminal çıktısı)
________________________________________
3. Oyuncu
Oyuncu profilini temsil eder.
•	adi: Oyuncu ismi
•	koleksiyon: Koleksiyona ait oyunlar
•	favori_oyunlar: Yıldız sırasına göre sıralanmış oyunlar
•	yildiz_ver(oyun, yildiz): Oyun için yıldız verip favori listesini günceller
________________________________________
4. YorumEkleDialog
Yorum yazmak için açılan bir metin girişi penceresidir.


________________________________________
5. FavoriOyunlarDialog
Yıldız puanlarına göre sıralanmış favori oyunları görüntülemek için açılan bilgi penceresidir.
________________________________________
6. YorumlarDialog
Sadece yorum yapılmış oyunları listelemek için kullanılır.


SELDAN TÜR   220
