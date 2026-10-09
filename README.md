# kod-inceleme-skill
# kod-inceleme

Kod değişikliklerini hata, güvenlik açığı, okunabilirlik ve eksik test
açısından inceleyen AI tabanlı kod inceleme aracı. Bulguları önem sırasına
göre raporlar.

## Özellikler

- `git diff` veya pull request üzerinden inceleme
- Doğruluk, güvenlik, okunabilirlik ve test kontrol listesi
- Bulguları üç gruba ayırır: Düzeltilmeli, Önerilir, İsteğe bağlı
- Her bulgu için dosya, satır ve somut düzeltme önerisi
- Kodu kendisi değiştirmez, yalnızca rapor verir

## Kurulum

```bash
git clone https://github.com/KULLANICI/kod-inceleme.git
cd kod-inceleme
```

## Kullanım

```bash
# Staged değişiklikleri incele
git diff --staged | ./review
```

Örnek çıktı:

```
Düzeltilmeli
- src/auth.py:42  Kullanıcı girdisi doğrulanmadan sorguya ekleniyor.
  Öneri: parametreli sorgu kullanın.

Önerilir
- src/utils.py:10  Fonksiyon 80 satır, ikiye bölünebilir.
```

## Katkı

Yeni kontrol kuralı eklemek için `kurallar/` klasörüne bir dosya ekleyip
pull request açın.

## Lisans

MIT
