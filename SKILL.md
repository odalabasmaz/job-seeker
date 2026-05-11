---
name: job-evaluator
description: Şirket adı veya web sitesi verilerek, Orhun Dalabasmaz'ın kariyer profili ve beklentilerine göre kapsamlı iş değerlendirme raporu üretir. Glassdoor, Kununu, Levels.fyi, LinkedIn ve Remotely.de kaynaklarını tarar. Kullanıcı bir veya birden fazla şirket adı veya URL verdiğinde, iş ilanı araştırması yaptığında, "bu şirketi değerlendir", "buraya başvurayım mı", "maaş ne kadar verir", "çalışan yorumları nasıl" gibi ifadeler kullandığında bu skill'i kullan.
---

# Job Evaluator Skill

Bu skill, Orhun Dalabasmaz'ın iş arama sürecinde şirketleri hızlıca değerlendirmek için kullanılır.

## Aday Profili (Sabit - Her raporda kullan)

- **İsim:** Orhun Dalabasmaz
- **Deneyim:** 15+ yıl
- **Mevcut Rol:** Principal Engineer @ Atlassian, Münih
- **Hedef Roller:** Principal Engineer, Staff Engineer, SRE, Engineering Manager, Solutions Architect, Team Lead
- **Öncelik:** Rol türünden çok ücret ve iş içeriği
- **Teknik Stack:** Java/Kotlin, Python, Spring, AWS (Neptune, EKS, DynamoDB, SQS, Lambda, KMS, S3, CloudFormation), Docker, Kubernetes, Microservices, Kafka, Grafana, Splunk, Datadog, Neo4j, Gremlin/Cypher, CI/CD (Bitbucket/Jenkins), MCP, Claude/Gemini AI entegrasyonları
- **Uzmanlık:** SRE, DevOps, Cloud Architecture (AWS odaklı), Distributed Systems, People Management, Technical Leadership, Roadmap Planning, Cross-functional Collaboration, FedRAMP/SOC2/GDPR Compliance
- **Cloud Tercihi:** AWS (multi-cloud kabul)
- **Çalışma Modeli:** Remote (her yer) VEYA Hybrid/On-site (yalnızca Münih)
- **İstihdam:** Full-time
- **Maaş:** Minimum 120.000 € base + equity/hisse senedi tercihli
- **On-call:** Kabul edilebilir
- **Seyahat:** Az miktarda kabul (konferans, ofis ziyareti)
- **People Management:** Fark etmez (IC veya EM)
- **Sektör:** SaaS/Cloud öncelikli, diğer sektörlere açık
- **Dil:** İş dili İngilizce olmalı (Almanca zorunlu değil)

---

## Araştırma Adımları

Kullanıcı şirket adı veya URL verdiğinde şu kaynakları web_search ile tara:

1. **Glassdoor:** `[şirket adı] Glassdoor reviews` → Genel puan, CEO onayı, tavsiye oranı, pro/con yorumlar
2. **Kununu:** `[şirket adı] Kununu Bewertungen` → Alman pazarı çalışan yorumları
3. **Levels.fyi:** `[şirket adı] levels.fyi engineer salary Germany` → Maaş verileri
4. **LinkedIn:** `[şirket adı] Principal Engineer SRE jobs Munich` → Açık pozisyonlar
5. **Remotely.de:** `[şirket adı] remotely.de` → Remote iş ilanları
6. **Genel:** `[şirket adı] employee benefits Germany equity RSU` → Yan haklar

Bulunamayan veriler için "veri bulunamadı" yaz, **asla tahmin etme**.

---

## Rapor Formatı

Her şirket için aşağıdaki Türkçe raporu üret:

---

### 🏢 [ŞİRKET ADI]
**Sektör:** | **Büyüklük:** | **Merkez:** | **Çalışma Modeli:**

#### ⚡ HIZLI BAKIŞ
| Kriter | Değer | Kaynak |
|--------|-------|--------|
| Glassdoor Puanı | X.X / 5 | Glassdoor |
| Kununu Puanı | X.X / 5 | Kununu |
| CEO Onay Oranı | %XX | Glassdoor |
| Tavsiye Eder mi? | %XX | Glassdoor/Kununu |
| Maaş Rekabetçiliği | ⭐⭐⭐⭐⭐ | Levels.fyi/Glassdoor |

#### 💰 MAAŞ & PAKET
- **Hedef Rol Base Maaş:** (Kaynak belirt)
- **Equity/Hisse:** RSU / ESOP / Stock options var mı?
- **Bonus:** Yapısı nedir?
- **Yan Haklar:** Sağlık, emeklilik, eğitim bütçesi, ekipman vb.

#### ✅ ARTILARI
(Çalışan yorumlarından — en sık tekrarlananlar)
- ...

#### ❌ EKSİLERİ
(Çalışan yorumlarından — en sık tekrarlananlar)
- ...

#### 🎯 ADAY PROFİLİNE UYGUNLUK
| Kriter | Durum | Notlar |
|--------|-------|--------|
| Teknik Stack (AWS, Java/Kotlin, K8s) | ✅/⚠️/❌ | |
| Hedef Rol Mevcut mu? | ✅/⚠️/❌ | |
| Çalışma Modeli (Remote/Hybrid-Münih) | ✅/⚠️/❌ | |
| Maaş 120k+ Base | ✅/⚠️/❌ | |
| Equity Var mı? | ✅/⚠️/❌ | |
| İngilizce Çalışma Ortamı | ✅/⚠️/❌ | |
| Engineering/IC Kültürü | ✅/⚠️/❌ | |

#### 🔗 KAYNAKLAR & AÇIK POZİSYONLAR
- 🔍 Glassdoor: [link]
- 🔍 Kununu: [link]
- 💰 Levels.fyi: [link]
- 💼 LinkedIn İlanları: [bulunan pozisyonlar]
- 🌐 Remotely.de: [bulunan pozisyonlar]

#### 🏁 GENEL DEĞERLENDİRME
**Karar:** 🟢 BAŞVUR | 🟡 ARAŞTIR | 🔴 ATLA

**Gerekçe:** (2-3 cümle özet — neden bu karar?)

---

## Birden Fazla Şirket

Kullanıcı birden fazla şirket verdiyse, raporların sonuna karşılaştırma tablosu ekle:

### 📊 KARŞILAŞTIRMA TABLOSU
| Şirket | Glassdoor | Maaş Uyumu | Stack Uyumu | Model Uyumu | Karar |
|--------|-----------|------------|-------------|-------------|-------|
| ... | | | | | 🟢/🟡/🔴 |

---

## Önemli Notlar

- Rapor **Türkçe** yazılır
- Eksik veri için "veri bulunamadı" yaz, tahmin etme
- Maaş kıyaslamasında 120k € base eşik olarak kullan
- Equity önemli: RSU/ESOP yoksa ⚠️ işaretle
- Remote ise her şehir kabul; hybrid/on-site ise sadece Münih kabul
