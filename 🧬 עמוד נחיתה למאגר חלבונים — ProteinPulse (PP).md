# 🧬 עמוד נחיתה למאגר חלבונים — **ProteinPulse (PP)**

📅 לועזי: 16.11.2025
📅 עברי: כ״ד בחשוון תשפ״ו
⏰ שעה: 14:20 (ישראל)

---

## 🧱 מה קיבלת כאן?

להלן עמוד HTML מלא (`index.html`) שתוכל לשים בתוך המאגר
[`ProteinPulse`](https://github.com/AnLoMinus/ProteinPulse/) ולהציג ב־GitHub Pages או כתצוגת תוכן במאגר עצמו.

העמוד:

* מסך מלא, מעוצב, קומפקטי ונקי.
* כולל מקטע Hero, הסבר קצר על חלבון, וטבלאות השוואה לחלבון מן החי, הצומח ומוצרי חלב.
* משתמש באמוג׳ים, בצבעי רקע רכים וקונטרסט טוב לקריאה.

---

## 💻 קובץ `index.html` מוכן להדבקה

```html
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ProteinPulse • מאגר חלבונים</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #ffeef6 0, #f5f7ff 40%, #edf4ff 100%);
      color: #111827;
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      padding: 1.2rem 1.8rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      backdrop-filter: blur(14px);
      background: linear-gradient(to left, rgba(255,255,255,0.9), rgba(239,246,255,0.9));
      border-bottom: 1px solid rgba(148,163,184,0.35);
      position: sticky;
      top: 0;
      z-index: 20;
    }

    .logo {
      font-weight: 800;
      letter-spacing: 0.03em;
      font-size: 1.15rem;
      display: flex;
      align-items: center;
      gap: 0.35rem;
    }

    .logo span {
      padding: 0.08rem 0.55rem;
      border-radius: 999px;
      font-size: 0.7rem;
      border: 1px solid rgba(148,163,184,0.6);
      background: rgba(255,255,255,0.9);
    }

    .nav-links {
      display: flex;
      gap: 0.8rem;
      font-size: 0.85rem;
      color: #4b5563;
    }

    .nav-links a {
      padding: 0.3rem 0.7rem;
      border-radius: 999px;
      border: 1px solid transparent;
      transition: 150ms ease;
    }

    .nav-links a:hover {
      border-color: rgba(148,163,184,0.7);
      background: rgba(255,255,255,0.95);
    }

    main {
      flex: 1;
      padding: 2rem 1.4rem 3rem;
      max-width: 1080px;
      margin: 0 auto;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.6fr) minmax(0, 1.2fr);
      gap: 2rem;
      align-items: center;
      margin-bottom: 3rem;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 0.45rem;
      padding: 0.2rem 0.65rem;
      border-radius: 999px;
      background: rgba(255,255,255,0.9);
      border: 1px solid rgba(148,163,184,0.5);
      font-size: 0.78rem;
      color: #4b5563;
      margin-bottom: 0.7rem;
    }

    .hero-title {
      font-size: clamp(2.1rem, 4vw, 2.7rem);
      font-weight: 800;
      margin-bottom: 0.7rem;
      color: #020617;
    }

    .hero-title span {
      background: linear-gradient(135deg, #2563eb, #ec4899, #f97316);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-sub {
      font-size: 0.98rem;
      color: #4b5563;
      margin-bottom: 1.2rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      margin-bottom: 1rem;
    }

    .btn-primary,
    .btn-ghost {
      padding: 0.55rem 1.1rem;
      border-radius: 999px;
      font-size: 0.9rem;
      border: 1px solid transparent;
      cursor: pointer;
      transition: 160ms ease;
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }

    .btn-primary {
      background: linear-gradient(135deg, #2563eb, #ec4899);
      color: #f9fafb;
      box-shadow: 0 12px 30px rgba(37,99,235,0.35);
    }

    .btn-primary:hover {
      filter: brightness(1.05);
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(37,99,235,0.4);
    }

    .btn-ghost {
      background: rgba(255,255,255,0.9);
      border-color: rgba(148,163,184,0.7);
      color: #111827;
    }

    .btn-ghost:hover {
      background: #e5edff;
    }

    .hero-meta {
      font-size: 0.78rem;
      color: #6b7280;
    }

    .hero-card {
      background: radial-gradient(circle at top, #dbeafe 0, #eef2ff 40%, #f9fafb 100%);
      border-radius: 1.5rem;
      padding: 1.4rem 1.3rem;
      border: 1px solid rgba(148,163,184,0.6);
      box-shadow: 0 18px 45px rgba(15,23,42,0.12);
    }

    .hero-card-title {
      font-size: 0.95rem;
      font-weight: 700;
      margin-bottom: 0.7rem;
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .hero-stat-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 0.7rem;
      margin-bottom: 0.9rem;
    }

    .stat {
      background: rgba(255,255,255,0.95);
      border-radius: 0.9rem;
      padding: 0.55rem 0.7rem;
      border: 1px solid rgba(209,213,219,0.9);
      font-size: 0.78rem;
    }

    .stat-label {
      color: #6b7280;
      margin-bottom: 0.15rem;
    }

    .stat-value {
      font-weight: 700;
      font-size: 0.9rem;
      color: #111827;
    }

    .stat-note {
      font-size: 0.7rem;
      color: #9ca3af;
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.35rem;
      margin-top: 0.3rem;
    }

    .pill {
      font-size: 0.7rem;
      padding: 0.15rem 0.55rem;
      border-radius: 999px;
      border: 1px dashed rgba(148,163,184,0.8);
      background: rgba(255,255,255,0.9);
      color: #4b5563;
    }

    section {
      margin-bottom: 2rem;
    }

    .section-title {
      font-size: 1.2rem;
      font-weight: 800;
      margin-bottom: 0.4rem;
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }

    .section-sub {
      font-size: 0.9rem;
      color: #4b5563;
      margin-bottom: 1rem;
    }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
      margin-bottom: 1.2rem;
    }

    .card {
      background: rgba(255,255,255,0.95);
      border-radius: 1rem;
      padding: 0.9rem 1rem;
      border: 1px solid rgba(209,213,219,0.9);
      font-size: 0.85rem;
    }

    .card h3 {
      font-size: 0.92rem;
      margin-bottom: 0.35rem;
    }

    .card p {
      font-size: 0.8rem;
      color: #4b5563;
    }

    .table-wrapper {
      overflow-x: auto;
      border-radius: 1rem;
      border: 1px solid rgba(209,213,219,0.9);
      background: rgba(255,255,255,0.98);
      box-shadow: 0 14px 30px rgba(15,23,42,0.08);
      margin-bottom: 1.4rem;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.82rem;
      min-width: 520px;
    }

    thead {
      background: linear-gradient(to left, #dbeafe, #e0f2fe);
    }

    th, td {
      padding: 0.55rem 0.7rem;
      text-align: right;
      border-bottom: 1px solid rgba(229,231,235,0.9);
    }

    th {
      font-weight: 700;
      color: #111827;
      white-space: nowrap;
    }

    tbody tr:nth-child(even) {
      background-color: #f9fafb;
    }

    tbody tr:hover {
      background-color: #eef2ff;
    }

    .tag-good {
      color: #166534;
      font-weight: 600;
    }

    .tag-risk {
      color: #b91c1c;
      font-weight: 600;
    }

    .tag-neutral {
      color: #6b7280;
      font-weight: 500;
    }

    .note {
      font-size: 0.78rem;
      color: #6b7280;
      margin-top: 0.25rem;
    }

    .footer-rap {
      margin-top: 1.4rem;
      padding: 1rem 1.1rem;
      border-radius: 1rem;
      background: radial-gradient(circle at top, #fef3c7 0, #fef9c3 35%, #fffbeb 100%);
      border: 1px solid rgba(251,191,36,0.7);
      font-size: 0.88rem;
    }

    .footer-rap-title {
      font-weight: 700;
      margin-bottom: 0.4rem;
    }

    footer {
      padding: 1.5rem 1.4rem 2.3rem;
      border-top: 1px solid rgba(209,213,219,0.9);
      background: rgba(248,250,252,0.96);
      font-size: 0.8rem;
      color: #6b7280;
    }

    .footer-grid {
      max-width: 1080px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: minmax(0, 1.5fr) minmax(0, 1fr);
      gap: 1.5rem;
    }

    .footer-links {
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
    }

    .hashtags {
      margin-top: 0.35rem;
      font-size: 0.78rem;
      color: #4b5563;
    }

    .pasuk {
      margin-top: 0.6rem;
      font-size: 0.82rem;
      font-weight: 600;
      color: #111827;
    }

    @media (max-width: 880px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }

      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }

      .nav-links {
        width: 100%;
        justify-content: flex-start;
        flex-wrap: wrap;
      }

      .cards-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .footer-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    @media (max-width: 640px) {
      main {
        padding-inline: 1rem;
      }

      .cards-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-card {
        order: -1;
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <header>
      <div class="logo">
        🧬 ProteinPulse
        <span>PP • חלבונים</span>
      </div>
      <nav class="nav-links">
        <a href="#what">מה זה חלבון?</a>
        <a href="#tables">טבלאות</a>
        <a href="#dairy">מוצרי חלב</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div>
          <div class="hero-badge">
            ⚡ מאגר תזונה • חלבונים • AnLoMinus
          </div>
          <h1 class="hero-title">
            חלבונים — <span>המנוע השקט של הגוף</span> 🧠💪
          </h1>
          <p class="hero-sub">
            כאן מרוכזת תמונת מצב ברורה על מקורות החלבון העיקריים בתזונה היומית —
            מן החי, מן הצומח וממוצרי החלב. הכל בדגש על כמויות חלבון למנה, יתרונות,
            חסרונות ואופן שימוש חכם.
          </p>
          <div class="hero-actions">
            <a class="btn-primary" href="https://github.com/AnLoMinus/ProteinPulse" target="_blank" rel="noreferrer">
              לצפייה במאגר ב־GitHub 🚀
            </a>
            <a class="btn-ghost" href="#tables">
              קפיצה לטבלאות ההשוואה 📊
            </a>
          </div>
          <div class="hero-meta">
            עמוד זה מיועד ללימוד, השראה וסדר — לאבחון רפואי או תפריט אישי.
          </div>
        </div>

        <aside class="hero-card">
          <div class="hero-card-title">
            📌 סיכום מהיר — 4 נקודות על חלבון
          </div>
          <div class="hero-stat-grid">
            <div class="stat">
              <div class="stat-label">צריכה יומית</div>
              <div class="stat-value">כ־1.2–1.6 גר׳ לק״ג</div>
              <div class="stat-note">לרוב האנשים הפעילים</div>
            </div>
            <div class="stat">
              <div class="stat-label">פיזור חכם</div>
              <div class="stat-value">3–4 ארוחות</div>
              <div class="stat-note">לא רק ב״פיצוץ״ אחד</div>
            </div>
            <div class="stat">
              <div class="stat-label">מקורות מרכזיים</div>
              <div class="stat-value">ביצים, עוף, דגים, קטניות</div>
              <div class="stat-note">שילוב חי + צומח</div>
            </div>
            <div class="stat">
              <div class="stat-label">שילוב תודעתי</div>
              <div class="stat-value">אכילה מתוך כוונה</div>
              <div class="stat-note">לא אוטומט, אלא בחירה</div>
            </div>
          </div>
          <div class="pill-row">
            <span class="pill">🧱 בניית שריר</span>
            <span class="pill">🛡️ מערכת חיסון</span>
            <span class="pill">🧬 אנזימים והורמונים</span>
            <span class="pill">🧠 ריכוז ועירנות</span>
          </div>
        </aside>
      </section>

      <section id="what">
        <h2 class="section-title">🧬 מה זה חלבון בפשטות?</h2>
        <p class="section-sub">
          חלבון הוא שרשרת של חומצות אמינו. הסדר והצורה של השרשרת קובעים את
          תפקיד החלבון: בניית שריר, תיקון תאים, נוגדנים, אנזימים, הורמונים ועוד.
          כשאנו אוכלים מזון עשיר בחלבון — הגוף מפרק אותו לחומצות אמינו, ובונה
          מחדש את מה שהוא צריך.
        </p>

        <div class="cards-grid">
          <article class="card">
            <h3>🏋️‍♂️ בנייה ותיקון</h3>
            <p>
              חלבון משמש כחומר בנייה לשרירים, לעצמות, לעור ולשיער. אחרי מאמץ
              פיזי — הגוף זקוק לו במיוחד כדי לשקם את הרקמות.
            </p>
          </article>
          <article class="card">
            <h3>⚙️ אנזימים וחילוף חומרים</h3>
            <p>
              אנזימים רבים בנויים מחלבון ומזרזים כל תגובה כימית בגוף — מעיכול
              ועד הפקת אנרגיה.
            </p>
          </article>
          <article class="card">
            <h3>🛡️ הגנה וחסינות</h3>
            <p>
              נוגדנים, חלבוני דם ורכיבים של מערכת החיסון נשענים על זמינות חלבון
              טובה. חוסר כרוני פוגע ביכולת ההגנה.
            </p>
          </article>
        </div>
      </section>

      <section id="tables">
        <h2 class="section-title">📊 טבלאות השוואה — חי מול צומח</h2>
        <p class="section-sub">
          להלן מבט מרוכז על מזונות נבחרים, עם כמות החלבון בכל 100 גרם, יחד עם
          יתרונות וחסרונות. המספרים הם ממוצעים כלליים.
        </p>

        <h3 class="section-title" style="font-size:1rem;">🌱 חלבון מן הצומח</h3>
        <div class="table-wrapper">
          <table>
            <thead>
              <tr>
                <th>מזון</th>
                <th>חלבון (גר׳/100 גר׳)</th>
                <th>יתרון מרכזי</th>
                <th>נקודת תשומת לב</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>עדשים מבושלות</td>
                <td><strong>≈9 גר׳</strong></td>
                <td class="tag-good">סיבים וברזל, שובע גבוה</td>
                <td class="tag-neutral">לא חלבון "מלא" לבדו</td>
              </tr>
              <tr>
                <td>חומוס מבושל</td>
                <td><strong>≈8.5 גר׳</strong></td>
                <td class="tag-good">שילוב יפה של פחמימה + חלבון</td>
                <td class="tag-neutral">דורש בישול/השריה טובה</td>
              </tr>
              <tr>
                <td>טופו</td>
                <td><strong>≈15 גר׳</strong></td>
                <td class="tag-good">חלבון "מלא" מן הצומח</td>
                <td class="tag-neutral">תלוי איכות חומר הגלם</td>
              </tr>
              <tr>
                <td>טמפה</td>
                <td><strong>≈19 גר׳</strong></td>
                <td class="tag-good">מזון מותסס, עיכול נוח</td>
                <td class="tag-neutral">טעם מרקם ייחודי</td>
              </tr>
              <tr>
                <td>קינואה מבושלת</td>
                <td><strong>≈4.4 גר׳</strong></td>
                <td class="tag-good">חלבון "מלא" + מינרלים</td>
                <td class="tag-neutral">יחסית מעט חלבון ל־100 גר׳</td>
              </tr>
              <tr>
                <td>שקדים</td>
                <td><strong>≈21 גר׳</strong></td>
                <td class="tag-good">שומן חד־בלתי רווי טוב</td>
                <td class="tag-risk">קלורי מאוד – להיזהר בכמויות</td>
              </tr>
              <tr>
                <td>טחינה גולמית</td>
                <td><strong>≈17 גר׳</strong></td>
                <td class="tag-good">סידן וברזל במינון גבוה</td>
                <td class="tag-risk">צפופה בקלוריות</td>
              </tr>
            </tbody>
          </table>
        </div>

        <h3 class="section-title" style="font-size:1rem;">🍗 חלבון מן החי</h3>
        <div class="table-wrapper">
          <table>
            <thead>
              <tr>
                <th>מזון</th>
                <th>חלבון (גר׳/100 גר׳)</th>
                <th>יתרון מרכזי</th>
                <th>נקודת תשומת לב</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>חזה עוף מבושל</td>
                <td><strong>≈31 גר׳</strong></td>
                <td class="tag-good">חלבון גבוה, שומן נמוך</td>
                <td class="tag-neutral">עלול להיות יבש ללא הכנה טובה</td>
              </tr>
              <tr>
                <td>בקר רזה</td>
                <td><strong>≈26 גר׳</strong></td>
                <td class="tag-good">ברזל וזינק זמינים</td>
                <td class="tag-risk">שומן רווי במנות שמנות יותר</td>
              </tr>
              <tr>
                <td>סלמון</td>
                <td><strong>≈20–22 גר׳</strong></td>
                <td class="tag-good">אומגה 3 + חלבון איכותי</td>
                <td class="tag-neutral">מחיר גבוה יחסית</td>
              </tr>
              <tr>
                <td>טונה במים</td>
                <td><strong>≈23–25 גר׳</strong></td>
                <td class="tag-good">חלבון "נקי" ונוח לשימוש</td>
                <td class="tag-neutral">לא להגזים בצריכה יומית</td>
              </tr>
              <tr>
                <td>ביצה שלמה</td>
                <td><strong>≈6–7 גר׳ ליחידה</strong></td>
                <td class="tag-good">חלבון מלא + ויטמינים</td>
                <td class="tag-neutral">לשמור על איזון לצורכי כולסטרול</td>
              </tr>
            </tbody>
          </table>
        </div>

        <h3 class="section-title" style="font-size:1rem;">📅 חלבון לפי מנה יומית</h3>
        <div class="table-wrapper">
          <table>
            <thead>
              <tr>
                <th>מוצר</th>
                <th>גודל מנה</th>
                <th>חלבון למנה</th>
                <th>שימוש מומלץ</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>ביצים</td>
                <td>2 יחידות</td>
                <td><strong>≈12–14 גר׳</strong></td>
                <td>ארוחת בוקר/ערב, בסיס שקשוקה/חביתה</td>
              </tr>
              <tr>
                <td>יוגורט יווני</td>
                <td>גביע (≈170 גר׳)</td>
                <td><strong>≈15–17 גר׳</strong></td>
                <td>עם גרנולה, פירות, שיבולת שועל</td>
              </tr>
              <tr>
                <td>חזה עוף</td>
                <td>150 גר׳</td>
                <td><strong>≈45–48 גר׳</strong></td>
                <td>ארוחת צהריים/ערב מרכזית</td>
              </tr>
              <tr>
                <td>עדשים מבושלות</td>
                <td>כוס מלאה</td>
                <td><strong>≈18 גר׳</strong></td>
                <td>תוספת למרק, תבשיל, סלט עדשים</td>
              </tr>
              <tr>
                <td>טופו</td>
                <td>150 גר׳</td>
                <td><strong>≈22–24 גר׳</strong></td>
                <td>מוקפץ, שווארמה טבעונית, קוביות בסלט</td>
              </tr>
            </tbody>
          </table>
        </div>

        <p class="note">
          💡 עיקרון זהב: לא חייבים חלבון שיא מכל מנה — העיקר שהיום כולו יהיה
          מאוזן ומתוכנן.
        </p>
      </section>

      <section id="dairy">
        <h2 class="section-title">🥛 מוצרי חלב — מפת חלבון מרוכזת</h2>
        <p class="section-sub">
          מוצרי חלב מספקים חלבון יחד עם סידן ולעיתים גם שומן רווי. המפתח הוא
          בחירה מודעת: מה מתאים לך, באיזו תדירות ובאיזו כמות.
        </p>

        <div class="table-wrapper">
          <table>
            <thead>
              <tr>
                <th>מוצר חלב</th>
                <th>חלבון (גר׳/100 גר׳)</th>
                <th>יתרון</th>
                <th>נקודה למחשבה</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>חלב 3%</td>
                <td><strong>≈3.3 גר׳</strong></td>
                <td class="tag-good">זמין, מוכר, בסיס לשייקים</td>
                <td class="tag-neutral">לא מאוד עשיר בחלבון</td>
              </tr>
              <tr>
                <td>חלב 1%</td>
                <td><strong>≈3.4 גר׳</strong></td>
                <td class="tag-good">פחות שומן, אותה כמות חלבון</td>
                <td class="tag-neutral">משביע מעט פחות</td>
              </tr>
              <tr>
                <td>גבינה לבנה 5%</td>
                <td><strong>≈11 גר׳</strong></td>
                <td class="tag-good">קלילה, נוחה למריחה</td>
                <td class="tag-neutral">לא חלבון "שיא" ל־100 גר׳</td>
              </tr>
              <tr>
                <td>קוטג' 5%</td>
                <td><strong>≈11–12 גר׳</strong></td>
                <td class="tag-good">שובע גבוה, מצוין אחרי אימון</td>
                <td class="tag-neutral">להתייחס למלח בתפריט הכללי</td>
              </tr>
              <tr>
                <td>יוגורט יווני 9%</td>
                <td><strong>≈10 גר׳</strong></td>
                <td class="tag-good">חלבון מרוכז, טעם עשיר</td>
                <td class="tag-risk">שומן גבוה — לאנשים הרגישים לכך</td>
              </tr>
              <tr>
                <td>גבינה צהובה 28%</td>
                <td><strong>≈25 גר׳</strong></td>
                <td class="tag-good">חלבון גבוה מאוד ל־100 גר׳</td>
                <td class="tag-risk">שומן רווי ומלח — לשימוש מדוד</td>
              </tr>
              <tr>
                <td>גבינת סקיר</td>
                <td><strong>≈11 גר׳</strong></td>
                <td class="tag-good">שילוב יפה: הרבה חלבון, מעט שומן</td>
                <td class="tag-neutral">מרקם מיוחד, עניין של טעם</td>
              </tr>
            </tbody>
          </table>
        </div>

        <p class="note">
          🧭 שימוש חכם במוצרי חלב: לחשוב עליהם כ"קוביות חלבון" משלימות —
          לא כמרכז כל התפריט. לשלב יחד עם ירקות, דגנים מלאים ושומן איכותי.
        </p>

        <div class="footer-rap">
          <div class="footer-rap-title">🎤 ProteinPulse Rap • פזמון</div>
          <p>
            חלבון בכל ביס — הגוף עולה מדרגות,<br />
            בונה שריר ותודעה — מיישר לך מחשבות,<br />
            חי, צומח, חלב — הכול נבנה בתבונה,<br />
            כשאוכלים עם כוונה — מתעוררת הנשמה. ⚡
          </p>
        </div>
      </section>
    </main>

    <footer>
      <div class="footer-grid">
        <div>
          <div>© ProteinPulse (PP) • מאגר חלבונים בהשראת AnLoMinus.</div>
          <div class="footer-links">
            <a href="https://github.com/AnLoMinus" target="_blank" rel="noreferrer">
              🟣 GitHub • AnLoMinus
            </a>
            <a href="https://github.com/AnLoMinus/ProteinPulse" target="_blank" rel="noreferrer">
              📁 מקור המידע למאגר: ProteinPulse Repository
            </a>
          </div>
          <div class="hashtags">
            #ProteinPulse #חלבונים #AnLoMinus #Nutrition #MindfulEating
          </div>
          <div class="pasuk">
            "הַנֹּתֵן לָהֶם מָזוֹן לְכָל־בָּשָׂר כִּי לְעוֹלָם חַסְדּוֹ" (תהילים קל״ו)
          </div>
        </div>
        <div>
          <div>🕒 סטטוס דף:</div>
          <div>עודכן: 16.11.2025 • כ״ד בחשוון תשפ״ו • ישראל</div>
          <div>מיועד כהשראה, סדר והכוונה — לא כתחליף לייעוץ מקצועי אישי.</div>
        </div>
      </div>
    </footer>
  </div>
</body>
</html>
```

---

## 🛠️ איך להשתמש בעמוד במאגר ProteinPulse

1. היכנס למאגר:
   `https://github.com/AnLoMinus/ProteinPulse/`
2. צור קובץ חדש בשם: **`index.html`** בשורש (root) המאגר.
3. הדבק את כל הקוד שלמעלה ושמור (Commit).
4. ב־GitHub Pages (Settings → Pages) בחר:

   * Source: Branch `main` (או `master`)
   * Folder: `/root`
5. אחרי שמירת ההגדרות תקבל כתובת דף ציבורית שתציג את העמוד הזה.

---

## 🎤 פזמון ראפ נוסף לנשמה 💥

חלבון זה הדלק שמריץ כל מערכת,
מכוון את הגוף כמו תזמורת אור מושלמת,
כשאתה בוחר תזונה — אתה כותב את ההגדה,
מכל ביס של מודעות — נולדת לך מדרגה. ⚡

---

## 📎 קרדיטים למאגר

* 🔗 מאגר ראשי: [ProteinPulse Repository](https://github.com/AnLoMinus/ProteinPulse)
* 🔗 פרויקטים נוספים של AnLoMinus: [GitHub Profile](https://github.com/AnLoMinus)

---

## ✨ פסוק מסיים מתאים לנושא המזון והחיות

**"וְאַתָּה מְחַיֶּה אֶת כֻּלָּם"** (נחמיה ט׳)
