# 🤖 WhatsApp AI Bot Platform - Complete Setup Guide

**For: Soheily Creations Clients**  
**Version:** 2.0 Production  
**Last Updated:** May 2026

---

## 📱 What is This Bot?

A smart WhatsApp AI assistant that:
- Replies to customer messages automatically (24/7)
- Learns from your product/service documents
- Handles Sinhala & English conversations
- Tracks customer interactions
- Increases sales by never missing a message

---

## 💰 Pricing

| Plan | Price | Messages/Month | Features |
|------|-------|---|---|
| **Basic** | Rs. 3,500 | 1,500 | FAQs only |
| **Standard** | Rs. 6,500 | 4,000 | + AI + Documents + Voice |
| **Pro** | Rs. 12,500+ | Unlimited | + Booking + Multiple numbers |

---

## 🚀 How to Set Up (Step-by-Step)

### **Phase 1: Create Free Accounts (5 minutes)**

#### Step 1: Create GitHub Account
1. Go to **github.com**
2. Click "Sign up" (top right)
3. Enter email, create password
4. Verify email
5. Done! ✅

#### Step 2: Create Render Account
1. Go to **render.com**
2. Click "Get started"
3. Sign up with GitHub (easiest)
4. Authorize Render
5. Done! ✅

#### Step 3: Create Supabase Account
1. Go to **supabase.com**
2. Click "Start your project"
3. Sign up with GitHub
4. Create new project (name: "whatsapp-bot")
5. Wait 2-3 minutes for database setup
6. Done! ✅

#### Step 4: Get Gemini API Key
1. Go to **ai.google.dev**
2. Click "Get API key"
3. Click "Create API key"
4. Copy the key (හරියටම copy කරන්න!)
5. Save somewhere safe
6. Done! ✅

---

### **Phase 2: Deploy to Render (10 minutes)**

#### Step 1: Fork Project on GitHub
1. Go to: **github.com/soheilycreations/whatsapp-platform**
2. Click "Fork" (top right)
3. Wait for fork to complete
4. You now have your own copy! ✅

#### Step 2: Deploy Backend on Render
1. Go to **render.com** (logged in)
2. Click "New +" → "Web Service"
3. Select your forked repo
4. Fill in:
   - **Name:** `whatsapp-bot-backend`
   - **Branch:** `main`
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`
5. Click "Advanced" → Add Environment Variables:

```
SUPABASE_URL=https://[your-project].supabase.co
SUPABASE_ANON_KEY=eyJhb...
GEMINI_API_KEY=AIzaSy...
```

(Supabase URL/key එක Supabase dashboard එකෙන් copy කරන්න)

6. Click "Deploy"
7. Wait 3-5 minutes (green checkmark = success)
8. Copy backend URL (example: `https://whatsapp-bot-backend-xxxx.onrender.com`)
9. Done! ✅

#### Step 3: Deploy Frontend on Render
1. Go to **render.com** → "New +" → "Web Service"
2. Select same forked repo
3. Fill in:
   - **Name:** `whatsapp-bot-frontend`
   - **Branch:** `main`
   - **Build Command:** `npm install && npm run build`
   - **Start Command:** `next start`
   - **Root Directory:** `frontend`
4. Add Environment Variable:

```
NEXT_PUBLIC_BACKEND_URL=[your-backend-url]
```

(Use backend URL from Step 2)

5. Click "Deploy"
6. Wait 3-5 minutes
7. Copy frontend URL (example: `https://whatsapp-bot-frontend-xxxx.onrender.com`)
8. Done! ✅

---

### **Phase 3: Setup Supabase Database (5 minutes)**

#### Step 1: Run SQL Setup
1. Go to **Supabase** → Your Project → **SQL Editor**
2. Click "New query"
3. Copy-paste this SQL:

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

4. Click "Run"
5. Done! ✅

---

### **Phase 4: Connect WhatsApp (2 minutes)**

1. Open frontend URL in browser (from Deploy Step 3)
2. Go to **"Connect Bot"** page
3. Click **"Start Session"**
4. Scan QR code with WhatsApp phone
5. Wait for "WhatsApp connected ✓"
6. Done! ✅

---

## 📚 How to Use

### **Dashboard - See your stats**
- Today's messages: බහු
- This week: සම්පූර්ණ සංඛ්යාව
- Active customers: අദ්විතීය ගણන
- Reply rate: % එකක්

### **Knowledge Base - Teach the bot**

**FAQs Tab:**
1. Click "Add FAQ"
2. Enter: Question, Answer, Keywords (comma separated)
3. Click "Save"
4. Bot will use these for quick replies

**Documents Tab:**
1. Upload: PDF, Excel, Word, CSV
2. Bot automatically reads & learns
3. Use for: Product catalog, price list, services

### **Messages - See conversations**
- All customer messages appear here
- See which got replies (keyword vs AI)
- Track conversations

### **Settings - Customize**
- Shop name & location
- Working hours
- Contact numbers
- Change password

---

## 🤖 How the AI Works

```
Customer sends message
        ↓
Bot checks: Is this a FAQ keyword?
        ↓ Yes → Send FAQ answer
        ↓ No → Ask Gemini AI
        ↓
Gemini reads: FAQs + your documents
        ↓
Generate smart reply in customer's language
        ↓
Send WhatsApp reply (2-4 sentences)
```

---

## 📝 Example FAQs to Add

**Q: What are your prices?**  
**A:** Our prices start from Rs. 3,500/month. We have Basic, Standard, and Pro plans. Contact us for details!  
**Keywords:** price, cost, how much, value, payment

**Q: Do you deliver?**  
**A:** Yes! We deliver across [your city]. Delivery takes 1-3 days depending on location.  
**Keywords:** delivery, ship, deliver, order

**Q: What's your working hours?**  
**A:** We're open 9 AM to 6 PM, Monday to Friday. Closed on weekends.  
**Keywords:** hours, open, closed, timing, when

---

## 📄 Upload Documents Example

**Best files to upload:**
1. **Product catalog** (PDF/Excel) - with names, prices, descriptions
2. **Price list** (Excel/CSV) - all your products & prices
3. **Service list** (Word/PDF) - services you offer
4. **FAQ document** - common questions customers ask

**How to make Excel file:**

| Product | Price | Description |
|---------|-------|---|
| Red T-Shirt | Rs. 1,500 | 100% cotton, sizes S-XXL |
| Black Jeans | Rs. 3,500 | Denim, all sizes |

Upload this → Bot learns automatically! 🤖

---

## 💬 Example Conversations

**Customer:** "මට ගිණුම තියෙනවද?"  
**Bot:** "ඔබ ඉන්දිකා ගිණුම ගතයි. අද වන විට ඔබට Rs. 2,450 ක් ගෙවිය යුතුයි. කිසිවෙක් තිබුණොත් අපට හඳුන්වන්න! 😊"

**Customer:** "What's the price?"  
**Bot:** "We have products from Rs. 500 to Rs. 5,000. What category are you interested in? 👕👖"

---

## ⚠️ Common Issues & Fixes

### **Issue: QR code not scanning**
**Fix:** 
- Use WhatsApp from phone camera
- Make sure camera has good light
- QR expires after 30 seconds (rescan)

### **Issue: Bot not replying**
**Fix:**
- Check: Auto-Reply is ON (Settings)
- Check: Knowledge Base has FAQs or documents
- Check: WhatsApp shows "connected" ✓
- Wait 10-15 seconds (Render free tier is slow)

### **Issue: Wrong language reply**
**Fix:**
- Bot detects language automatically
- If wrong, add FAQ in both languages

### **Issue: Render says "Not found"**
**Fix:**
- Check URLs are correct
- Wait 5 minutes after deploy
- Refresh browser (Ctrl+F5)

---

## 🔒 Important - Keep Safe

- ✅ Save your **Gemini API key** somewhere safe
- ✅ Save your **Supabase credentials** somewhere safe
- ✅ Change password monthly (Settings page)
- ✅ Don't share links in public chats
- ✅ Regular backup: Download messages from dashboard

---

## 📞 Support & FAQ

**Q: Can I use my own WhatsApp number?**  
A: Yes! The bot doesn't need special number. Uses any WhatsApp account.

**Q: Does bot see my personal chats?**  
A: No! Bot only replies to customer messages. Personal chats are private.

**Q: Can I customize bot responses?**  
A: Yes! Through FAQs and by uploading your documents.

**Q: How much internet does bot use?**  
A: Very little. Only sends/receives messages. ~1MB per 1000 messages.

**Q: Can I pause the bot?**  
A: Yes! Turn off "Auto-Reply" in Settings.

**Q: Multi-language support?**  
A: Yes! Sinhala, English, Tamil. Bot auto-detects.

---

## 🎓 Next Steps

1. **Complete Setup** (follow all 4 phases above)
2. **Add FAQs** (at least 5-10)
3. **Upload Documents** (product list or price list)
4. **Test** - Send message to bot from WhatsApp
5. **Monitor** - Check Dashboard stats daily
6. **Optimize** - Add more FAQs based on "Top Questions"

---

## 📧 Contact Soheily Creations

**WhatsApp:** +94 77X XXX XXXX  
**Email:** hello@soheilycreations.lk  
**Website:** soheilycreations.lk

---

**Built with ❤️ by Soheily Creations**  
*"Build Smart · Grow Fast"*
