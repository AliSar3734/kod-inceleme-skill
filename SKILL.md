# Kod İnceleme Skill

## Genel Tanım
Bu skill, AI ajanları tarafından kod kalitesi, güvenlik ve okunabilirlik açısından kapsamlı kod incelemesi yapmak için kullanılır. Verilen kod parçacıklarını analiz ederek detaylı raporlar üretir.

## Amaç ve Sorumluluk
- Sunulan kodun hata, güvenlik ve okunabilirlik açısından detaylı incelemesini yapmak
- Potansiyel sorunları belirleyip çözüm önerileri sunmak
- Kod kalitesi metriklerini değerlendirmek
- Best practices ve endüstri standartlarına uygunluğu kontrol etmek
- Yapıcı ve uygulanabilir geri bildirim sağlamak

## Girdi (Input)
- Kod dosyası veya kod parçacığı
- Programlama dili
- Proje bağlamı (varsa)
- İnceleme odakları (tümü veya seçili)

## Çıktı Formatı (Output Structure)

Kod incelemesi raporu aşağıdaki yapıda sunulmalıdır:

### 1. **ÖZET (Summary)**
   - Genel değerlendirme (✓/⚠/✗)
   - Kodun genel durumu
   - Ana bulgular (3-5 madde)

### 2. **GÜVENLIK ANALİZİ (Security Analysis)**
   - SQL Injection riski
   - XSS/CSRF zafiyetleri
   - Kimlik doğrulama/yetkilendirme kontrol
   - Hassas veri işleme
   - Dependency güvenliği
   - Risk seviyesi: KRITIK / YÜKSEK / ORTA / DÜŞÜK

### 3. **HATA VE SORUNLAR (Bugs & Issues)**
   - Mantık hataları
   - Null pointer/undefined kontrol eksikleri
   - Exception handling eksikleri
   - Resource leak riski
   - Her sorun için: Satır numarası, açıklama, etki

### 4. **KOD KALİTESİ (Code Quality)**
   - Karmaşıklık analizi (Cyclomatic Complexity)
   - Kod tekrarı (DRY)
   - SOLID prensiplerine uygunluk
   - Isimlendirme (Naming Conventions)
   - Fonksiyon/Method uzunluğu
   - Nested bloklara derinlik

### 5. **PERFORMANS (Performance)**
   - Algoritma verimliliği (Time/Space Complexity)
   - Döngü ve sorgu optimizasyonu
   - Bellek yönetimi
   - Gereksiz işlemler
   - Önerilen optimizasyonlar

### 6. **OKUNABİLİRLİK VE DOKÜMANTASYON (Readability & Documentation)**
   - Yorum kalitesi ve yeterliliği
   - Docstring/JSDoc eksikleri
   - Kodu anlama kolaylığı
   - Fonksiyon amacının açıklığı
   - Değişken isimleri

### 7. **OLUMLU YÖNLER (Strengths)**
   - İyi uygulanmış kısımlar
   - Takdir edilecek patterns
   - Başarılı çözümler

### 8. **İYİLEŞTİRME ÖNERİLERİ (Recommendations)**
   - Öncelik sırasına göre sıralanmış
   - Her öneri için: Sebep, çözüm, örnek kod (varsa)
   - Aciliyet seviyeleri: HEMEN / KISA VADEDE / UZUN VADEDE

### 9. **SES BAĞLAMLAŞTIRMASI (Context & Notes)**
   - Proje türüne göre değerlendirme
   - Legacy kod varsayımı
   - Version/Framework uyumluluğu

### 10. **PUANLAMA (Scoring)**
   - Güvenlik: X/10
   - Performans: X/10
   - Okunabilirlik: X/10
   - Maintainability: X/10
   - **Genel Puan: X/10**

## İnceleme Kriterleri

### Güvenlik Kontrolü
- [ ] Input validation
- [ ] SQL/NoSQL injection kontrol
- [ ] Cross-site scripting (XSS) kontrol
- [ ] CSRF koruma
- [ ] Authentication/Authorization
- [ ] Cryptography doğruluğu
- [ ] Sensitive data exposure
- [ ] Dependency vulnerabilities

### Kod Kalitesi
- [ ] Tekrarlayan kod
- [ ] Çok uzun fonksiyonlar/classlar
- [ ] Deeply nested kodlar
- [ ] Dead code
- [ ] Magic numbers/strings
- [ ] Inconsistent naming
- [ ] God objects/classes
- [ ] Circular dependencies

### Performans
- [ ] N+1 queries
- [ ] Unnecessary data fetches
- [ ] Inefficient algorithms
- [ ] Memory leaks
- [ ] Blocking operations
- [ ] Caching opportunities

### Maintainability
- [ ] Test coverage
- [ ] Documentation
- [ ] Code comments
- [ ] Error handling
- [ ] Logging
- [ ] Configuration management

## Desteklenen Diller
- Python (Django, Flask, FastAPI)
- JavaScript/TypeScript (Node.js, React, Vue, Angular)
- Java (Spring, Hibernate)
- C# (.NET, ASP.NET)
- Go
- Rust
- PHP (Laravel, Symfony)
- Ruby (Rails)
- SQL (MySQL, PostgreSQL, MongoDB)

## Özel İşlem Kuralları

### 1. Bağlam-Duyarlılık
- Legacy kodlar için farklı standartlar uygula
- Proje büyüklüğüne göre beklentileri ayarla
- Framework'e özel best practices dikkate al

### 2. Yapıcı Geri Bildirim
- Negatif bulguları objektif sunun
- Çözüm önerileri her zaman ekleyin
- Başarıları da takdir edin
- Aşırı kritik olmayın

### 3. Örnek Kod
- Yanlış kod ve doğru kod karşılaştırmasını yap
- Diff format tercih et
- Minimal ve çalışan örnekler sun

### 4. Prioritizasyon
- Güvenlik sorunlarını öncelik ver
- Kritik hatalardan başla
- İyileştirme önerilerini aciliyete göre sırala

## Versiyon
**1.0** - AI Kod İnceleme Ajanı için Profesyonel Skill Tanımı

---

**Skill Name**: kod-inceleme-skill  
**Description**: Kodu hata, güvenlik ve okunabilirlik açısından inceleyen AI kod inceleme aracı.  
**Last Updated**: 2026-10-09
