# Arşiv — eski dönem dersleri

2026-10-23'te HADİ'den otomatik çekilen **2026-27 Güz (2627G) dönemine ait olmayan** ders
klasörleri buraya taşındı.

## Neden

HADİ hesabında 25 kurs kayıtlı: 9'u aktif dönem, 16'sı 2025-26 Bahar (2526B) / 2025-26 Güz
(2526G). `hadi_pull.py --pull` hepsini çekiyordu → 13 ders klasörü yalnız PDF/DOCX yığını
olarak duruyordu. **Hiçbirinde elle yazılmış not yoktu** (kontrol: klasör başına `.md` sayısı
`kaynak/` dışında 0).

## Taşınanlar (13)

`ADE137, ADE144, ADE226, ADE256, ADE285, ADE286, ADE338, ADE339, ADE340, ADE346, ADE390,
ADE396, ADE415`

Hepsi `kaynak/` içeriği + `INDEX.md` + `.hadi-manifest.json`. Toplam ~189 MB (git dışı,
`900-Dersler/.gitignore` kapsamında).

## Geri alma

Tek ders: `mv "_arsiv-eski-donem/ADE346" ..` → dosyalar ve manifest korunur, tekrar indirme olmaz.
Kalıcı takip: kodu `../_donem.md` listesine ekle.

## Yer açmak

Bu klasör git'te izlenmiyor; `rm -rf "📚 900-Dersler/_arsiv-eski-donem"` ~189 MB açar.
Silmeden önce gereken tek şey: içinden bir dosya lazımsa çıkar, çünkü sunucudan HADİ'ye
bağlanıp yeniden indirmek de mümkün (`--course ADE346 --force`).
