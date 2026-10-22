# CNSZR Kat Hizmetleri — Demo

Tarayıcıda çalışan, mobil ekrana uyumlu otel kat hizmetleri prototipi.

## Mevcut özellikler

- Ana bina ve ek bina için toplam 34 odalık örnek oda listesi.
- Resepsiyon ekranında oda durumu, misafir giriş saati ve VIP işaretleme.
- Temizlik görevlerini ortak listeye gönderme; göreve başlama ve bitirme.
- Yönetici tarafından temizlik kontrolü.
- Ek bina odaları için çıkış, giriş ve saat aralıklı temizlik talebi.
- Arıza kaydı, önem seviyesi, teknik personelin işlem ve çözüm notu.
- Gün kapatma, geçmiş kayıtlar ve CSV raporu.
- Aynı tarayıcıdaki sekmeler arasında yerel veri değişikliği bildirimi ve sesli uyarı.

## Demo hesapları

| Kullanıcı adı | Şifre | Rol |
|---|---|---|
| yonetici | 1234 | Yönetici |
| resepsiyon | 1234 | Resepsiyon |
| kat | 1234 | Kat görevlileri |
| teknik | 1234 | Teknik personel |

**Bunlar yalnızca deneme hesaplarıdır; gerçek kullanım için güvenli değildir.**

## Çalıştırma

index.html dosyasını tarayıcıda açın. İnternet bağlantısı gerektiren bir uygulama servisi bu demo sürümünde kullanılmıyor.

## Önemli sınırlar

- Veriler yalnızca o tarayıcının `localStorage` alanında tutulur; başka telefon veya bilgisayara eşitlenmez.
- Kullanıcı adı ve şifre doğrulaması istemci tarafındaki demo koduyla yapılır. Yetkilendirme güvenli değildir.
- Gerçek çok cihazlı kullanım için sunucu/veritabanı bağlantısı, sunucu tarafı kimlik doğrulama ve rol bazlı erişim kuralları gerekir.
- Bu sürümde PWA manifesti ve service worker bulunmadığından yüklenebilir/çevrimdışı PWA olarak tamamlanmış değildir.
- Bu nedenle üretim otel operasyonunda kullanmadan önce veri güvenliği, yedekleme, eşzamanlı işlem ve yetki testleri yapılmalıdır.

## Önerilen geliştirme sırası

1. Oda ve görev akışındaki hataları düzeltip temel senaryoları test etmek.
2. Supabase veya eşdeğer bir sunucu/veritabanı katmanını güvenli erişim kurallarıyla kurmak.
3. Kullanıcıları yönetici tarafından oluşturma ve güvenli oturum açma.
4. PWA manifesti, service worker ve mobil kurulum testi.
5. Gün kapatma, arıza ve CSV raporları için kabul testleri.

