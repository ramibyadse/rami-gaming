[rami-gaming-index.html](https://github.com/user-attachments/files/23194358/rami-gaming-index.html)
<!--
  Rami Gaming - Single-file HTML mockup
  اللغة الافتراضية: العربية (RTL). يوجد زر لتبديل اللغة إلى الإنجليزية.
  يحتوي على: الصفحة الرئيسية، المنتجات/الألعاب، الأخبار، من نحن، تواصل معنا.
  ستايل: داكن (أسود/بنفسجي). مبني بـ HTML / CSS / JavaScript (بدون مكتبات).
-->

<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>رامي جيمنج — Rami Gaming</title>
  <style>
    :root{
      --bg:#0b0b10;
      --card:#0f0f16;
      --muted:#bfb7e6;
      --accent1:#7b3cff; /* purple */
      --accent2:#a86bff;
      --glass: rgba(255,255,255,0.03);
      --danger:#ff4d6d;
      --radius:12px;
      --maxw:1200px;
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0;
      background:linear-gradient(180deg,var(--bg) 0%, #07070a 100%);
      color:#e9e6ff;
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.4;
      padding-bottom:60px;
    }

    /* Container */
    .wrap{max-width:var(--maxw);margin:28px auto;padding:18px}

    /* Header */
    header{
      display:flex;align-items:center;justify-content:space-between;gap:18px;margin-bottom:22px;
    }
    .brand{
      display:flex;gap:14px;align-items:center;
    }
    .logo{
      width:56px;height:56px;border-radius:14px;background:linear-gradient(135deg,var(--accent1),var(--accent2));display:flex;align-items:center;justify-content:center;font-weight:800;color:white;font-size:20px;box-shadow:0 6px 18px rgba(123,60,255,0.14);
    }
    .site-title{font-size:20px;font-weight:700}
    .site-sub{font-size:12px;color:var(--muted)}

    nav ul{Display:flex;gap:14px;align-items:center;list-style:none;padding:0;margin:0}
    nav a{padding:8px 12px;border-radius:10px;text-decoration:none;color:var(--muted);font-weight:600}
    nav a.active, nav a:hover{background:linear-gradient(90deg, rgba(123,60,255,0.14), rgba(168,107,255,0.08));color:#fff}

    .controls{display:flex;gap:10px;align-items:center}
    .btn{background:var(--glass);padding:8px 12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);cursor:pointer;color:var(--muted);font-weight:600}
    .btn.primary{background:linear-gradient(90deg,var(--accent1),var(--accent2));box-shadow:0 8px 28px rgba(123,60,255,0.12);color:white}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:22px;align-items:center;margin-bottom:28px}
    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:20px;border-radius:18px;border:1px solid rgba(255,255,255,0.03)}
    .hero h1{margin:0 0 8px 0;font-size:32px}
    .hero p{margin:0;color:var(--muted)}

    .promo{background:linear-gradient(90deg, rgba(123,60,255,0.18), rgba(168,107,255,0.12));padding:18px;border-radius:14px;text-align:center}
    .promo h3{margin:0 0 6px}
    .promo p{margin:0;color:#fff;font-weight:600}

    /* Sections */
    section{margin-bottom:28px}
    .section-title{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px}
    .section-title h2{margin:0;font-size:18px}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px}

    /* Product card */
    .card{background:var(--card);padding:14px;border-radius:14px;border:1px solid rgba(255,255,255,0.03);display:flex;flex-direction:column;gap:10px}
    .media{height:140px;border-radius:10px;background:linear-gradient(135deg,#12081a, #21112f);display:flex;align-items:center;justify-content:center;font-weight:700}
    .meta{display:flex;justify-content:space-between;align-items:center}
    .price{font-weight:800}
    .muted{color:var(--muted);font-size:13px}
    .tags{display:flex;gap:8px}
    .tag{padding:6px 8px;border-radius:999px;background:rgba(255,255,255,0.03);font-size:12px}
    .card .actions{display:flex;gap:8px}

    /* News */
    .news-item{display:flex;gap:12px;align-items:flex-start}
    .news-item img{width:120px;height:72px;object-fit:cover;border-radius:8px}

    /* Footer */
    footer{margin-top:26px;padding:16px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);display:flex;justify-content:space-between;align-items:center}

    /* Contact form */
    form{display:grid;gap:10px}
    input,textarea,select{background:transparent;border:1px solid rgba(255,255,255,0.05);padding:10px;border-radius:8px;color:inherit}

    /* Responsive */
    @media (max-width:880px){
      .hero{grid-template-columns:1fr}
      .brand .site-title{display:none}
      nav ul{display:none}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo">ر</div>
        <div>
          <div class="site-title" data-i18n="siteTitle">رامي جيمنج</div>
          <div class="site-sub" data-i18n="siteSub">متجر الألعاب والأجهزة بأسعار معقولة</div>
        </div>
      </div>

      <nav>
        <ul>
          <li><a href="#home" class="active" data-nav data-i18n="navHome">الرئيسية</a></li>
          <li><a href="#products" data-nav data-i18n="navProducts">المنتجات</a></li>
          <li><a href="#news" data-nav data-i18n="navNews">الأخبار</a></li>
          <li><a href="#about" data-nav data-i18n="navAbout">من نحن</a></li>
          <li><a href="#contact" data-nav data-i18n="navContact">تواصل معنا</a></li>
        </ul>
      </nav>

      <div class="controls">
        <button class="btn" id="langToggle">English</button>
        <button class="btn primary" data-i18n="btnShop">تسوّق الآن</button>
      </div>
    </header>

    <!-- HERO -->
    <section id="home" class="hero">
      <div class="hero-card">
        <h1 data-i18n="heroTitle">أهلاً بك في رامي جيمنج</h1>
        <p data-i18n="heroDesc">أفضل العروض على الألعاب، الأجهزة، والاكسسوارات — كل ذلك بأسعار معقولة ومضمونة.</p>

        <div style="height:14px"></div>
        <div style="display:flex;gap:12px;flex-wrap:wrap">
          <div class="tag">توصيل سريع</div>
          <div class="tag">ضمان ٦ أشهر</div>
          <div class="tag">دعم فني</div>
        </div>

        <div style="height:14px"></div>
        <div class="promo">
          <h3 data-i18n="promoTitle">عرض خاص</h3>
          <p data-i18n="promoDesc">خصم حتى 20% على الألعاب المختارة — سارع بالحصول على نسختك!</p>
        </div>
      </div>

      <aside>
        <div class="hero-card">
          <h3 data-i18n="topSellers">الأكثر مبيعًا</h3>
          <div style="height:10px"></div>
          <div class="grid" style="grid-template-columns:1fr">
            <div class="card">
              <div class="meta">
                <div>
                  <div style="font-weight:800">PlayStation 5</div>
                  <div class="muted">جهاز منزلي</div>
                </div>
                <div class="price">₪2,199</div>
              </div>
            </div>
            <div class="card">
              <div class="meta">
                <div>
                  <div style="font-weight:800">Cyberpunk 2077</div>
                  <div class="muted">للكمبيوتر</div>
                </div>
                <div class="price">₪129</div>
              </div>
            </div>
          </div>
        </div>
      </aside>
    </section>

    <!-- PRODUCTS -->
    <section id="products">
      <div class="section-title">
        <h2 data-i18n="productsTitle">المنتجات / الألعاب</h2>
        <div class="muted" data-i18n="productsSub">عرض لأشهر الأجهزة والألعاب - اضغط على "اشترِ الآن" للمحاكاة</div>
      </div>

      <div class="grid" id="productGrid">
        <!-- المنتجات ستُنشأ ديناميكياً من JavaScript -->
      </div>
    </section>

    <!-- NEWS -->
    <section id="news">
      <div class="section-title">
        <h2 data-i18n="newsTitle">الأخبار</h2>
        <div class="muted" data-i18n="newsSub">آخر أخبار الألعاب والإصدارات</div>
      </div>

      <div class="grid">
        <article class="card news-item">
          <img src="https://picsum.photos/seed/game1/400/240" alt="news">
          <div>
            <h3 style="margin:0">إصدار لعبة جديدة يتصدر المبيعات</h3>
            <div class="muted">20 أكتوبر 2025 — أصدرت الشركة...</div>
            <p class="muted">نسخة مختصرة للخبر لعرض التصميم. يمكنك استبدال هذه الفقرة بالمحتوى الحقيقي لاحقًا.</p>
          </div>
        </article>

        <article class="card news-item">
          <img src="https://picsum.photos/seed/game2/400/240" alt="news">
          <div>
            <h3 style="margin:0">خصومات نهاية الموسم على الاكسسوارات</h3>
            <div class="muted">12 سبتمبر 2025</div>
            <p class="muted">عروض حقيقية على سماعات ولوحات المفاتيح ومقاعد الألعاب.</p>
          </div>
        </article>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="section-title">
        <h2 data-i18n="aboutTitle">من نحن</h2>
      </div>
      <div class="card">
        <p data-i18n="aboutText">رامي جيمنج متجر افتراضي مُصمَّم لعشاق الألعاب. هدفنا توفير أجهزة مبتكرة، ألعاب أصلية، واكسسوارات بجودة معقولة ودعم ممتاز.</p>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="section-title">
        <h2 data-i18n="contactTitle">تواصل معنا</h2>
      </div>
      <div class="card">
        <form id="contactForm">
          <input type="text" placeholder="الاسم" data-i18n-placeholder="contactName" required>
          <input type="email" placeholder="البريد الإلكتروني" data-i18n-placeholder="contactEmail" required>
          <textarea rows="4" placeholder="رسالتك" data-i18n-placeholder="contactMessage"></textarea>
          <div style="display:flex;gap:8px;justify-content:flex-end">
            <button type="submit" class="btn primary" data-i18n="contactSend">إرسال الرسالة</button>
          </div>
        </form>
      </div>
    </section>

    <footer>
      <div>
        <strong>رامي جيمنج</strong>
        <div class="muted">© 2025 - جميع الحقوق محفوظة</div>
      </div>
      <div class="muted">تصميم افتراضي • متجر عرضي</div>
    </footer>
  </div>

  <script>
    // --- بيانات المنتجات (يمكنك تعديلها أو جلبها من API لاحقًا) ---
    const products = [
      {id:1,name_ar:'PlayStation 5',name_en:'PlayStation 5',type:'جهاز',price:'₪2,199',price_num:2199,tag:'جديد'},
      {id:2,name_ar:'Xbox Series X',name_en:'Xbox Series X',type:'جهاز',price:'₪1,999',price_num:1999,tag:'شائع'},
      {id:3,name_ar:'Corsair K70 لوحة مفاتيح',name_en:'Corsair K70 Keyboard',type:'اكسسوار',price:'₪429',price_num:429,tag:'خصم'},
      {id:4,name_ar:'Cyberpunk 2077',name_en:'Cyberpunk 2077 (PC)',type:'لعبة',price:'₪129',price_num:129,tag:'ألعاب'},
      {id:5,name_ar:'Elden Ring',name_en:'Elden Ring',type:'لعبة',price:'₪169',price_num:169,tag:'مميز'},
    ];

    const productGrid = document.getElementById('productGrid');

    function renderProducts(lang='ar'){
      productGrid.innerHTML = '';
      products.forEach(p =>{
        const card = document.createElement('article');
        card.className = 'card';
        card.innerHTML = `
          <div class="media">${p.name_en}</div>
          <div>
            <div style="font-weight:800">${lang==='ar'?p.name_ar:p.name_en}</div>
            <div class="muted">${p.type}</div>
          </div>
          <div class="meta">
            <div class="tags"><div class="tag">${p.tag}</div></div>
            <div class="price">${p.price}</div>
          </div>
          <div class="actions">
            <button class="btn">${lang==='ar'? 'اشترِ الآن':'Buy Now'}</button>
            <button class="btn">${lang==='ار'? 'تفاصيل':'Details'}</button>
          </div>
        `;
        productGrid.appendChild(card);
      })
    }

    // --- ترجمة بسيطة والتبديل بين العربية والإنجليزية ---
    const i18n = {
      ar: {
        siteTitle:'رامي جيمنج', siteSub:'متجر الألعاب والأجهزة بأسعار معقولة',
        navHome:'الرئيسية', navProducts:'المنتجات', navNews:'الأخبار', navAbout:'من نحن', navContact:'تواصل معنا',
        btnShop:'تسوّق الآن',
        heroTitle:'أهلاً بك في رامي جيمنج', heroDesc:'أفضل العروض على الألعاب، الأجهزة، والاكسسوارات — كل ذلك بأسعار معقولة ومضمونة.',
        promoTitle:'عرض خاص', promoDesc:'خصم حتى 20% على الألعاب المختارة — سارع بالحصول على نسختك!',
        topSellers:'الأكثر مبيعًا',
        productsTitle:'المنتجات / الألعاب', productsSub:'عرض لأشهر الأجهزة والألعاب - اضغط على "اشترِ الآن" للمحاكاة',
        newsTitle:'الأخبار', newsSub:'آخر أخبار الألعاب والإصدارات',
        aboutTitle:'من نحن', aboutText:'رامي جيمنج متجر افتراضي مُصمَّم لعشاق الألعاب. هدفنا توفير أجهزة مبتكرة، ألعاب أصلية، واكسسوارات بجودة معقولة ودعم ممتاز.',
        contactTitle:'تواصل معنا', contactName:'الاسم', contactEmail:'البريد الإلكتروني', contactMessage:'رسالتك', contactSend:'إرسال الرسالة'
      },
      en: {
        siteTitle:'Rami Gaming', siteSub:'Affordable games & gear',
        navHome:'Home', navProducts:'Products', navNews:'News', navAbout:'About', navContact:'Contact',
        btnShop:'Shop Now',
        heroTitle:'Welcome to Rami Gaming', heroDesc:'Top deals on games, consoles, and accessories — affordable prices you can trust.',
        promoTitle:'Special Offer', promoDesc:'Up to 20% off selected games — grab your copy today!',
        topSellers:'Top Sellers',
        productsTitle:'Products / Games', productsSub:'Showcasing top consoles and games - click "Buy Now" for demo',
        newsTitle:'News', newsSub:'Latest gaming releases and updates',
        aboutTitle:'About Us', aboutText:'Rami Gaming is a demo store for gamers. We provide original games, reliable gear, and affordable prices with great support.',
        contactTitle:'Contact', contactName:'Name', contactEmail:'Email', contactMessage:'Your message', contactSend:'Send Message'
      }
    }

    let currentLang = 'ar';
    const langBtn = document.getElementById('langToggle');

    function applyLang(lang){
      currentLang = lang;
      document.documentElement.lang = (lang==='ar')? 'ar' : 'en';
      document.documentElement.dir = (lang==='ar')? 'rtl' : 'ltr';

      // عناصر تحتوي على data-i18n
      document.querySelectorAll('[data-i18n]').forEach(el=>{
        const key = el.getAttribute('data-i18n');
        if(i18n[lang] && i18n[lang][key]) el.textContent = i18n[lang][key];
      })

      // عناصر placeholder
      document.querySelectorAll('[data-i18n-placeholder]').forEach(el=>{
        const key = el.getAttribute('data-i18n-placeholder');
        if(i18n[lang] && i18n[lang][key]) el.placeholder = i18n[lang][key];
      })

      // زر اللغة
      langBtn.textContent = (lang==='ar')? 'English' : 'العربية';

      // اعادة عرض المنتجات
      renderProducts(lang);
    }

    langBtn.addEventListener('click',()=>{
      applyLang(currentLang==='ar' ? 'en' : 'ar');
    })

    // تنقّل داخلي سريع
    document.querySelectorAll('[data-nav]').forEach(a=>{
      a.addEventListener('click',(e)=>{
        document.querySelectorAll('nav a').forEach(x=>x.classList.remove('active'));
        e.target.classList.add('active');
      })
    })

    // نموذج الاتصال (محاكاة إرسال)
    document.getElementById('contactForm').addEventListener('submit', (e)=>{
      e.preventDefault();
      alert(currentLang==='ar' ? 'تم إرسال رسالتك! سنتواصل معك قريبًا.' : 'Your message was sent! We will contact you soon.');
      e.target.reset();
    })

    // عرض أولي
    applyLang('ar');
  </script>
</body>
</html>
