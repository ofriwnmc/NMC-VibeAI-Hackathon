# 🛠️ מדריך חיבור סביבות עבודה (Lovable + Supabase + GitHub)

בצעו את השלבים הבאים כדי לחבר את "המוח" (Supabase) ל"פנים" (Lovable) של האפליקציה.

### שלב 1: הקמת בסיס נתונים (Supabase)
*מבוצע ע"י נציג אחד מהקבוצה.*

1. היכנסו ל-[Supabase](https://supabase.com) והתחברו עם חשבון ה-GitHub שלכם.
2. לחצו על **New Project**.
3. בחרו את הארגון שיצרתם בהרשמה.
4. **Name:** תנו שם לאפליקציה (באנגלית, ללא רווחים).
5. **Password:** לחצו על "Generate a password" ו**שמרו אותה בצד!**
6. **Region:** בחרו Frankfurt או London (הכי קרוב לישראל).
7. **Pricing Plan:** ודאו שנבחר **Free** ($0).
8. לחצו על **Create new project**.

### שלב 2: חיבור ל-Lovable

1. בזמן ש-Supabase מכין את הפרויקט (זה לוקח דקה), היכנסו ל-Lovable.
2. התחברו (Login) וצרו פרויקט חדש.
3. בתפריט הצד ב-Lovable, חפשו את **Supabase** או **Settings > Integrations**.
4. המערכת תבקש מכם שני מפתחות: **Project URL** ו-**Anon Key**.

### שלב 3: העתקת המפתחות

1. חזרו ל-Supabase.
2. גשו ל-**Project Settings** (אייקון גלגל שיניים למטה) -> **API**.
3. העתיקו את **Project URL** והדביקו ב-Lovable.
4. העתיקו את **Project API keys (anon / public)** והדביקו ב-Lovable.

✅ **זהו! האפליקציה שלכם מחוברת לבסיס נתונים.**

### שלב 4: חיבור ל-GitHub

1. בפינה הימנית העליונה ב-Lovable, לחצו על כפתור GitHub (או Export/Sync).
2. התחברו לחשבון ה-GitHub שלכם.
3. בחרו ברשימה את הפרויקט שיצרתם על בסיס הטמפלייט.
4. לחצו Link Repo (או Push).

✅ סטטוס: הכל מחובר! Lovable יודע לשמור את הקוד ב-GitHub ואת המידע ב-Supabase.
