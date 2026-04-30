# OpenRefine ile Kirli Veri Temizleme

Adım adım, panik yapmadan bir OpenRefine eğitimi. Türkçe.

## Bu Eğitim Ne Vaat Ediyor?

Eline kirli bir CSV geldiğinde "Excel'de elle düzeltirim" deyip iki saat kaybetmeyi bırakıp, OpenRefine ile **yarım saatte hem temiz hem tekrarlanabilir** bir iş çıkartacaksın. Sekiz kısa bölümde:

- Yazım, büyük/küçük harf, boşluk tutarsızlıklarını
- Beş farklı tarih formatını
- Birden fazla para birimi ve sayı formatını
- Bozuk telefon numaralarını ve eksik e-postaları
- Yinelenen kayıtları

birer birer hallederken, hangi sırayla, neden o sırayla yapıldığını da öğreniyorsun.

## İçindekiler

| # | Bölüm | Konu |
|---|---|---|
| 0 | Önsöz | OpenRefine nedir, neden kullanmalıyız |
| 1 | Kurulum ve Veri Güvenliği | Kurulum + hassas verilerle çalışma rehberi |
| 2 | Veriyi Tanıyalım | Proje oluşturma, ilk bakış |
| 3 | Kategorik Kolonlar | gender, subscriber, country, city |
| 4 | Sayısal Kolonlar | score, income (GREL'e giriş) |
| 5 | Telefon Numaraları | Regex pratiği |
| 6 | Tarihler | toDate ile çoklu format |
| 7 | E-posta ve Yinelenenler | Doğrulama ve duplicate silme |
| 8 | Bitiriş | Export + operations.json ile tekrarlanabilirlik |

## Veri Seti

`data/customers_dirty.csv` — uydurulmuş 35 satır, 13 kolon. İçinde her türlü tipik kirlilik var: format kaosu, eksik veri, geçersiz e-posta, duplicate. İsimler uluslararası (John Smith, Yuki Tanaka, François Dubois...).

Eğitimi bitirdiğinde 30 satıra inmiş, tüm tipleri doğru, tüm formatları tutarlı bir tablo elde edeceksin.

## Kimler İçin?

- Veri analizi öğrenenler
- Excel'in yetmediği noktada takılan herkes
- Akademik araştırmacılar, gazeteciler
- "Bana her hafta aynı pis CSV geliyor" diyen kurumsal çalışanlar

## Nasıl Render Edilir?

### Yerelde

[Quarto](https://quarto.org/) gerekiyor:

```bash
# Repo'yu klonla
git clone https://github.com/KULLANICI_ADIN/REPO_ADIN.git
cd REPO_ADIN

# Render et
quarto render

# Canlı önizleme
quarto preview
```

Render sonrası `_book/index.html` dosyasını tarayıcıda açabilirsin.

### GitHub Pages'ta Otomatik Yayın

Repo'da `.github/workflows/publish.yml` dosyası mevcut. Her `main` push'unda Quarto'yu otomatik build edip `gh-pages` branch'ine atar.

Bir kez ayarlaman gerekenler:

1. Repo'ya push at — workflow tetiklenir, `gh-pages` branch'i otomatik oluşur (1-2 dakika).
2. **Settings → Pages → Source:** "Deploy from a branch" → **Branch:** `gh-pages` / `(root)` → **Save**.
3. Bir-iki dakika içinde site `https://KULLANICI_ADIN.github.io/REPO_ADIN/` adresinde yayında.

> İlk deploy'da yetki hatası alırsan: **Settings → Actions → General → Workflow permissions** kısmından "Read and write permissions" seç ve workflow'u yeniden çalıştır.

## Kaynaklar

- [OpenRefine resmi sitesi](https://openrefine.org/)
- [OpenRefine kullanım kılavuzu](https://openrefine.org/docs/)
- [GREL fonksiyon referansı](https://openrefine.org/docs/manual/grelfunctions)
- [Quarto dokümanı](https://quarto.org/docs/)

## Lisans

Bu eğitim **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.tr)** lisansı altında yayınlanıyor.

Yani:

- ✅ **Paylaşabilirsin** — kopyalayıp dağıtabilirsin (her ortamda, her formatta).
- ✅ **Uyarlayabilirsin** — değiştirip türev eserler oluşturabilirsin.
- ✅ **Ticari amaçla bile kullanabilirsin.**
- ⚠️ **Atıf vermek şartıyla.** Orijinal kaynağa link ver, değişiklik yaptıysan belirt.

Yani derste, blogda, kurum içi eğitimde, kitapta — istediğin yerde kullan. Sadece "Şuradan aldım" demeyi unutma.

## Katkıda Bulunmak

Hata bulduysan, eklemek istediğin bir bölüm varsa, açıklamayı netleştirmek istediğin bir yer varsa: **Issue** aç ya da **Pull Request** gönder. Her tür katkı kıymetli.

---

İyi temizlikler! 🧹
