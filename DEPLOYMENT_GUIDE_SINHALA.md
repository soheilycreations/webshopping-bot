# 🤖 WhatsApp AI බොට් - සම්පූර්ණ සැකසුම් මාර්ගෝපදේශ

**සඳහා:** Soheily Creations ගනුවැසියන්  
**කේතාංක:** 2.0 නිපදනය  
**අවසන් යාවත්කාලීනය:** මැයි 2026

---

## 🤔 මෙම බොට් කුමක්ද?

ස්මාර්ට් WhatsApp සහායකයෙකු එය:
- ගනුවැසി පණිවිඩවලට ස্වයංක්රීයව පිළිතුරු දෙයි (24/7)
- ඔබේ භාණ්ඩ/සේවා ឯකඵrazor් දේ ඉගෙන ගනී
- සිංහල සහ ඉංග්‍රේජි සංවාදනයට ප්‍රතිචාර දක්වයි
- ගනුවැසි සබඳතා ලුහුබඳු කරයි
- කිසිවෙක් පණිවිඩයක් අමතක නොකර විකිණුම් වැඩි කරයි

---

## 💰 මිල ගණන්

| සැලැස්ම | මිල | මාසික පණිවිඩ | ලක්ෂණ |
|------|-------|---|---|
| **සරල** | රු. 3,500 | 1,500 | FAQs විතරක් |
| **සම්මත** | රු. 6,500 | 4,000 | + AI + ឯකඵrazורត + හඬ |
| **ප්‍රිමියම** | රු. 12,500+ | සීමාසં‌ටවත්ව | + බුකින් + බහුවිධ අංක |

---

## 🚀 සැකසුම් කරන්නේ කොහොමද? (පියවර-පියවරින්)

### **අංගය 1: නිදහස් ගිණුම් සෑදුම (මිනිත්තු 5)**

#### පියවර 1: GitHub ගිණුම සෑදුම
1. **github.com** යන්න
2. "Sign up" (ඉහළ දකුණු කෙළවර) click කරන්න
3. ඊ-තැපෑල, මුරපදය ඇතුළු කරන්න
4. ඊ-තැපෑල තහවුරු කරන්න
5. සම්පූර්ණ! ✅

#### පියවර 2: Render ගිණුම සෑදුම
1. **render.com** යන්න
2. "Get started" click කරන්න
3. GitHub සමඟ ලියාපදිංචි වන්න (පහසුම)
4. Render අauthorization කරන්න
5. සම්පූර්ණ! ✅

#### පියවර 3: Supabase ගිණුම සෑදුම
1. **supabase.com** යන්න
2. "Start your project" click කරන්න
3. GitHub සමඟ ලියාපදිංචි වන්න
4. නව ව්‍යාපෘතිය සෑදුම (නම: "whatsapp-bot")
5. තත්පර 2-3 ගිණුම-ගත සඳහා බලා සිටින්න
6. සම්පූර්ණ! ✅

#### පියවර 4: Gemini API key ලබාගන්න
1. **ai.google.dev** යන්න
2. "Get API key" click කරන්න
3. "Create API key" click කරන්න
4. key copy කරන්න (හරියටම copy කරන්න!)
5. ආරක්ෂිතව සংරක්ෂණ කරන්න
6. සම්පූර්ණ! ✅

---

### **අංගය 2: Render එකට යොදිතැබුම (මිනිත්තු 10)**

#### පියවර 1: GitHub මත ව්‍යාපෘතිය fork කරන්න
1. යන්න: **github.com/soheilycreations/whatsapp-platform**
2. "Fork" click කරන්න (ඉහළ දකුණු කෙළවර)
3. fork සම්පූර්ණ වන තුරු බලා සිටින්න
4. දැන් ඔබ ඔබේ own copy තිබේ! ✅

#### පියවර 2: Render එකේ Backend යොදිතැබුම
1. **render.com** යන්න (logged in)
2. "New +" → "Web Service" click කරන්න
3. ඔබේ forked repo තෝරන්න
4. පුරවන්න:
   - **නම:** `whatsapp-bot-backend`
   - **Branch:** `main`
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`
5. "Advanced" click කරන්න → Environment Variables එකතු කරන්න:

```
SUPABASE_URL=https://[your-project].supabase.co
SUPABASE_ANON_KEY=eyJhb...
GEMINI_API_KEY=AIzaSy...
```

(Supabase URL/key එක Supabase dashboard එකෙන් copy කරන්න)

6. "Deploy" click කරන්න
7. මිනිත්තු 3-5 බලා සිටින්න (හරි checkmark = success)
8. Backend URL copy කරන්න (උදාහරණ: `https://whatsapp-bot-backend-xxxx.onrender.com`)
9. සම්පූර්ණ! ✅

#### පියවර 3: Render එකේ Frontend යොදිතැබුම
1. **render.com** → "New +" → "Web Service" යන්න
2. එම forked repo තෝරන්න
3. පුරවන්න:
   - **නම:** `whatsapp-bot-frontend`
   - **Branch:** `main`
   - **Build Command:** `npm install && npm run build`
   - **Start Command:** `next start`
   - **Root Directory:** `frontend`
4. Environment Variable එකතු කරන්න:

```
NEXT_PUBLIC_BACKEND_URL=[your-backend-url]
```

(පියවර 2 එකෙන් Backend URL භාවිතා කරන්න)

5. "Deploy" click කරන්න
6. මිනිත්තු 3-5 බලා සිටින්න
7. Frontend URL copy කරන්න (උදාහරණ: `https://whatsapp-bot-frontend-xxxx.onrender.com`)
8. සම්පූර්ණ! ✅

---

### **අංගය 3: Supabase Database සැකසුම (මිනිත්තු 5)**

#### පියවර 1: SQL සැකසුම run කරන්න
1. **Supabase** → ඔබේ Project → **SQL Editor** යන්න
2. "New query" click කරන්න
3. මෙම SQL copy-paste කරන්න:

```sql
-- Create tables
CREATE TABLE IF NOT EXISTS shops (
  id TEXT PRIMARY KEY,
  name TEXT,
  auto_reply BOOLEAN DEFAULT true,
  created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE IF NOT EXISTS faqs (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  shop_id TEXT REFERENCES shops(id) ON DELETE CASCADE,
  question TEXT NOT NULL,
  answer TEXT NOT NULL,
  keywords TEXT[],
  is_active BOOLEAN DEFAULT true,
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE IF NOT EXISTS messages (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  shop_id TEXT REFERENCES shops(id) ON DELETE CASCADE,
  sender_jid TEXT,
  sender_name TEXT,
  message_text TEXT,
  reply_sent TEXT,
  reply_type TEXT,
  created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE IF NOT EXISTS knowledge_docs (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  shop_id TEXT REFERENCES shops(id) ON DELETE CASCADE,
  file_name TEXT NOT NULL,
  file_type TEXT NOT NULL,
  content TEXT NOT NULL,
  created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE TABLE IF NOT EXISTS shop_settings (
  shop_id TEXT PRIMARY KEY REFERENCES shops(id) ON DELETE CASCADE,
  shop_name TEXT,
  location TEXT,
  address TEXT,
  working_hours TEXT,
  contact_numbers TEXT[],
  language TEXT DEFAULT 'sinhala',
  updated_at TIMESTAMPTZ DEFAULT NOW()
);

-- Create indexes
CREATE INDEX IF NOT EXISTS idx_faqs_shop ON faqs(shop_id);
CREATE INDEX IF NOT EXISTS idx_messages_shop ON messages(shop_id);
CREATE INDEX IF NOT EXISTS idx_docs_shop ON knowledge_docs(shop_id);

-- Insert default shop
INSERT INTO shops (id, name) VALUES ('shop_123', 'My Shop')
ON CONFLICT (id) DO NOTHING;
```

4. "Run" click කරන්න
5. සම්පූර්ණ! ✅

---

### **අංගය 4: WhatsApp සংයුක්ත කරන්න (මිනිත්තු 2)**

1. Frontend URL open කරන්න (Deploy පියවර 3 එකෙන්)
2. **"Connect Bot"** පිටුවට යන්න
3. **"Start Session"** click කරන්න
4. WhatsApp දුරකතනය සමඟ QR code scan කරන්න
5. "WhatsApp connected ✓" බලා සිටින්න
6. සම්පූර්ණ! ✅

---

## 📚 භාවිතා කරන්නේ කොහොමද?

### **Dashboard - ඔබේ සංඛ්‍යාලේඛන බලන්න**
- අදට礼 පණිවිඩ: සংඛ්‍යාව
- සතිය: සම්පූර්ණ ගණන
- active ගනුවැසි: අනන්‍ය ගණන
- පිළිතුර අනුපාතය: % එකක්

### **Knowledge Base - බොට් ඉගෙන දෙන්න**

**FAQs Tab:**
1. "Add FAQ" click කරන්න
2. ඇතුළු කරන්න: ප්‍රශ්නය, පිළිතුර, Keywords (comma separated)
3. "Save" click කරන්න
4. බොට් ඒවා ඉක්මන් පිළිතුරු සඳහා භාවිතා කරනු ඇත

**Documents Tab:**
1. Upload කරන්න: PDF, Excel, Word, CSV
2. බොට් ස්වයංක්‍රීයව කියවයි සහ ඉගෙන ගනී
3. භාවිතයි: භාණ්ඩ catalogue, මිල ලැයිස්තුව, සේවා

### **Messages - සංවාද බලන්න**
- සෑම ගනුවැසි පණිවිඩයක් පෙන්වයි
- කුමන පිළිතුර ලැබුණි බලන්න (keyword vs AI)
- සංවාද ලුහුබඳු කරන්න

### **Settings - customize කරන්න**
- කඩ නම සහ ස්ථානය
- සිටින පෙන්න වේල
- සම්බන්ධ අංක
- මුරපදය වෙනස් කරන්න

---

## 🤖 AI කිරුණු ක්‍රියා කරන්නේ කොහොමද?

```
ගනුවැසි පණිවිඩ එවයි
        ↓
බොට් බලයි: මෙය FAQ keyword ද?
        ↓ ඔව් → FAQ පිළිතුර එවන්න
        ↓ නැහැ → Gemini AI ඉල්ලන්න
        ↓
Gemini කියවයි: FAQs + ඔබේ ཁྱེ‌nt
        ↓
ගනුවැසි භාෂාවෙන් ස්මාර්ට් පිළිතුර ජනිතයි
        ↓
WhatsApp පිළිතුර එවයි (වාක්‍ය 2-4)
```

---

## 📝 එකතු කිරීමට උදාහරණ FAQs

**ප්‍රශ්නය: ඔබේ මිල කුමක්ද?**  
**පිළිතුර:** අපේ මිල රු. 3,500/මාසින් සිට ඉරඳුම් කරයි. අපට සරල, සම්මත සහ ප්‍රිමියම සැලැස්ම තිබේ. විස්තර සඳහා අපට අමතරණ කරන්න!  
**Keywords:** මිල, වියදම, කීයද, අගය, ගෙවීම

**ප්‍රශ්නය: ඔබ බෙදා දෙන්නේද?**  
**පිළිතුර:** ඔව්! අපි [ඔබේ නගරය] පුරා බෙදා දෙමු. බෙදා දීම දින 1-3 ගතවේ ස්ථානය අනුව.  
**Keywords:** බෙදා දීම, නැව්, බෙදා දීම, ඇණවුම

**ප්‍රශ්නය: ඔබේ වැඩ කරන පෙන්වා වේල කුමක්ද?**  
**පිළිතුර:** අපි සকාල 9 සිට සන්ධ්‍යා 6 දක්වා විවෘතයි, සඳුදා සිට සිකුරාදා දක්වා. සති අන්තයේ වසා ඇත.  
**Keywords:** පෙන්වා වේල, විවෘත, වසා, సमय, එවිට

---

## 📄 Upload කිරීමට උදාහරණ ઍकᠠ‌ment

**උපයුක්ත ফائل upload කිරීමට:**
1. **භාණ්ඩ catalogue** (PDF/Excel) - නම, මිල, විස්තර සහිතව
2. **මිල ලැයිස්තුව** (Excel/CSV) - ඔබේ සෑම භාණ්ඩයක් සහ මිල
3. **සේවා ලැයිස්තුව** (Word/PDF) - ඔබ ඉදිරිපත් කරන සේවා
4. **FAQ document** - ගනුවැසි සඳහා සාමාන්‍ය ප්‍රශ් න

**Excel ফाইล ගෙනඒ විධිය:**

| භාණ්ඩය | මිල | විස්තර |
|---------|-------|---|
| රතු T-Shirt | රු. 1,500 | 100% cotton, sizes S-XXL |
| කළු Jeans | රු. 3,500 | Denim, සෑම size |

Upload කරන්න → බොට් ස්වයංක්‍රීයව ඉගෙන ගනී! 🤖

---

## 💬 උදාහරණ සංවාද

**ගනුවැසි:** "මට ගිණුම තියෙනවද?"  
**බොට්:** "ඔබ ඉන්දිකා ගිණුම ගතයි. අද වන විට ඔබට Rs. 2,450 ක් ගෙවිය යුතුයි. කිසිවෙක් තිබුණොත් අපට හඳුන්වන්න! 😊"

**ගනුවැසි:** "What's the price?"  
**බොට්:** "We have products from Rs. 500 to Rs. 5,000. What category are you interested in? 👕👖"

---

## ⚠️ සාමාන්‍ය ගැටලු සහ නිරාකරණ

### **ගැටලු: QR code scan නොවෙයි**
**නිරාකරණය:** 
- දුරකතන ကamera සිට WhatsApp භාවිතා කරන්න
- කැමරාවට ලුහුබඳු ආලෝකය තිබේද බලන්න
- QR තත්පර 30 පසු ඉකුත් වේ (rescan කරන්න)

### **ගැටලු: බොට් පිළිතුරු නොදෙයි**
**නිරාකරණය:**
- පරීක්ෂා කරන්න: Auto-Reply ON (Settings)
- පරීක්ෂා කරන්න: Knowledge Base FAQs හෝ ઈkumenti තිබේද
- පරීක්ෂා කරන්න: WhatsApp "connected" පෙන්වයි ✓
- තත්පර 10-15 බලා සිටින්න (Render free tier slow)

### **ගැටලු: වැරදි භාෂාවෙන් පිළිතුරු**
**නිරාකරණය:**
- බොට් භාෂාව ස්වයංක්‍රීයව හඳුනා ගනී
- වැරදි නම්, FAQs දෙම භාෂාවෙන් එකතු කරන්න

### **ගැටලු: Render "Not found" කියයි**
**නිරාකරණය:**
- URLs ճეղ බලන්න
- Deploy පසු මිනිත්තු 5 බලා සිටින්න
- බ්‍රව්සරයි නැවුම් කරන්න (Ctrl+F5)

---

## 🔒 වැදගත - ආරක්ෂිතව තබාගන්න

- ✅ ඔබේ **Gemini API key** ආරක්ෂිතව සংරක්ෂණ කරන්න
- ✅ ඔබේ **Supabase credentials** ආරක්ෂිතව සংරක්ෂණ කරන්න
- ✅ ամ ամ මුරපදය වෙනස් කරන්න (Settings පිටුව)
- ✅ පෙබෙසු චැට්‌වලින් link කරන්න එපා
- ✅ නිතිපතා backup: Dashboard එකෙන් පණිවිඩ බාගාගන්න

---

## 📞 සහාය සහ FAQ

**ප්‍රශ්නය: මට ඔබේ WhatsApp අංකය භාවිතා කරන්න පුළුවන්ද?**  
**පිළිතුරු:** ඔව්! බොට්ට විශේෂ අංකයක් අවශ්‍ය නැත. ඕනෑම WhatsApp ගිණුම භාවිතා කරයි.

**ප්‍රශ්නය: බොට් මගේ පෞද්ගලික චැට්‍ය බලනවද?**  
**පිළිතුරු:** නැහැ! බොට් ගනුවැසි පණිවිඩවලට විතරක් පිළිතුරු දෙයි. පෞද්ගලික චැට්‍ය පෞද්ගලිකයි.

**ප්‍රශ්නය: බොට් පිළිතුරු customize කරන්න පුළුවන්ද?**  
**පිළිතුරු:** ඔව්! FAQs සහ ඔබේ ઍkumenti upload කිරීම මගින්.

**ප්‍රශ්නය: බොට්ට internet ස්ފอɗ කිපයිද?**  
**පිළිතුරු:** ખමार අඩුයි. පණිවිඩ එවා ගතයි විතරක්. ~1MB per 1000 පණිවිඩ.

**ප්‍රශ්නය: බොට් තාවකාලිකව නැවතිම්විම පුළුවන්ද?**  
**පිළිතුරු:** ඔව්! Settings එකෙන් "Auto-Reply" OFF කරන්න.

**ප්‍රශ්නය: බහුවිධ භාෂා සඳහා?**  
**පිළිතුරු:** ඔව්! සිංහල, ඉංග්‍රේජි, තමිල්. බොට් ස්වයංක්‍රීයව හඳුනා ගනී.

---

## 🎓 ඊළඟ පියවර

1. **සැකසුම සම්පූර්ණ කරන්න** (ඉහතින් සෑම අංගයක්)
2. **FAQs එකතු කරන්න** (අවම වශයෙන් 5-10)
3. **ઍkumenti upload කරන්න** (බාණ්ඩ ලැයිස්තුව හෝ මිල ලැයිස්තුව)
4. **පරීක්ෂා කරන්න** - WhatsApp එකෙන් බොට්ට පණිවිඩ එවන්න
5. **Monitor කරන්න** - Dashboard සංඛ්‍යාලේඛන දිනපතා බලන්න
6. **Optimize කරන්න** - "Top Questions" ඉතින් තවත් FAQs එකතු කරන්න

---

## 📧 Soheily Creations අමතරණ කරන්න

**WhatsApp:** +94 77X XXX XXXX  
**ඊ-තැපෑල:** hello@soheilycreations.lk  
**බෙදා:** soheilycreations.lk

---

**❤️ සමඟින් Soheily Creations විසින් ගතයි**  
*"Build Smart · Grow Fast"*
