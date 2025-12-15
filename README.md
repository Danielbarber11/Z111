<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>אתר הדגמה מודרני</title>
    <!-- טעינת Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- הגדרת עיצוב וגופנים -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Heebo:wght@100..900&display=swap');
        body {
            font-family: 'Heebo', sans-serif;
            background-color: #f7f9fc; /* רקע בהיר כללי */
        }
        .text-shadow-custom {
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
    </style>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary': '#4f46e5',
                        'secondary': '#10b981',
                        'accent': '#f59e0b',
                    },
                }
            }
        }
    </script>
</head>
<body class="min-h-screen antialiased text-gray-800">

    <!-- סרגל ניווט (Header) -->
    <header class="bg-white shadow-md sticky top-0 z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- לוגו -->
                <div class="flex-shrink-0">
                    <a href="#" class="text-xl font-bold text-primary hover:text-indigo-600 transition duration-300">
                        פרויקט <span class="text-secondary">דיגיטל</span>
                    </a>
                </div>

                <!-- ניווט ראשי (מוצג רק בדסקטופ) -->
                <nav class="hidden md:flex space-x-8 space-x-reverse">
                    <a href="#home" class="text-gray-600 hover:text-primary transition duration-300 font-medium">ראשי</a>
                    <a href="#features" class="text-gray-600 hover:text-primary transition duration-300 font-medium">שירותים</a>
                    <a href="#about" class="text-gray-600 hover:text-primary transition duration-300 font-medium">אודותינו</a>
                    <a href="#contact" class="px-4 py-2 bg-primary text-white rounded-lg shadow-lg hover:bg-indigo-600 transition duration-300 font-medium">צור קשר</a>
                </nav>

                <!-- כפתור תפריט המבורגר (מוצג רק במובייל) -->
                <button id="mobile-menu-button" class="md:hidden p-2 text-gray-600 hover:text-primary rounded-md transition duration-300" aria-label="Open menu">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                </button>
            </div>
        </div>

        <!-- תפריט מובייל נשלף -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-xl">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <a href="#home" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-indigo-50 hover:text-primary">ראשי</a>
                <a href="#features" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-indigo-50 hover:text-primary">שירותים</a>
                <a href="#about" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-indigo-50 hover:text-primary">אודותינו</a>
                <a href="#contact" class="block w-full text-center px-3 py-2 mt-2 rounded-md text-base font-medium text-white bg-primary hover:bg-indigo-600">צור קשר</a>
            </div>
        </div>
    </header>

    <!-- סקשן גיבור (Hero Section) -->
    <section id="home" class="py-20 md:py-32 bg-primary/95 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold mb-4 leading-tight text-shadow-custom">
                הפתרון הדיגיטלי המושלם לעסק שלך
            </h1>
            <p class="text-xl sm:text-2xl font-light mb-8 max-w-3xl mx-auto">
                בנה את הנוכחות המקוונת שלך בקלות ובמהירות. התחל היום והגיע ללקוחות חדשים.
            </p>
            <a href="#contact" class="inline-block px-10 py-4 text-lg font-bold bg-secondary text-white rounded-full shadow-2xl transition duration-500 transform hover:scale-105 hover:bg-emerald-500 focus:outline-none focus:ring-4 focus:ring-secondary/50">
                התחל עכשיו
            </a>
        </div>
    </section>

    <!-- סקשן תכונות (Features Section) -->
    <section id="features" class="py-16 md:py-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <span class="text-primary font-semibold text-sm uppercase tracking-wider">היתרונות שלנו</span>
                <h2 class="text-3xl font-bold text-gray-900 mt-2">למה לבחור בנו?</h2>
            </div>

            <!-- גריד תכונות -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">

                <!-- כרטיס תכונה 1 -->
                <div class="bg-white p-6 rounded-xl shadow-lg hover:shadow-2xl transition duration-300 border-t-4 border-primary/70">
                    <div class="text-primary mb-4">
                        <!-- אייקון עיצוב רספונסיבי (SVG) -->
                        <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9.25 12L12 8L14.75 12L14.25 17M12 21a9 9 0 110-18 9 9 0 010 18z"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-900">עיצוב רספונסיבי</h3>
                    <p class="text-gray-600">האתר נראה מדהים בכל מכשיר - ממחשב שולחני ועד סמארטפון, ומותאם אוטומטית לכל גודל מסך.</p>
                </div>

                <!-- כרטיס תכונה 2 -->
                <div class="bg-white p-6 rounded-xl shadow-lg hover:shadow-2xl transition duration-300 border-t-4 border-secondary/70">
                    <div class="text-secondary mb-4">
                        <!-- אייקון ביצועים מהירים (SVG) -->
                        <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-900">ביצועים מהירים</h3>
                    <p class="text-gray-600">טעינה מהירה במיוחד (פחות מ-2 שניות) ששומרת על המבקרים שלך מרוצים ומפחיתה נטישה.</p>
                </div>

                <!-- כרטיס תכונה 3 -->
                <div class="bg-white p-6 rounded-xl shadow-lg hover:shadow-2xl transition duration-300 border-t-4 border-accent/70">
                    <div class="text-accent mb-4">
                        <!-- אייקון תמיכה (SVG) -->
                        <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m3.536 3.536l-3.536-3.536m0 0a3.5 3.5 0 10-5.656 0 3.5 3.5 0 005.656 0zm-8.484 0L5.636 18.364"></path></svg>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-gray-900">תמיכה 24/7</h3>
                    <p class="text-gray-600">צוות התמיכה שלנו זמין עבורך מסביב לשעון לכל שאלה, תקלה או בקשת עדכון.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- סקשן אודות (About Section - Mock) -->
    <section id="about" class="bg-gray-50 py-16 md:py-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="md:flex md:items-center md:space-x-12 md:space-x-reverse">
                <!-- טקסט אודות -->
                <div class="md:w-1/2 mb-8 md:mb-0">
                    <h2 class="text-3xl font-bold text-gray-900 mb-4">הסיפור שלנו: מובילים את המחר הדיגיטלי</h2>
                    <p class="text-gray-600 mb-4 leading-relaxed">
                        אנחנו ב-<span class="font-semibold text-primary">פרויקט דיגיטל</span> מאמינים שכל עסק, קטן כגדול, ראוי לנוכחות מקוונת מרשימה ומקצועית. הקמנו את החברה מתוך שליחות לספק פתרונות בניית אתרים מתקדמים, קלים לשימוש ובמחירים הוגנים.
                    </p>
                    <p class="text-gray-600 leading-relaxed">
                        אנו משלבים ידע טכנולוגי עמוק עם הבנה עיצובית, כדי להבטיח שהאתר שלך לא רק ייראה טוב, אלא גם ישיג את המטרות העסקיות שלך.
                    </p>
                    <a href="#contact" class="mt-6 inline-block text-primary font-semibold hover:text-indigo-600 transition duration-300 border-b-2 border-primary/50 hover:border-primary">
                        למידע נוסף וייעוץ חינם &rarr;
                    </a>
                </div>
                <!-- תמונה אודות (Placeholder) -->
                <div class="md:w-1/2 flex justify-center">
                    <img src="https://placehold.co/600x400/4f46e5/ffffff?text=Image+of+Team" alt="" class="rounded-2xl shadow-xl transform hover:scale-[1.02] transition duration-500 w-full max-w-md">
                </div>
            </div>
        </div>
    </section>


    <!-- סקשן צור קשר (Contact Section) -->
    <section id="contact" class="py-16 md:py-24">
        <div class="max-w-xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-900 mt-2">בואו נדבר על הפרויקט שלך</h2>
                <p class="text-gray-600 mt-2">מלא את הטופס הקצר ואחד המומחים שלנו יחזור אליך בהקדם.</p>
            </div>

            <div class="bg-white p-8 rounded-xl shadow-2xl border-t-4 border-secondary">
                <form id="contact-form" class="space-y-4">
                    <div>
                        <label for="name" class="block text-sm font-medium text-gray-700 mb-1">שם מלא</label>
                        <input type="text" id="name" name="name" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-primary focus:border-primary transition duration-200" placeholder="שם ומשפחה">
                    </div>
                    <div>
                        <label for="email" class="block text-sm font-medium text-gray-700 mb-1">דוא"ל</label>
                        <input type="email" id="email" name="email" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-primary focus:border-primary transition duration-200" placeholder="example@company.com">
                    </div>
                    <div>
                        <label for="message" class="block text-sm font-medium text-gray-700 mb-1">הודעה</label>
                        <textarea id="message" name="message" rows="4" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-primary focus:border-primary transition duration-200" placeholder="כיצד נוכל לעזור?"></textarea>
                    </div>
                    <button type="submit" class="w-full px-4 py-3 bg-primary text-white font-bold rounded-lg shadow-lg hover:bg-indigo-600 transition duration-300 focus:outline-none focus:ring-4 focus:ring-primary/50">
                        שלח הודעה
                    </button>
                    <p id="form-message" class="text-center mt-4 hidden text-sm font-medium"></p>
                </form>
            </div>
        </div>
    </section>

    <!-- פוטר (Footer) -->
    <footer class="bg-gray-800 text-white mt-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 md:py-12 text-center">
            <div class="flex flex-col md:flex-row justify-between items-center space-y-4 md:space-y-0">
                <div class="text-sm">
                    &copy; 2025 פרויקט דיגיטל. כל הזכויות שמורות.
                </div>
                <div class="flex space-x-4 space-x-reverse text-sm">
                    <a href="#" class="hover:text-primary transition duration-300">תנאי שימוש</a>
                    <a href="#" class="hover:text-primary transition duration-300">מדיניות פרטיות</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- לוגיקת JavaScript -->
    <script>
        // לוגיקה לתפריט המובייל
        document.getElementById('mobile-menu-button').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // לוגיקה לטיפול בטופס (לדוגמה בלבד, אין שליחה אמיתית)
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const formMessage = document.getElementById('form-message');
            formMessage.classList.remove('hidden');
            formMessage.classList.remove('text-red-600');
            formMessage.classList.add('text-secondary');
            formMessage.innerHTML = 'הטופס נשלח בהצלחה! ניצור קשר בהקדם.';
            
            // אפס את הטופס לאחר שליחה
            document.getElementById('contact-form').reset();

            // הסתרת ההודעה לאחר 5 שניות
            setTimeout(() => {
                formMessage.classList.add('hidden');
            }, 5000);
        });

        // סגירת תפריט מובייל בלחיצה על קישור
        document.querySelectorAll('#mobile-menu a').forEach(item => {
            item.addEventListener('click', () => {
                document.getElementById('mobile-menu').classList.add('hidden');
            });
        });
    </script>
</body>
</html># Z111
