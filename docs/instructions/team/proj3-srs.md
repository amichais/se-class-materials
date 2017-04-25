<div dir="rtl">
<div>
</div>

חזרה ל[עמוד ראשי](../../..)

# פרויקט 3 – מפרט דרישות תוכנה - Software Requirements Specification

## מטרת המשימה
מטרת משימה זו היא לכתוב את מפרט דרישות התוכנה – Software Requirements Specification - של הפרויקט שלכם, כך שתתעדו את תהליך ניתוח הדרישות שבצעתם. מפרט זה ישמש בסיס להמשך הפיתוח, כאשר בשלבים הבאים נכתוב גם מפרטי תיכון ותכנון לפרויקט.

## פירוט הציון
ראו בהמשך.

## הנחיות הגשה כלליות
ההגשה היא ע״י פתיחת כרטיס (issue) במערכת המשימות של מאגר הפרויקט ושיוכו למתרגל\ת.

בכותרת הכרטיס יש לציין את המשימה, למשל: project3-srs-submission בפרטי הכרטיס יש לתת קישורים רלוונטיים לתיעוד (במיוחד עמוד הויקי של ההגשה), קוד והפצה.

בנוסף:

יש לפרסם הודעה בחדר הצ׳אט של הפרויקט על ההגשה עם תיוג (@) המרצה והמתרגל\ת והפניה (קישור) לכרטיס שנפתח (#xx) (יש להזמין אותנו לחדרים ואנחנו נהיה שם במוד שקט ונשים לב להודעות רק אם קוראים לנו).

במשימות מימוש (סבבי פיתוח) יש להוסיף תג מתאים למערכת בקרת הגרסאות.
כל חברי הצוות ממלאים הערכת עמיתים (בסבבים בהם הוגדר).

פירוט הנחיות להגשה במשימה זו בהמשך.

## הנחיות עבודה

### כללי
ברכותינו! הצוות שלכם מצא פרויקט שנבחר בשלב הקודם. בפרויקט מעורבים גם הלקוח שהזמין את הפרויקט וגם צוות הקורס שייפגשו אתכם מדי פעם לדון במוצר המבוקש.

במשימה זו, הצוות שלכם יגדיר את הדרישות העיקריות למוצר התוכנה וכן יפרט דרישות סביבה של התוכנה עם סקיצות של חלק מממשק המשתמש.

### דרישות חיצוניות
אמנם הלקוח התלהב מאד מהמאפיינים הכלליים של המוצר שהוצגו לו, ולכן גם החליט להשאיר בידיכם את השלב הבא להגדרה, אך עדיין יש לו כמה דרישות כלליות:

- המוצר צריך להיות קל לשימוש ככל האפשר, גם למי שאינו משתמש מחשב מנוסה (למעט כלים שנועדו עבור משתמשים כאלו).
- המוצר צריך להיות עמיד לשגיאות שאפשר לצפות שיקרו משימוש סביר, כמו קלט משתמש לא נכון, בעיות תקשורת וכדו'
- כמו מקודם, המוצר צריך להיות מבוסס לקוח-שרת, או לפחות בעל ארכיטקטורה של כמה רכיבים משמעותיים שלפחות אחד מהם מכיל לוגיקה שאינה טריוויאלית.
- חלק הלקוח צריך להיות נגיש מאד למשתמש. אם המוצר מבוסס רשת (SaaS), אז צריכה להיות גישה פתוחה אליו באינטרנט דרך URL באמצעות דפדפן סטנדרטי. במידה וצד הלקוח הוא אפליקציה עצמאית אז תצטרכו לתת דרך פשוטה ללקוח להתקין ולהריץ או לגשת גם לחלק השרת (אפשר להניח שלמשתמש יש את החומרה והכלים או הספריות נחוצים (כמו אנדרואיד, JVM או .Net Framework וכדו׳))
- קוד המוצר יהיה פתוח (open source, למעט אם הוסכם עם הלקוחות שלא כך יהיה) ואחרים גם יוכלו להוריד את הקוד שלכם ולבנות את המוצר. בנוסף יהיה תיעוד, כך שאחרים יוכלו בקלות להבין ולהרחיב את המוצר שלכם. התיעוד יהיה חלק מתוצרי הפרויקט ויכלול מסמכי תהליך, תכנון, תיכון, בדיקות ודוחות של תקלות - שיוגדרו בהמשך הפרויקט.
- היקף הפרויקט יהיה בהתאמה טובה למשאבים שקיבלתם.

מעבר לדרישות אלו, אתם יכולים להמשיך בתוכנית הפיתוח ולהתחיל בבניית מפרט הדרישות. מסמך מפרט הדרישות שייכתב יהיה בעצם החוזה שלכם מול הלקוח המגדיר את המוצר המפותח. כתוצאה מכך עליכם להיות בקשר אם הלקוח תוך כדי התכנון כדי לוודא שהמוצר עונה על דרישותיו וצרכיו.


### מפרט דרישות – Software Requirements Specification (SRS)
מסמך SRS הוא כלי ללכידת (איסוף) והבנת (ניתוח) דרישות המוצר. מפרט זה נכתב לעיתים רבות לפי פורמט ארגוני ונקרא לעיתים מסמך *אפיון*.

אתם תכינו מפרט דרישות כדף ויקי עם סעיפים שונים (ראו ב[דף ויקי התבנית][srs-wiki-template]), לחלופין, מצורפת [תבנית][srs-template] בעברית שהותאמה עבור משימה זו (ואם תבחרו להשתמש בה תקשרו את המסמך לעמוד). המטרה העיקרית היא לתרגל כתיבת תרחישי שימוש מפורטים לשם ניתוח דרישות המוצר, אך גם לאסוף את כלל סיפורי המשתמשים לרשימה שעליה יתבסס המשך הפיתוח. 

מומלץ גם להתרשם ממפרטי דרישות של פרויקטים קודמים.

#### השפעה על תהליך הפיתוח
מסמך זה מגדיר את מוצר התוכנה שייבנה, הוא נסמך על הצעת ואתחול הפרויקט ומסמכים נוספים שהתקבלו מהלקוח. המסמך מגדיר אוסף דרישות שעל המוצר לממש ולכן עליו מתבססים השלבים הבאים, כגון תיכון, תכנון, מימוש ובדיקות ותחזוקה. לעיתים מסמך זה ייכתב לאחר מסמך דרישות מערכת, המהווה קלט לכתיבת מסמך זה (שם נוסף למסמך User Requirements Document).

### הנקודות העיקריות להתייחסות במסמך הן
- תיאור כללי של המוצר והפעם בדגש מיוחד על ההיקף הצפוי שלו.
- אוסף use cases (תרחישי שימוש) הכולל לפחות דיאגראמת סיכום אחת ותיאור מלא של שניים מתרחישי השימושים העיקריים במערכת (אפילו במוצר בינוני בד"כ מוגדרים עשרות תרחישי שימוש).
- כלל הדרישות הידועות יכוסו ע"י רשימת סיפורי משתמש (בהמשך יוזנו כ- github issues)
- גם דרישות כלליות מהמוצר, שהוזכרו לעיל, צריכות לבוא לידי ביטוי ברשימה זו וכן דרישות לא-פונקציונליות כגון סביבה (חומרה, תקנים וכדו')
- אב טיפוס של ממשק המשתמש
   0. קישור לעמוד ההפצה הנוכחי עם מסכים ראושניים, לחלופין,
   0. הכניסו (או קשרו ל) לפחות שתי דיאגראמות המכילות סקיצה של ממשק המשתמש של המוצר וכיצד עוברים ביניהן.

- רשימה של דרישות לא ברורות או סותרות שנשארו לאחר ניתוח כל המקורות שלרשותכם.
- רשות: טבלת דרישות כללית. לכל דרישה יצוינו: מספר הדרישה, סוג הדרישה (פונקציונאלית או לא), מספר תרחיש השימוש או סיפור המשתמש שהיא נובעת ממנו (אם רלוונטי) וכן דרגתה: הכרחית, כדאית או אופציונאלית (טבלה כזו חשובה במיוחד בפרויקטים מורכבים בהם יש לעקוב לאורך זמן אחד דרישות ושינויים בהן).

מסמך זה יהיה הבסיס להמשך הפיתוח. שימו לב שהכוונה שמסמך זה יהיה נושם, יתכן שתצטרכו בשלבים מאוחרים לעדכן אותו ומסיבה זו אנחנו ממליצים שהמסמך יוכן כעמוד ויקי – אך אם תעדיפו תוכלו להשתמש בתבנית (ואז כדאי כבר לחשוב על ניהול גרסאות למסמך). פעמים רבות מסמכים אלו הם באורך מאות ואלפי עמודים, אך בהתחשב במשאבים ואופי הפיתוח האיטרטיבי המתוכנן לפרויקט שלכם, הוא צריך להיות בסביבות 10 עמודים.

### הנחיות הגשה וציונים

הגשה: ההגשה ע״י פתיחת כרטיס במערכת המשימות והודעה בחדר הצ׳אט. כמפורט לעיל.

#### עד לערב ההרצאה הבאה:
- הכנה ופרסום של ויקי או מסמך ה- SRS.
- ~~תיאור קצר בויקי (גם אם המפרט עצמו במסמך חיצוני) של מצב אב הטיפוס ו/או ניסיונות אחרים שהתחלתם לבצע להנמכת סיכון משמעותי שעלה בהצעת הפרויקט.~~
- רישום לסקר דרישות [בעמוד הפגישות][coursewiki-meetings]: במסגרת ההרצאה או התרגיל עם סגל הקורס.
- הצגה בסקר של דיאגראמת תרחישים, תרחיש ראשי, סיפורי משתמשים וסקיצת UI, במסגרת הסקר דווחו גם על הניסיון הטכנולוגי שלכם או אב-טיפוס.<br/>
יש לתעד את ההערות שעלו בסקר בהערות לכרטיס ההגשה.

#### יומיים אחרי ביצוע הסקר:
- הגשת גרסה מתוקנת ומליאה של מפרט הדרישות
- סיכום סקר דרישות עם הלקוח כפסקה בעמוד הדרישות ו\או הפניה לתיעוד הסקר (למשל בדומה לתבנית שבנספח התבנית, ראו ב[ויקי לדוגמא][demorepo-srs-review] או הערות באישיו ההגשה) ותיעוד של תקשורת נוספת עם הלקוח כרישום שיחות, שרשורי מייל, תרשימים על נייר (סרוק אם צריך), משימות (issues) ובעיקר סיכום חוות דעתו של הלקוח על הדרישות כפי שהתגבשו בשלב זה.
- נא לעדכן את המתרגל/ת בהגשת סיכום זה.

#### ציונים

הציון ייקבע לפי  הגשה ורישום בזמן לפי ההנחיות (5%), איכות המסמך וההצגה בסקר עם צוות הקורס (50%),  תכני עמוד ה-SRS (~~התקדמות באב טיפוס~~, סיכונים - 20%), תיקונים לפי סיכום סקר (10%), סקר וחוות דעת לקוח (15%).

### הנחיות לשימוש בתבנית

[התבנית][srs-template] כוללת את המרכיבים העיקריים שמסמך כזה בד"כ מכיל. ניתן להוסיף או להוריד חלקים לפי הצורך.
גופנים:
טקסט <font style="color:red">_כזה_</font> (אדום, נטוי עם קו תחתי), יש להחליף בטקסט משלכם.
טקסט המתחיל עם ציור של גלגל מיסב מהווה הסבר למקומו של התוכן בתהליך הפיתוח, יש למחוק לאחר מילוי המסמך.
טקסט המתחיל עם הציור  ו\או בגופן הזה (סגול נטוי) מהווה הוראות למילוי, שניתן למחוק.

### מקורות לתבנית
- תבניות הפרויקט [ReadySET][ReadySET] (רשיון קוד פתוח BSD)
- תבניות מלוות לספר McConnell S.,  "Software Project Survival Guide", http://www.construx.com/Page.aspx?nid=253
- תבניות בשימוש התעשיה בארץ.

### קישורים להרחבה

<p dir="ltr" markdown='1'>

- Amber, [Quick UML Use Case](http://www.agiledata.org/essays/objectOrientation101.html#UMLUseCaseDiagrams) Diagrams Tutorial<br/>
- Mike Cohn, [User Stories](http://www.mountaingoatsoftware.com/system/presentation/file/42/SDBP2006_UserStories.pdf?1267636376) (presentation)<br/>
- Assaf Stove, [Why Should I INVEST in User Stories?](http://www.softwareandi.com/2012/03/why-should-i-invest-in-user-stories.html), Blog 2012<br/>
- Wake, [INVEST in Good Stories, and SMART Tasks](http://xp123.com/articles/invest-in-good-stories-and-smart-tasks/), 2003<br/>
- Steve Yegge, [Business Requirements are Bullshit](http://steve-yegge.blogspot.com/2008/08/business-requirements-are-bullshit.html)<br/>
- Spolsky, [Painless Functional Specifications - Part 1: Why Bother?](http://steve-yegge.blogspot.com/2008/08/business-requirements-are-bullshit.html)<br/>
- [830-1998](http://dx.doi.org/10.1109%2FIEEESTD.1994.121431) — IEEE Recommended Practice for Software Requirements Specifications. 1998.  

</p>

בהצלחה!

<!-- Links -->
[coursewiki-meetings]: https://github.com/jce-il/se-class/wiki/Meetings#srs-review
[srs-template]: ./se-proj03-srs-template.docx
[srs-wiki-template]: https://github.com/jce-il/project-template/wiki/srs
[demorepo-srs-review]: https://github.com/robi-y/seproject-team-template/wiki/SRS-Review-Summary
[ReadySET]: http://readyset.tigris.org