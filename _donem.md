---
title: HADİ — aktif dönem ders listesi
created: 2026-10-23
modified: 2026-10-23
type: ayar
status: aktif
tags: [ders, hadi, ayar]
---

# Aktif dönem: 2026-27 Güz (2627G)

`hadi-pull-cron.sh` **yalnız bu listede kodu olan** dersleri indirir. Satır başında `ADE` ile
başlayan ilk token kod sayılır, gerisi yorumdur. Dönem değişince **sadece bu dosyayı** güncelle;
script'e dokunmak gerekmez.

```
ADE255   # Yazınsal Metin Çevirisi (T-A) I
ADE279   # Avrupa Birliği Kurumları
ADE345   # Uygulamalı Dilbilim
ADE395   # Edebiyat Tarihi III
ADE407   # Biçembilim I
ADE411   # Çeviribilim
ADE437   # Edebiyat Tarihi V
ADE479   # Ağ Edebiyatı
ADE489   # Karşılaştırmalı Edebi Metinler I
```

## Notlar

- HADİ'de hesaba bağlı **25 kurs** görünüyor: 9'u 2627G (aktif), 16'sı 2025-26 Güz/Bahar.
  Moodle eski dersleri silmiyor, `--pull` hepsini çekmeye çalışıyordu → süzgeç bu dosya.
- ADE255, ADE345, ADE395 iki dönemde de var (2627G + 2526G). İndirme iki kurs id'sini de
  kapsıyor, ama güncellik kuralı sayesinde aynı dosya ikinci kez inmiyor.
- Liste boşaltılırsa script eski davranışa döner: **tüm** eşlenmiş dersleri indirir.
