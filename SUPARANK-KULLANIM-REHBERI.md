# 🚀 SUPA - Suparank Otomatik Blog Sistemi

Tam otomatik SEO-optimized blog içeriği ve görsel üretimi için kurulmuş Suparank sistemi.

---

## 📋 İçindekiler

1. [Sistem Özellikleri](#sistem-özellikleri)
2. [Hızlı Başlangıç](#hızlı-başlangıç)
3. [Otomatik Workflow'lar](#otomatik-workflowlar)
4. [Örnek Kullanımlar](#örnek-kullanımlar)
5. [Araçlar](#araçlar)
6. [Güvenlik](#güvenlik)
7. [Sorun Giderme](#sorun-giderme)

---

## 🎯 Sistem Özellikleri

### **Tam Otomatik İçerik Üretimi**
✅ Keyword araştırması
✅ SEO stratejisi oluşturma
✅ Blog yazısı yazma (Türkçe)
✅ AI ile görsel oluşturma (Gemini)
✅ Internal link önerileri
✅ Meta tag optimizasyonu

### **Harici MCP Entegrasyonları**
- 🖼️ **Gemini MCP**: AI görsel oluşturma
- 🔍 **SEO Research MCP**: Ahrefs/Semrush veri entegrasyonu
- 🕷️ **Firecrawl MCP**: Rakip içerik analizi

### **Türkçe İçerik Optimizasyonu**
- Türkçe dilbilgisi ve akıcılık
- Lokal SEO (Türkiye pazarı)
- TL para birimi ve yerel örnekler
- Profesyonel "siz" dili

---

## ⚡ Hızlı Başlangıç

### **1. API Anahtarlarını Ayarlayın**

`.env` dosyanız zaten hazır, gerekirse düzenleyin:

\`\`\`bash
# .env dosyasını düzenle
nano .env
\`\`\`

### **2. Suparank MCP'yi Başlatın**

\`\`\`bash
# MCP sunucusu zaten ekli
npx suparank
\`\`\`

### **3. İlk Blog Yazınızı Oluşturun**

Claude Code ile:

\`\`\`
"Kripto para yatırımı için komple blog oluştur"
\`\`\`

Sistem otomatik olarak:
1. ✅ Keyword araştırması yapar
2. ✅ SEO stratejisi oluşturur
3. ✅ 3000+ kelimelik blog yazar
4. ✅ Hero image ve section image'lar oluşturur
5. ✅ JSON formatında size sunar

---

## 🔄 Otomatik Workflow'lar

### **1. Complete Blog Post** (Tam Otomatik)

**Kullanım:**
\`\`\`
"[KONU] için komple blog oluştur"
\`\`\`

**Örnek:**
\`\`\`
"Evde spor yapma için komple blog oluştur"
\`\`\`

**Ne Yapar:**
- Keyword research
- SEO strategy
- Blog yazısı (2500-4000 kelime)
- Hero image (Gemini ile)
- Section images (her bölüm için)
- Internal link önerileri
- Tüm SEO metadata

**Çıktı:**
\`\`\`json
{
  "content": {
    "title": "...",
    "meta_description": "...",
    "body": "...",
    "word_count": 3200
  },
  "images": {
    "hero": {"url": "...", "alt": "..."},
    "sections": [...]
  },
  "seo": {
    "keywords": [...],
    "internal_links": [...]
  }
}
\`\`\`

---

### **2. Quick Blog Post** (Hızlı, Görselsiz)

**Kullanım:**
\`\`\`
"[ANAHTAR KELİME] için hızlı blog yaz"
\`\`\`

**Örnek:**
\`\`\`
"python veri analizi için hızlı blog yaz"
\`\`\`

**Ne Yapar:**
- SEO stratejisi
- Blog yazısı
- Temel metadata

**Süre:** ~2-3 dakika

---

### **3. SEO Audit and Content** (Rakip Analizi + İçerik)

**Kullanım:**
\`\`\`
"[KONU] için rakip [DOMAIN] analizi yap ve içerik üret"
\`\`\`

**Örnek:**
\`\`\`
"dijital pazarlama için rakip neilpatel.com analizi yap ve içerik üret"
\`\`\`

**Ne Yapar:**
- Rakibin keyword'lerini analiz eder
- Gap analysis (sizin eksik keyword'ler)
- Gap keyword'leri hedefleyen içerik yazar
- Rakipten daha iyi strateji önerir

---

### **4. Social Media Content** (Blog + Sosyal Medya)

**Kullanım:**
\`\`\`
"[KONU] için sosyal medya içerik paketi"
\`\`\`

**Örnek:**
\`\`\`
"vegan beslenme için sosyal medya içerik paketi"
\`\`\`

**Ne Yapar:**
- Blog yazısı
- Instagram square (1:1) görsel
- Twitter card (2:1) görsel
- LinkedIn post (1.91:1) görsel
- Her platform için optimize edilmiş text

---

## 🛠️ Araçlar (Manuel Kullanım)

### **keyword_research**

\`\`\`
"e-ticaret SEO için keyword araştırması yap"
\`\`\`

**Parametreler:**
- `seed_keyword`: Başlangıç kelimesi
- `competitor_domain`: Rakip domain (opsiyonel)
- `content_goal`: traffic / conversions / brand-awareness

**Çıktı:** Keyword kümeleri, zorluk skorları, fırsatlar

---

### **seo_strategy**

\`\`\`
"react hooks için SEO stratejisi oluştur"
\`\`\`

**Parametreler:**
- `target_keyword`: Hedef keyword
- `content_type`: guide / tutorial / comparison / listicle
- `search_intent`: otomatik tespit edilir

**Çıktı:** Detaylı content brief, outline, rakip analizi

---

### **content_write**

\`\`\`
"blockchain teknolojisi hakkında blog yaz"
\`\`\`

**Parametreler:**
- `target_keyword`: Hedef keyword
- `title`: Başlık (otomatik oluşturulabilir)
- `outline`: İçerik yapısı (otomatik oluşturulabilir)
- `tone`: Yazım tonu

**Çıktı:** Tam blog yazısı (JSON formatında)

---

### **image_prompt**

\`\`\`
"python tutorial için hero image"
\`\`\`

**Parametreler:**
- `subject`: Konu
- `image_purpose`: hero / diagram / illustration / social
- `mood`: modern / minimalist / vibrant

**Çıktı:**
- Optimized Gemini prompt
- Otomatik görsel (eğer Gemini MCP aktifse)

---

### **internal_links**

\`\`\`
"bu blog için internal link önerileri"
\`\`\`

**Çıktı:** Semantik olarak ilgili sayfalar + natural anchor text

---

## 📚 Örnek Kullanım Senaryoları

### **Senaryo 1: Sıfırdan Blog Başlatma**

\`\`\`
Siz: "Kişisel finans blogu için 10 blog konusu öner"

AI: [10 keyword cluster]

Siz: "İlk 3 konu için komple blog oluştur"

AI: [3 tam blog + görseller + SEO]
\`\`\`

---

### **Senaryo 2: Rakip Geçme Stratejisi**

\`\`\`
Siz: "paratic.com'u 'bütçe yönetimi' keyword'ünde geçmek için strateji"

AI:
1. Rakip analizi
2. Content gap tespiti
3. Daha iyi içerik stratejisi
4. İçerik üretimi

Siz: "Stratejiye göre 5 blog yaz"

AI: [5 SEO-optimized blog]
\`\`\`

---

### **Senaryo 3: Mevcut İçeriği Güncelleme**

\`\`\`
Siz: "[Mevcut blog URL] için SEO audit yap"

AI: [Eksikler, geliştirme önerileri]

Siz: "Önerilere göre içeriği yeniden yaz"

AI: [Güncellenmiş, daha iyi içerik]
\`\`\`

---

### **Senaryo 4: Sosyal Medya Kampanyası**

\`\`\`
Siz: "Tasarruf ipuçları için 30 günlük Instagram içerik planı"

AI:
- 30 blog konusu
- Her konu için Instagram görseli
- Carousel post'lar için çoklu görsel
- Caption önerileri
- Hashtag stratejisi
\`\`\`

---

## 🔐 Güvenlik

### **API Anahtarı Güvenliği**

✅ **YAPILMASI GEREKENLER:**
- `.env` dosyası `.gitignore`'a eklenmiş ✓
- Asla `.env`'yi commit etmeyin
- API anahtarlarını paylaşmayın
- Gerekirse anahtarları yenileyin

❌ **YAPILMAMASI GEREKENLER:**
- API anahtarlarını kod içine yazmayın
- Public repository'de paylaşmayın
- Screenshot'larda göstermeyin

### **API Anahtarı Yenileme**

Eğer yanlışlıkla paylaştıysanız:

1. **Google Cloud Console** → API & Services → Credentials
2. Mevcut anahtarı devre dışı bırak
3. Yeni anahtar oluştur
4. `.env` dosyasını güncelle

---

## 🔧 Sorun Giderme

### **Sorun: API anahtarı çalışmıyor**

\`\`\`bash
# .env dosyasını kontrol et
cat .env

# Doğru environment variable yüklü mü?
echo $GEMINI_API_KEY
\`\`\`

**Çözüm:** `.env` dosyasında doğru formatta olduğundan emin olun.

---

### **Sorun: Gemini görseller oluşturulmuyor**

**Kontrol:**
1. Gemini MCP yüklü mü?
2. API anahtarı geçerli mi?
3. Imagen API aktif mi? (Google Cloud Console)

**Çözüm:**
\`\`\`bash
# Gemini MCP'yi yükle
npm install -g @google/generative-ai

# veya npx kullan
npx @google/generative-ai
\`\`\`

---

### **Sorun: Türkçe karakterler bozuk**

**Çözüm:** Dosya encoding'ini kontrol edin:

\`\`\`bash
# UTF-8 olmalı
file -I 50-30-20-kurali-blog-post.json
\`\`\`

Credentials'da `"encoding": "utf-8"` ayarı var.

---

### **Sorun: Keyword research veri vermiyor**

**Sebep:** Harici SEO MCP yüklü değil (opsiyonel)

**Çözüm:**
- Suparank kendi verilerini kullanır (tahmini)
- Gerçek veri için: SEO Research MCP yükleyin

\`\`\`bash
npm install -g seo-research-mcp
claude mcp add seo-research npx seo-research-mcp
\`\`\`

---

## 📊 Performans İstatistikleri

### **Üretim Süreleri (Ortalama)**

| İşlem | Süre | Kelime/Görsel |
|-------|------|---------------|
| Keyword Research | 30 sn | 50-100 keyword |
| SEO Strategy | 45 sn | Detaylı brief |
| Blog Yazma | 2-3 dk | 3000 kelime |
| Görsel Oluşturma | 10-15 sn/görsel | 1 görsel |
| **TAM BLOG** | **4-5 dk** | **Blog + 5 görsel** |

---

## 🎯 En İyi Pratikler

### **1. Keyword Seçimi**

✅ **İyi:**
- "bütçe nasıl yapılır"
- "python ile web scraping"
- "keto diyeti rehberi"

❌ **Kötü:**
- "blog" (çok genel)
- "şey" (belirsiz)
- "aaa" (anlamsız)

---

### **2. İçerik Kalitesi**

Sistem otomatik optimize eder, ama siz de:

- **Spesifik olun:** "finans" yerine "kişisel finans yönetimi"
- **Hedef kitle belirtin:** "yeni başlayanlar için"
- **Lokal context:** "Türkiye'de" ekleyin

---

### **3. Görsel Kullanımı**

**Hero Image:** Her blog'da mutlaka
**Section Images:** 4+ bölüm varsa
**Diagrams:** Teknik konularda
**Social Images:** Paylaşım için

---

## 🚀 Sonraki Adımlar

1. **İlk blogunuzu oluşturun** (yukarıdaki örnekleri deneyin)
2. **10 blog hedefi** koyun (haftada 2-3)
3. **SEO performansını takip edin** (Google Search Console)
4. **İçerikleri güncelleyin** (3-6 ayda bir)
5. **Internal link ağını genişletin**

---

## 💡 İpuçları

- **Batch üretim:** Tek seferde 5-10 blog planlayın, sonra üretin
- **Keyword research önce:** Her zaman önce keyword araştırması yapın
- **Rakip analizi:** Büyük keyword'ler için mutlaka rakip analizi
- **A/B test:** Farklı başlıklar deneyin
- **Internal linking:** Her yeni blog, eski bloglara link ekleyin

---

## 📞 Destek

**Sorun mu var?**

1. Bu README'yi kontrol edin
2. `.suparank-credentials.json` dosyasını inceleyin
3. Log dosyalarını kontrol edin

**Suparank Dokümantasyon:** [Suparank Official Docs]

---

## 📝 Değişiklik Günlüğü

### v1.0 - 2026-01-14
- ✅ Tam otomatik sistem kurulumu
- ✅ Gemini API entegrasyonu
- ✅ Türkçe içerik optimizasyonu
- ✅ 4 otomatik workflow
- ✅ Tool composition yapılandırması

---

**Mutlu blog yazımları! 🎉**
