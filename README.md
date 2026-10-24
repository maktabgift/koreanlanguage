# Korean Master AI — Vercel'ga joylash

Papka tarkibi:
- index.html — ilovaning o'zi
- api/feedback.js — AI javoblari uchun server funksiyasi (API kalit shu yerda saqlanadi)

## 1-usul: GitHub orqali (tavsiya etiladi)
1. github.com da yangi repository yarating (masalan, korean-master-ai).
2. "Add file → Upload files" orqali index.html va api/feedback.js ni yuklang. api papkasi ichida bo‘lsin.
3. vercel.com ga GitHub hisobi bilan kiring. "Add New → Project" ni bosing, repository ni tanlang va "Import" qiling.
4. Framework Preset: "Other". Build sozlamalariga tegmang, "Deploy" ni bosing.
5. Deploy tugagach: Settings → Environment Variables bo‘limida Name: ANTHROPIC_API_KEY, Value: console.anthropic.com dan olingan kalit. Saqlang.
6. Deployments bo‘limida oxirgi deploy ustida "Redeploy" ni bosing (yangi kalit ishlashi uchun).
7. Berilgan https://...vercel.app manzilini oching.

## 2-usul: Vercel CLI (kompyuterda)
    npm i -g vercel
    cd korean-master-ai
    vercel login
    vercel --prod
Keyin 5–6-bosqichlarni bajaring (kalit va Redeploy).

## Telefonga o‘rnatish
- Android (Chrome): ⋮ menyu → "Bosh ekranga qo‘shish".
- iPhone (Safari): Ulashish (□↑) → "Bosh ekranga qo‘shish".
Hozircha bu oddiy yorliq. Oflayn rejim va to‘liq ilova sifatida o‘rnatish keyingi bosqich.

## Muhim
- ANTHROPIC_API_KEY ni hech kimga va hech qayerga (chatga ham) yubormang.
- /api/feedback manzili ochiq. Kalit sarfini cheklash uchun keyinroq parol yoki so‘rov limiti qo‘shish kerak.
- Model: ANTHROPIC_MODEL o‘zgaruvchisi bilan o‘zgartirish mumkin (standart: claude-haiku-5-5).
- Progress (lug‘at, test, AI tarixi) har bir manzilda alohida saqlanadi: claude.ai dagi va Vercel dagi nusxalar bir-biridan farq qiladi.
- Ovoz tanish (mikrofon) faqat HTTPS da ishlaydi. Vercel manzili HTTPS.
