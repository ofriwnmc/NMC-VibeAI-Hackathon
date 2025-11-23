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
4. חיבור ידני: המערכת תבקש מכם שני מפתחות: **Project URL** ו-**Anon Key**. (הנחיות בשלב 3) 
5. חיבור אוטומטי: יכול להיות שהמערכת תזהה את חשבון הSUPABASE שלכם ולכן תאפשר לכם לבחור מתוך רשימה את הפרוייקט הרלוונטי ותבקש הרשאה לפרוייקט זה ויקשר אליו אוטומטית (לאחר שאתם ניגשים לאפשרות האינטגרציה עם SUPABASE, זה לא יקרה אם לא תגדירו זאת באינטגרציות). 

### שלב 3: העתקת המפתחות
במידה והתבקשתם לחבר ידנית את Supabase:
1. חזרו ל-Supabase.
2. גשו ל-**Project Settings** (אייקון גלגל שיניים למטה).
3. העתיקו את **Project URL** (נמצא בDATA API) והדביקו ב-Lovable .
4. העתיקו את **Project API keys (anon / public)** (נמצא ב  API KEYS -> Legacy API keys) והדביקו ב-Lovable.

### דגשים לגבי חיבור לSupabase:
1. כאשר נרצה לעשות פעולה אשר שומרת או משפיעה על מידע נדגיש לLOVABLE שאנחנו רוצים שימוש בSUPABASE כך שישמור את הנתונים בטבלאות רלוונטיות והמידע באמת ישמר ולא ישמר בזיכרון זמני ומקומי שלא יהיה רלוונטי להמשך השימוש בעתיד.
2. גשו לSupabase וודאו כי הטבלאות נוצרות בפועל כדי לוודא את החיבור שלכם (עשו זאת בתחילת העבודה כדי לוודא שהכל נשמר כמו שצריך ולחסוך עבודה כפולה בהמשך).
 שימו לב יש שני מקומות בהם יכול להתעדכן מידע בSupabase-
  כדי לראות מי נרשם (אימייל, התחברות אחרונה): תפריט צד שמאל > Authentication.
  כדי לראות את הנתונים עצמם (שמות, טפסים, פרופילים, מידע): תפריט צד שמאל > Table Editor.
3. מה לעשות אם עשינו פעולה על נתונים והמידע לא מתעדכן בsupabase:
   דבר ראשון וודאו כי ביצעתם פעולה שבאמת משפיעה על מידע ונסו לממש אותה (למשל אם יצרתם עמוד הרשמה והתחברות - רישמו משתמש כדי שיהיה מידע שנצפה לו בטבלאות בsupabase)
   אם ביצעתם פעולה כזו ואינכם רואים מידע מעודכן השתמשו בפרומפט הבא כדי לעדכן את פרטי החיבור ולוודא שהLOVABLE שולח את המידע ליעד הנכון:

I need to manually override the Supabase credentials because the automatic connection is not working as expected.
Please hardcode or update the environment variables with these EXACT credentials:
Supabase URL: [הכנס את הPROJECT URL נמצא בDATA API]
Anon Key: [הכנס את הAnon Key (נמצא בAPI KEYS --->LEGACY API KEYS)]
Action required:
Update the supabaseClient.ts (or wherever the client is initialized) to use THESE values explicitly.
Stop using mock data.
Redeploy/Refresh the app so I can test the connection
בצעו מחדש את פעולת שמירת הנתונים ובדקו פעם נוספת את המידע בsupabase וודאו כי כעת הוא נשמר- אם לא פנו לעזרה מהמדריך. 

✅ **זהו! האפליקציה שלכם מחוברת לבסיס נתונים.**

### שלב 4: חיבור ל-GitHub

1.  בתפריט הצד ב-Lovable, חפשו את **GitHub** או **Settings > Integrations**.
2. התחברו לחשבון ה-GitHub שלכם.
3. בחרו ברשימה את הפרויקט שיצרתם על בסיס הטמפלייט.

שימו לב עדכון הקוד בגיטהאב הוא לא אוטומטי הוא יקרה כאשר תלחצו על האייקון של גיטהאב שנמצא בצד הימני העליון של המסך "sync your project to GitHu"
מתי נבצע את הסנכרון? כל פעם שמשהו עובד- יצרתם יכולת חדשה במערכת? וידאתם שהיא עובדת כמו שצריך ואין באגים? בצעו סנכרון כדי לשמור את הקוד התקין!

✅ סטטוס: הכל מחובר! Lovable יודע לשמור את הקוד ב-GitHub ואת המידע ב-Supabase.
