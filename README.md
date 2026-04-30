# OpenRefine ile Kirli Veri Temizleme

Adım adım, panik yapmadan bir OpenRefine eğitimi. Türkçe.

## Bu Repo Ne İçeriyor?

- **8 bölümlük Quarto book** — kurulumdan duplicate temizliğine kadar her şey
- **Kirli bir CSV veri seti** — uydurulmuş 35 satırlık müşteri verisi, içinde her türlü kirlilik var
- **Veri güvenliği rehberi** — OpenRefine'ın hangi özellikleri verini dış sunuculara gönderir, hangileri yerel çalışır

## İçindekiler

1. **Önsöz** — OpenRefine nedir, neden kullanmalıyız
2. **Kurulum ve Veri Güvenliği** — kurulum + hassas verilerle çalışma rehberi
3. **Veriyi Tanıyalım** — proje oluşturma, ilk bakış
4. **Kategorik Kolonları Standartlaştırma** — gender, subscriber, country, city
5. **Sayısal Kolonları Düzenleme** — score, income (GREL'e giriş)
6. **Telefon Numaraları** — regex pratiği
7. **Tarihleri Standartlaştırma** — toDate ile çoklu format
8. **E-posta ve Yinelenen Kayıtlar** — doğrulama ve duplicate silme
9. **Export ve Tekrarlanabilirlik** — operations.json ile işlem geçmişini saklama

## Kimler İçin?

- Veri analizi öğrenenler
- Excel'in yetmediği noktada takılan herkes
- Akademik araştırmacılar, gazeteciler, veri gazetecileri
- "Bana her hafta aynı pis CSV geliyor" diyen kurumsal çalışanlar

## Nasıl Render Edilir?

[Quarto](https://quarto.org/) gerekiyor:

```bash
# Quarto'yu yükle (https://quarto.org/docs/get-started/)

# Repo'yu klonla
git clone https://github.com/KULLANICI_ADIN/openrefine-egitim.git
cd openrefine-egitim

# Render et
quarto render

# Önizle (canlı sunucu)
quarto preview
```

Render sonrası `_book/` klasöründe HTML çıktıları olur. `_book/index.html` dosyasını tarayıcıda açabilirsin.

## Veri Seti

`data/customers_dirty.csv` — 35 satır, 13 kolon. İçinde:

- 5 farklı tarih formatı
- 4 farklı para birimi sembolü
- Her türlü telefon yazımı
- Yazım/büyük-küçük harf tutarsızlıkları
- Geçersiz e-postalar
- 5 yinelenen kayıt

## Lisans

MIT — istediğin gibi kullan, paylaş, değiştir.

## Katkıda Bulunmak

Hata bulduysan veya geliştirmek istediğin bir bölüm varsa **Issue** aç ya da **Pull Request** gönder.

## Kaynaklar

- [OpenRefine resmi sitesi](https://openrefine.org/)
- [OpenRefine dokümanı](https://openrefine.org/docs/)
- [GREL fonksiyon referansı](https://openrefine.org/docs/manual/grelfunctions)
- [Quarto dokümanı](https://quarto.org/docs/)

---

İyi temizlikler! 🧹
