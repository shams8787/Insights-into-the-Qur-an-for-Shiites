# Insights-into-the-Qur-an-for-Shiites <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ترجمة القرآن الكريم - المصادر الشيعية</title>
    <style>
        :root {
            --primary-color: #1a5e63;
            --secondary-color: #4caf50;
            --accent-color: #d4af37;
            --light-color: #f8f5e6;
            --dark-color: #2c3e50;
            --shiite-green: #0a5f38;
            --shiite-gold: #d4af37;
            --font-arabic: 'Scheherazade New', 'Traditional Arabic', serif;
            --font-english: 'Montserrat', 'Open Sans', sans-serif;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: var(--font-english);
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="none" width="100" height="100"/><path d="M30,50 A20,20 0 0,1 70,50 A20,20 0 0,1 30,50" fill="none" stroke="%230a5f38" stroke-width="0.5" opacity="0.1"/></svg>');
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--shiite-green), var(--primary-color));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            margin-left: 10px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--shiite-gold);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(10, 95, 56, 0.85), rgba(26, 94, 99, 0.85)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="%230a5f38" width="100" height="100"/><path d="M30,50 A20,20 0 0,1 70,50 A20,20 0 0,1 30,50" fill="none" stroke="%23d4af37" stroke-width="2" opacity="0.2"/></svg>');
            color: white;
            text-align: center;
            padding: 4rem 0;
            margin-bottom: 2rem;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .shiite-badge {
            display: inline-block;
            background-color: var(--shiite-gold);
            color: var(--shiite-green);
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: bold;
            margin-top: 1rem;
            font-size: 0.9rem;
        }
        
        /* Quran Browser */
        .quran-browser {
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            padding: 2rem;
            margin-bottom: 2rem;
            border-right: 4px solid var(--shiite-green);
        }
        
        .browser-controls {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }
        
        .surah-selector, .ayah-selector, .translation-selector {
            flex: 1;
            min-width: 200px;
            margin: 0 10px 10px 0;
        }
        
        select, button {
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
            width: 100%;
        }
        
        button {
            background-color: var(--shiite-green);
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #083c24;
        }
        
        /* Quran Display */
        .quran-display {
            margin-top: 2rem;
        }
        
        .surah-header {
            text-align: center;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }
        
        .surah-header h2 {
            color: var(--shiite-green);
            font-size: 1.8rem;
        }
        
        .surah-header p {
            color: #666;
        }
        
        .verse-container {
            margin-bottom: 2.5rem;
            padding: 1.5rem;
            background-color: #f9f9f9;
            border-radius: 8px;
            border-right: 3px solid var(--shiite-gold);
        }
        
        .verse-number {
            display: inline-block;
            background-color: var(--shiite-green);
            color: white;
            width: 30px;
            height: 30px;
            text-align: center;
            line-height: 30px;
            border-radius: 50%;
            margin-left: 10px;
        }
        
        .arabic-text {
            font-family: var(--font-arabic);
            font-size: 2rem;
            text-align: right;
            line-height: 2.5;
            margin-bottom: 1.5rem;
            color: var(--dark-color);
        }
        
        .translation-text {
            font-family: var(--font-english);
            font-size: 1.1rem;
            line-height: 1.8;
            padding: 1rem;
            background-color: white;
            border-radius: 4px;
            margin-bottom: 1rem;
        }
        
        .translation-source {
            font-size: 0.9rem;
            color: var(--shiite-green);
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .transliteration {
            font-style: italic;
            color: #666;
            margin-bottom: 1rem;
            padding: 0.5rem;
            background-color: #f0f0f0;
            border-radius: 4px;
        }
        
        .shiite-interpretation {
            background-color: #e8f5e9;
            padding: 1rem;
            border-radius: 4px;
            border-right: 3px solid var(--shiite-green);
            margin-top: 1rem;
        }
        
        .shiite-interpretation h4 {
            color: var(--shiite-green);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
        }
        
        .shiite-interpretation h4 i {
            margin-left: 5px;
        }
        
        /* Features Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            text-align: center;
            border-top: 4px solid var(--shiite-green);
        }
        
        .feature-card i {
            font-size: 2.5rem;
            color: var(--shiite-green);
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--shiite-green);
        }
        
        /* Resources Section */
        .resources {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 2rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .resources h2 {
            text-align: center;
            color: var(--shiite-green);
            margin-bottom: 1.5rem;
        }
        
        .resource-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .resource-item {
            padding: 1rem;
            background-color: #f9f9f9;
            border-radius: 4px;
            border-right: 3px solid var(--shiite-gold);
        }
        
        .resource-item h4 {
            color: var(--shiite-green);
            margin-bottom: 0.5rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--shiite-green);
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        
        .footer-links {
            display: flex;
            list-style: none;
            margin: 1rem 0;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .footer-links li {
            margin: 0 15px;
        }
        
        .footer-links a {
            color: white;
            text-decoration: none;
        }
        
        .footer-links a:hover {
            color: var(--shiite-gold);
        }
        
        .copyright {
            margin-top: 1rem;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            .browser-controls {
                flex-direction: column;
            }
            
            .surah-selector, .ayah-selector, .translation-selector {
                margin: 0 0 10px 0;
            }
            
            .arabic-text {
                font-size: 1.5rem;
            }
            
            .footer-links {
                flex-direction: column;
            }
            
            .footer-links li {
                margin: 5px 0;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&family=Scheherazade+New:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-quran"></i>
                <span>القرآن الشيعي - الترجمة الإنجليزية</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#">الرئيسية</a></li>
                    <li><a href="#">التفاسير الشيعية</a></li>
                    <li><a href="#">أهل البيت</a></li>
                    <li><a href="#">المفضلة</a></li>
                    <li><a href="#">اتصل بنا</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>القرآن الكريم بالترجمة الإنجليزية وفق المذهب الشيعي</h1>
            <p>موقع متخصص في ترجمة وتفسير القرآن الكريم وفق روايات وتفاسير أهل البيت (عليهم السلام)</p>
            <div class="shiite-badge">مصادر شيعية معتمدة</div>
        </div>
    </section>

    <main class="container">
        <section class="quran-browser">
            <div class="browser-controls">
                <div class="surah-selector">
                    <select id="surah-select">
                        <option value="">اختر السورة</option>
                        <option value="1">سورة الفاتحة</option>
                        <option value="2">سورة البقرة</option>
                        <option value="33">سورة الأحزاب</option>
                        <option value="42">سورة الشورى</option>
                        <option value="61">سورة الصف</option>
                        <option value="98">سورة البينة</option>
                    </select>
                </div>
                <div class="ayah-selector">
                    <select id="ayah-select">
                        <option value="">اختر الآية</option>
                    </select>
                </div>
                <div class="translation-selector">
                    <select id="translation-select">
                        <option value="shiite">ترجمة شيعية</option>
                        <option value="pooya">تفسير پويا</option>
                        <option value="qomi">تفسير القمي</option>
                    </select>
                </div>
                <div class="action-buttons">
                    <button id="view-button"><i class="fas fa-eye"></i> عرض الآية</button>
                </div>
            </div>

            <div class="quran-display">
                <div class="surah-header">
                    <h2 id="surah-name">سورة الفاتحة</h2>
                    <p id="surah-info">مكية - 7 آيات</p>
                </div>
                
                <div class="verse-container">
                    <span class="verse-number">1</span>
                    <div class="arabic-text" id="arabic-text">
                        بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ
                    </div>
                    <div class="translation-source">ترجمة شيعية معتمدة:</div>
                    <div class="translation-text" id="translation-text">
                        In the name of Allah, the Entirely Merciful, the Especially Merciful.
                    </div>
                    <div class="transliteration" id="transliteration">
                        Bismillāhir-Raĥmānir-Raĥīm
                    </div>
                    
                    <div class="shiite-interpretation">
                        <h4><i class="fas fa-star"></i> تفسير شيعي</h4>
                        <p>روي عن الإمام جعفر الصادق (ع) في تفسير البسملة: "الله هو المعبود، الرحمن بجميع خلقه، الرحيم بالمؤمنين خاصة".</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="resources">
            <h2>مصادر شيعية معتمدة</h2>
            <div class="resource-list">
                <div class="resource-item">
                    <h4>تفسير الميزان</h4>
                    <p>للعلامة السيد محمد حسين الطباطبائي</p>
                </div>
                <div class="resource-item">
                    <h4>تفسير نور الثقلين</h4>
                    <p>للحويزي</p>
                </div>
                <div class="resource-item">
                    <h4>تفسير القمي</h4>
                    <p>لعلي بن إبراهيم القمي</p>
                </div>
                <div class="resource-item">
                    <h4>تفسير البرهان</h4>
                    <p>للسيد هاشم البحراني</p>
                </div>
            </div>
        </section>

        <section class="features">
            <div class="feature-card">
                <i class="fas fa-book-open"></i>
                <h3>ترجمة شيعية</h3>
                <p>ترجمة دقيقة وفق روايات أهل البيت (عليهم السلام) وتفاسير المذهب الشيعي</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-microphone"></i>
                <h3>تلاوات</h3>
                <p>استمع إلى التلاوات القرآنية بقُرّاء شيعية معتمدين</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-graduation-cap"></i>
                <h3>تفاسير أهل البيت</h3>
                <p>وصول إلى شروح وتفاسير القرآن المروية عن الأئمة المعصومين</p>
            </div>
        </section>
    </main>

    <footer>
        <div class="container footer-content">
            <div class="footer-logo">
                <i class="fas fa-quran"></i>
                <span>القرآن الشيعي - الترجمة الإنجليزية</span>
            </div>
            <ul class="footer-links">
                <li><a href="#">عن الموقع</a></li>
                <li><a href="#">المصادر والمراجع</a></li>
                <li><a href="#">اتصل بنا</a></li>
                <li><a href="#">سياسة الخصوصية</a></li>
            </ul>
            <div class="copyright">
                &copy; 2023 موقع ترجمة القرآن الكريم وفق المذهب الشيعي. جميع الحقوق محفوظة.
            </div>
        </div>
    </footer>

    <script>
        // نموذج بسيط للبيانات (في التطبيق الحقيقي، ستأتي هذه البيانات من قاعدة بيانات أو API)
        const quranData = {
            "1": {
                name: "سورة الفاتحة",
                info: "مكية - 7 آيات",
                ayahs: {
                    1: {
                        arabic: "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
                        translation: "In the name of Allah, the Entirely Merciful, the Especially Merciful.",
                        transliteration: "Bismillāhir-Raĥmānir-Raĥīm",
                        shiiteTafsir: "روي عن الإمام جعفر الصادق (ع) في تفسير البسملة: 'الله هو المعبود، الرحمن بجميع خلقه، الرحيم بالمؤمنين خاصة'."
                    },
                    2: {
                        arabic: "الْحَمْدُ لِلَّهِ رَبِّ الْعَالَمِينَ",
                        translation: "[All] praise is [due] to Allah, Lord of the worlds -",
                        transliteration: "Al-Ĥamdu lillāhi Rabbi l-'Ālamīn",
                        shiiteTafsir: "عن الإمام الباقر (ع): 'الحمد لله هو الشكر لله على ما أنعم، ورب العالمين يعني رب جميع الخلائق'."
                    }
                }
            },
            "98": {
                name: "سورة البينة",
                info: "مدنية - 8 آيات",
                ayahs: {
                    1: {
                        arabic: "لَمْ يَكُنِ الَّذِينَ كَفَرُوا مِنْ أَهْلِ الْكِتَابِ وَالْمُشْرِكِينَ مُنفَكِّينَ حَتَّىٰ تَأْتِيَهُمُ الْبَيِّنَةُ",
                        translation: "Those who disbelieved among the People of the Scripture and the polytheists were not to be parted [from misbelief] until there came to them clear evidence -",
                        transliteration: "Lam yakuni allatheena kafaroo min ahli alkitabi waalmushrikeena munfakkeena hatta tatiyahumu albayyinatu",
                        shiiteTafsir: "روي عن الإمام الصادق (ع) أن البينة هي الإمام علي (ع) والأئمة من ولده، وهم الحجة البالغة على الناس."
                    }
                }
            }
        };

        // عناصر DOM
        const surahSelect = document.getElementById('surah-select');
        const ayahSelect = document.getElementById('ayah-select');
        const viewButton = document.getElementById('view-button');
        const arabicText = document.getElementById('arabic-text');
        const translationText = document.getElementById('translation-text');
        const transliterationText = document.getElementById('transliteration');
        const surahName = document.getElementById('surah-name');
        const surahInfo = document.getElementById('surah-info');
        const tafsirElement = document.querySelector('.shiite-interpretation p');

        // عند تغيير السورة
        surahSelect.addEventListener('change', function() {
            const surahId = this.value;
            ayahSelect.innerHTML = '<option value="">اختر الآية</option>';
            
            if (surahId && quranData[surahId]) {
                const surah = quranData[surahId];
                surahName.textContent = surah.name;
                surahInfo.textContent = surah.info;
                
                const ayahs = surah.ayahs;
                for (let ayahNum in ayahs) {
                    const option = document.createElement('option');
                    option.value = ayahNum;
                    option.textContent = `آية ${ayahNum}`;
                    ayahSelect.appendChild(option);
                }
            }
        });

        // عند النقر على زر العرض
        viewButton.addEventListener('click', function() {
            const surahId = surahSelect.value;
            const ayahId = ayahSelect.value;
            
            if (surahId && ayahId && quranData[surahId] && quranData[surahId].ayahs[ayahId]) {
                const ayah = quranData[surahId].ayahs[ayahId];
                arabicText.textContent = ayah.arabic;
                translationText.textContent = ayah.translation;
                transliterationText.textContent = ayah.transliteration;
                tafsirElement.textContent = ayah.shiiteTafsir;
            } else {
                // عرض الآية الافتراضية (بسم الله الرحمن الرحيم)
                arabicText.textContent = "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ";
                translationText.textContent = "In the name of Allah, the Entirely Merciful, the Especially Merciful.";
                transliterationText.textContent = "Bismillāhir-Raĥmānir-Raĥīm";
                tafsirElement.textContent = "روي عن الإمام جعفر الصادق (ع) في تفسير البسملة: 'الله هو المعبود، الرحمن بجميع خلقه، الرحيم بالمؤمنين خاصة'.";
            }
        });
    </script>
</body>
</html>
