# Ders Notu Protokolü — her ders, her oturum

> [!important] Bu dosya bağlayıcı
> Yeni sohbette, yeni dersin notlarını çıkarmak istediğinde **önce bu dosyayı oku**,
> sonra `📚 900-Dersler/<DERS>/<DERS>.md` indeks dosyasını oku.

## Yeni sohbette ne yazman lazım

Tek satır yeter. Örnek:

```
📚 900-Dersler/PROTOKOL.md oku. ADE489 kağıt s. 35-37.
```

veya yeni bir ders için:

```
📚 900-Dersler/PROTOKOL.md oku. Ders: ADEXXX, kaynak: <dosya.pdf>, kağıt s. 1-10.
```

**Bundan sonrası benim işim.** Araç aramam gerekmez, kural bu dosyada.

## Yedi kural

1. **"Sayfa" = kağıttaki basılı sayfa.** PDF görüntüleyici sayfası DEĞİL.
   Kayma hesaplanır ve notun frontmatter'ına `pdf_viewer:` olarak yazılır.
   *Kanıt:* `ADE489`'de PDF = kağıt + 12.

2. **Sözlük ayrı dosyada.** `📚 900-Dersler/<DERS>/sozluk/<sayfa-arası>-sozluk.md`
   Her sözlük dosyasının başında **hangi sayfalara ait olduğu** yazılı
   (`sayfa:` alanı + başlıkta aralık) ve hangi sayfa notlarına ait olduğu listelenir.

3. **Almanca ve Türkçe alt alta ayrı paragraflar hâlinde yazılır.**

 ```
 Almanca açıklama veya metin paragrafı.

 Türkçe karşılığı ve açıklaması ayrı paragraf olarak yazılır.
 ```

 Almanca metin ana metindir; hemen ardından Türkçe çeviri/açıklama gelir. Kelime kelime parantez içi çeviri kullanılmaz. Sözlük yine ayrı dosyada tutulur; A2+ ve üzeri kelimeler bağlamlarıyla sözlüğe eklenir.

4. **Sen verirsin, ben çıkarım.** Kaynak + aralık senin belirlediğin kadar.
   Tüm kaynakları birden okumam. Yeni kaynak verirsen **mevcut notlara eklerim**,
   baştan yazmam.

5. **Sözlük genişliği korunur.** A1 kelimeler (`das Buch`, `die Schule`) girmez.

6. **Her notun sonunda boşluk raporu:** hangi sayfalar işlenmedi.

7. **Notlar kaynak kaynağa ayrılır (2026-10-06 kuralı).** Her kaynağın
   (yazar/makale/kitap) notu **kendi klasöründe** durur; tüm notlar ders klasörünün
   altına düz dizilmez.
   - Klasör adı = kaynak/yazar adı (küçük harf, boşluksuz): `linke/`, `nicklas/`
   - Yapı: `<DERS>/<kaynak>/sayfa-XX-YY-<konu>.md` +
     `<DERS>/<kaynak>/sozluk/sayfa-XX-YY-sozluk.md`
   - Kaynağın `sozluk/` klasörü kendine aittir; ders düzeyinde ortak sözlük klasörü YOK.
   - İndeks (`<DERS>.md`) her kaynağı ayrı tablo altında listeler.
   - **Not çıkarırken internet/mcp araştırması kullanılır:** yazar, makale adı, yayın
     yeri ve sayfa aralığı web'den doğrulanır; notun `> [!source]` bloğuna gerçek
     künye (dergi/kitap adı, editör, yıl, sayfa) yazılır.

## Dosya düzeni

```
📚 900-Dersler/
  PROTOKOL.md                    ← bu dosya
  README.md                      ← sistem genel tanıtım
  <DERS>/
    <DERS>.md                    ← künye, kaynak künyeleri, indeks, boşluk raporu
    <kaynak-1>/                  ← kaynağa göre klasör (örn. linke/)
      sayfa-24-27-<konu>.md      ← sayfa notu (Almanca paragraf + altında TR paragraf)
      konu-01-<konu>.md          ← sayfasız kaynak notu (sunum/slayt)
      sozluk/
        sayfa-24-27-sozluk.md    ← o sayfaların A2+ sözlüğü
    <kaynak-2>/                  ← her kaynak kendi klasöründe (örn. nicklas/)
      sayfa-35-42-<konu>.md
      sozluk/
        sayfa-35-37-sozluk.md
    kaynak/                      ← PDF (git'e girmez)
    kartlar/                     ← S10 aralıklı tekrar
```

## Erişim (4 cihaz)

Vault tek yazıcı tarafından üretilir, Git ile tüm cihazlara gider:
masaüstü, laptop, sunucu, telefon (Obsidian). Sunucudaki Hermes bu notları
doğrudan okuyabilir — RAG/embedding gerekmez.
