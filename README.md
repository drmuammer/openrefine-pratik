# 🧹 OpenRefine Eğitimi

### _Adım adım, panik yapmadan kirli veri temizleme rehberi_

[![Site](https://img.shields.io/badge/Site-drmuammer.github.io%2Fopenrefine--pratik-14B8A6?style=for-the-badge)](https://drmuammer.github.io/openrefine-pratik/)
[![License](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg?style=flat-square)](https://creativecommons.org/licenses/by/4.0/)
[![Status](https://img.shields.io/badge/Status-Aktif-success?style=flat-square)](#)
[![Lang](https://img.shields.io/badge/Dil-Türkçe-red?style=flat-square)](#)

---

## Bu Eğitim Ne İşe Yarar?

Excel'in yetmediği noktada takılan herkes için **OpenRefine** kullanım rehberi. Yazım kaosu, format düzensizliği, yinelenen kayıtlar — hepsini tek seferde, tekrarlanabilir biçimde temizlemeyi öğretir.

## 🌐 Online Olarak Okuma

Eğitimin online sürümü: **<https://drmuammer.github.io/openrefine-pratik/>**

## 📚 İçerik

8 bölümlük eğitim:

1. **Kurulum ve Veri Güvenliği** — Kurulum + hassas verilerle çalışma rehberi
2. **Veriyi Tanıyalım** — Proje oluşturma, ilk bakış
3. **Kategorik Kolonları Standartlaştırma** — Text Facet ve Cluster
4. **Sayısal Kolonları Düzenleme** — GREL'e giriş
5. **Telefon Numaraları** — Regex pratiği
6. **Tarihleri Standartlaştırma** — `toDate()` ile çoklu format
7. **E-posta ve Yinelenenler** — Doğrulama ve duplicate silme
8. **Bitiriş** — Export + operations.json ile tekrarlanabilirlik

## 💻 Yerel Olarak Çalıştırma

### Önkoşul

[Quarto](https://quarto.org/docs/get-started/) kurulu olmalı.

### Adımlar

```bash
git clone https://github.com/drmuammer/openrefine-pratik.git
cd openrefine-pratik
quarto preview    # canlı önizleme (localhost:4848 açar)
quarto render     # statik HTML üretir → _site/ klasörüne
```

## 📂 Klasör Yapısı

```
openrefine-pratik/
├── _quarto.yml                  ← Site yapılandırma (website tipi)
├── styles.css                   ← Tema CSS (lacivert + teal)
├── index.qmd                    ← Ana sayfa (hero banner ile)
├── bolumler/                    ← 8 bölüm
│   ├── 01-kurulum-ve-guvenlik.qmd
│   ├── 02-baslangic.qmd
│   ├── 03-kategorik-kolonlar.qmd
│   ├── 04-sayisal-kolonlar.qmd
│   ├── 05-telefon.qmd
│   ├── 06-tarih.qmd
│   ├── 07-email-ve-yinelenenler.qmd
│   └── 08-bitiris.qmd
├── data/
│   └── customers_dirty.csv      ← 35 satırlık çalışma veri seti
└── .github/workflows/
    └── publish.yml              ← Otomatik GitHub Pages deploy
```

## 📦 Veri Seti

`data/customers_dirty.csv` — 35 satır, 13 kolon, uluslararası isimler (John Smith, Yuki Tanaka, François Dubois...). İçinde her türlü tipik kirlilik var:

- 5 farklı tarih formatı
- 4 farklı para birimi (`$`, `USD`, `EUR`, `€`, `£`)
- Bozuk telefon, eksik e-posta
- 5 yinelenen kayıt çifti

## 🤝 Katkı

Hata, eksik ya da öneriniz varsa [Issue](https://github.com/drmuammer/openrefine-pratik/issues) açın veya [Pull Request](https://github.com/drmuammer/openrefine-pratik/pulls) gönderin.

## 📜 Lisans

Tüm içerik [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/) altında paylaşılmaktadır.

**Önerilen atıf:**

> Beslen, M. (2026). _OpenRefine Eğitimi: Adım adım kirli veri temizleme rehberi_. <https://drmuammer.github.io/openrefine-pratik/>

## 📫 İletişim

🌐 [muammerbeslen.com](https://muammerbeslen.com)  
🔐 [Veri Güvenliği Rehberi](https://drmuammer.github.io/veri-seti-guvenligi/)  
📚 [Diğer notlar](https://github.com/drmuammer)

---

_"Temiz veri, doğru kararın yarısıdır."_
