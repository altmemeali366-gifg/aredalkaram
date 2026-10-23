[code_artifact.html](https://github.com/user-attachments/files/33889179/code_artifact.html)
<!doctype html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#087fc3">
<meta name="description" content="الموسوعة التدريبية التفاعلية المصوّرة لشركة أرض الكرم: الدعم الفني، خدمة العملاء، المبيعات، التدريب، والصيانة الميدانية. إعداد وتطوير: علي وجدي.">
<title>الموسوعة التدريبية المصوّرة والمتحركة | أكاديمية أرض الكرم</title>
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    darkMode: 'class',
    theme: {
      extend: {
        colors: {
          brand: {
            navy: '#0b1b33',
            dark: '#081324',
            blue: '#0785ce',
            cyan: '#00c2cb',
            teal: '#0b9f87',
            accent: '#ff9800',
            cardDark: '#0f223d'
          }
        },
        fontFamily: {
          cairo: ['Cairo', 'sans-serif']
        },
        animation: {
          'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
          'float': 'float 6s ease-in-out infinite',
          'spin-slow': 'spin 20s linear infinite',
        },
        keyframes: {
          float: {
            '0%, 100%': { transform: 'translateY(0px) rotate(0deg)' },
            '50%': { transform: 'translateY(-12px) rotate(1.5deg)' }
          }
        }
      }
    }
  }
</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #0785ce;
    --primary-glow: rgba(7, 133, 206, 0.35);
  }
  body {
    font-family: 'Cairo', sans-serif;
  }
  /* Scroll Progress Bar */
  #scrollProgress {
    position: fixed;
    top: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #00c2cb, #0785ce, #2563eb, #10b981);
    z-index: 100;
    width: 0%;
    transition: width 0.1s ease-out;
  }
  /* Glowing LEDs */
  .led {
    position: relative;
    transition: all 0.3s ease;
  }
  .led.on-green {
    background-color: #10b981;
    box-shadow: 0 0 10px #10b981, 0 0 20px #10b981;
  }
  .led.on-red {
    background-color: #ef4444;
    box-shadow: 0 0 10px #ef4444, 0 0 22px #ef4444;
  }
  .led.on-blue {
    background-color: #0ea5e9;
    box-shadow: 0 0 10px #0ea5e9, 0 0 20px #0ea5e9;
  }
  .led.blink-slow {
    animation: blinkLed 1.2s infinite;
  }
  .led.blink-fast {
    animation: blinkLed 0.5s infinite;
  }
  .led.off {
    background-color: #475569;
    box-shadow: none;
    opacity: 0.35;
  }
  @keyframes blinkLed {
    0%, 100% { opacity: 1; filter: brightness(1.2); }
    50% { opacity: 0.2; filter: brightness(0.7); }
  }
  /* Interactive 3D Card Hover */
  .tilt-card {
    transition: transform 0.2s cubic-bezier(0.2, 0, 0.3, 1), box-shadow 0.2s ease, border-color 0.2s ease;
    transform-style: preserve-3d;
  }
  .tilt-card:hover {
    transform: translateY(-6px);
  }
  /* Custom scrollbar */
  ::-webkit-scrollbar {
    width: 8px;
  }
  ::-webkit-scrollbar-track {
    background: #0b1b3310;
  }
  ::-webkit-scrollbar-thumb {
    background: #0785ce60;
    border-radius: 9999px;
  }
  ::-webkit-scrollbar-thumb:hover {
    background: #0785ce;
  }
  /* Fiber Mesh Canvas */
  #fiberCanvas {
    position: absolute;
    inset: 0;
    pointer-events: none;
    z-index: 0;
    opacity: 0.65;
  }
</style>
</head>
<body class="bg-slate-50 dark:bg-slate-950 text-slate-800 dark:text-slate-100 transition-colors duration-300 selection:bg-brand-blue selection:text-white">

<!-- Scroll Progress -->
<div id="scrollProgress"></div>

<!-- Top Dynamic Ambient Glow Bar -->
<div class="h-1.5 w-full bg-gradient-to-r from-cyan-400 via-blue-600 to-teal-400 animate-pulse"></div>

<!-- Interactive Navigation -->
<header class="sticky top-0 z-50 bg-white/90 dark:bg-slate-900/90 backdrop-blur-xl border-b border-slate-200/80 dark:border-slate-800/80 transition-all">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between gap-4">
    <!-- Brand -->
    <a href="#home" class="flex items-center gap-3.5 group" aria-label="الرئيسية">
      <div class="relative w-12 h-12 rounded-2xl bg-gradient-to-tr from-brand-blue to-cyan-500 p-0.5 shadow-lg shadow-brand-blue/30 group-hover:scale-105 transition-transform duration-300 flex-shrink-0">
        <div class="w-full h-full bg-white dark:bg-slate-900 rounded-[14px] flex items-center justify-center overflow-hidden">
          <span class="text-xl font-black bg-gradient-to-r from-brand-blue to-teal-500 bg-clip-text text-transparent group-hover:rotate-12 transition-transform duration-300">AK</span>
        </div>
      </div>
      <div>
        <b class="text-base font-extrabold tracking-tight text-slate-900 dark:text-white flex items-center gap-1.5">
          شركة أرض الكرم
          <span class="w-2 h-2 rounded-full bg-emerald-500 animate-ping"></span>
        </b>
        <small class="text-xs text-slate-500 dark:text-slate-400 block -mt-0.5 font-medium">أكاديمية التدريب والمعرفة التقنية</small>
      </div>
    </a>

    <!-- Nav Links (Desktop) -->
    <nav id="desktopNav" class="hidden md:flex items-center gap-1 lg:gap-2">
      <a href="#home" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition">الرئيسية</a>
      <a href="#simulator" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition flex items-center gap-1">
        <span class="w-1.5 h-1.5 rounded-full bg-brand-cyan animate-pulse"></span>
        مختبر الأعطال
      </a>
      <a href="#departments" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition">الأقسام</a>
      <a href="#devices" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition">أجهزة الفايبر</a>
      <a href="#routers" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition">الراوترات</a>
      <a href="#offers" class="px-3 py-1.5 text-xs lg:text-sm font-bold text-slate-600 dark:text-slate-300 hover:text-brand-blue dark:hover:text-cyan-400 rounded-lg hover:bg-slate-100 dark:hover:bg-slate-800/60 transition">الباقات</a>
    </nav>

    <!-- Controls -->
    <div class="flex items-center gap-3">
      <!-- Dark mode switch -->
      <button id="themeToggle" class="p-2.5 rounded-xl border border-slate-200 dark:border-slate-700 bg-white dark:bg-slate-800 text-slate-600 dark:text-yellow-400 hover:scale-105 active:scale-95 transition shadow-sm" aria-label="تبديل المظهر">
        <span id="themeIcon" class="text-base block">🌙</span>
      </button>

      <!-- Search modal trigger -->
      <button id="quickSearchBtn" class="hidden sm:inline-flex items-center gap-2 px-3 py-2 rounded-xl text-xs font-bold border border-slate-200 dark:border-slate-700 bg-slate-100/80 dark:bg-slate-800 text-slate-500 dark:text-slate-300 hover:border-brand-blue/50 transition">
        <span>🔍 بحث سريع في الأدلة</span>
        <kbd class="px-1.5 py-0.5 text-[10px] rounded bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-700 font-mono">Ctrl+K</kbd>
      </button>

      <!-- CTA -->
      <a href="#simulator" class="inline-flex items-center gap-2 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-black text-white bg-gradient-to-r from-brand-blue to-teal-500 hover:from-blue-600 hover:to-teal-600 shadow-md shadow-brand-blue/25 hover:shadow-lg hover:shadow-brand-blue/40 transition active:scale-95">
        <span>فحص فوري</span>
        <span class="animate-bounce font-mono">←</span>
      </a>

      <!-- Mobile Menu Button -->
      <button id="mobileMenuBtn" class="md:hidden p-2.5 rounded-xl border border-slate-200 dark:border-slate-700 text-slate-700 dark:text-slate-200" aria-label="القائمة">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
      </button>
    </div>
  </div>

  <!-- Mobile Dropdown -->
  <div id="mobileMenu" class="md:hidden hidden border-t border-slate-200 dark:border-slate-800 bg-white/95 dark:bg-slate-900/95 backdrop-blur-xl px-4 py-4 space-y-2">
    <a href="#home" class="block py-2 text-sm font-bold text-slate-700 dark:text-slate-200 hover:text-brand-blue">الرئيسية</a>
    <a href="#simulator" class="block py-2 text-sm font-bold text-brand-blue dark:text-cyan-400">⚡ مختبر الأعطال التفاعلي</a>
    <a href="#departments" class="block py-2 text-sm font-bold text-slate-700 dark:text-slate-200 hover:text-brand-blue">الأقسام التدريبية</a>
    <a href="#devices" class="block py-2 text-sm font-bold text-slate-700 dark:text-slate-200 hover:text-brand-blue">أجهزة الفايبر</a>
    <a href="#routers" class="block py-2 text-sm font-bold text-slate-700 dark:text-slate-200 hover:text-brand-blue">دليل الراوترات</a>
    <a href="#offers" class="block py-2 text-sm font-bold text-slate-700 dark:text-slate-200 hover:text-brand-blue">باقات المشتركين</a>
    <button id="mobileSearchTrigger" class="w-full text-right py-2.5 px-3 rounded-lg bg-slate-100 dark:bg-slate-800 text-xs font-bold text-slate-600 dark:text-slate-300">🔍 ابحث في المحتوى والأعطال...</button>
  </div>
</header>

<main class="relative overflow-hidden">

  <!-- ================= HERO SECTION WITH INTERACTIVE CANVAS ================= -->
  <section id="home" class="relative min-h-[720px] flex items-center py-16 lg:py-24 border-b border-slate-200/80 dark:border-slate-800">
    <canvas id="fiberCanvas"></canvas>
    
    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-8 items-center">
        
        <!-- Copy Left -->
        <div class="lg:col-span-7 text-right space-y-6">
          <div class="inline-flex items-center gap-2.5 px-4 py-1.5 rounded-full bg-cyan-50 dark:bg-cyan-950/50 border border-cyan-200 dark:border-cyan-800/80 shadow-sm">
            <span class="w-2.5 h-2.5 rounded-full bg-teal-500 animate-ping"></span>
            <span class="text-xs font-extrabold text-brand-blue dark:text-cyan-400 tracking-wide">تعلّم • فحص فوري • احتراف عملي</span>
          </div>

          <h1 class="text-3xl sm:text-5xl lg:text-6xl font-black text-slate-900 dark:text-white leading-[1.25] tracking-tight">
            الموسوعة التفاعلية لفريق 
            <span class="bg-gradient-to-l from-brand-blue via-cyan-500 to-teal-400 bg-clip-text text-transparent">أرض الكرم،</span>
            <br>
            بأسلوب عملي نابض بالحياة.
          </h1>

          <p class="text-sm sm:text-base text-slate-600 dark:text-slate-300 max-w-2xl leading-relaxed">
            المنصة المعرفية الرسمية لفريق الدعم الفني، خدمة العملاء (Call Center)، المبيعات، والكوادر الميدانية. تتضمن الآن محاكياً حياً لمؤشرات أجهزة ONU، تشخيص قراءات الباور الضوئي، وفاحص أعطال الفايبر خطوة بخطوة.
          </p>

          <div class="inline-flex flex-wrap items-center gap-3 p-2 rounded-2xl bg-white/80 dark:bg-slate-900/80 backdrop-blur border border-slate-200/90 dark:border-slate-800 shadow-md">
            <span class="text-xs font-bold text-slate-500 dark:text-slate-400 px-2">إعداد وتطوير المحتوى:</span>
            <span class="px-3 py-1 rounded-xl bg-blue-50 dark:bg-blue-900/40 text-brand-blue dark:text-cyan-300 text-xs font-black flex items-center gap-1.5">
              <span class="text-base">👨‍💻</span> علي وجدي
            </span>
          </div>

          <!-- Quick Action Buttons -->
          <div class="flex flex-wrap gap-3 pt-2">
            <a href="#simulator" class="inline-flex items-center justify-center gap-2 px-6 py-3.5 rounded-xl font-black text-sm text-white bg-gradient-to-r from-brand-blue to-teal-500 hover:shadow-xl hover:shadow-brand-blue/30 hover:-translate-y-0.5 active:translate-y-0 transition duration-200">
              <span>جرّب محاكي الأعطال (ONU Live)</span>
              <span>⚡</span>
            </a>
            <a href="#departments" class="inline-flex items-center justify-center gap-2 px-6 py-3.5 rounded-xl font-extrabold text-sm text-slate-700 dark:text-slate-200 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 hover:bg-slate-50 dark:hover:bg-slate-700/60 hover:-translate-y-0.5 transition duration-200 shadow-sm">
              <span>استعراض أقسام العمل</span>
              <span>📂</span>
            </a>
          </div>

          <!-- Quick Stats / Badges -->
          <div class="grid grid-cols-3 gap-4 pt-4 border-t border-slate-200 dark:border-slate-800">
            <div>
              <span class="block text-2xl sm:text-3xl font-black text-brand-blue dark:text-cyan-400">05</span>
              <span class="text-xs text-slate-500 dark:text-slate-400 font-bold">أقسام تخصصية</span>
            </div>
            <div>
              <span class="block text-2xl sm:text-3xl font-black text-teal-500 dark:text-teal-400">100%</span>
              <span class="text-xs text-slate-500 dark:text-slate-400 font-bold">سيناريوهات عملية</span>
            </div>
            <div>
              <span class="block text-2xl sm:text-3xl font-black text-blue-600 dark:text-blue-400">GPON</span>
              <span class="text-xs text-slate-500 dark:text-slate-400 font-bold">فحص بصري دقيق</span>
            </div>
          </div>
        </div>

        <!-- 3D Interactive Mockup Hero Right -->
        <div class="lg:col-span-5 relative flex justify-center">
          <div class="relative w-full max-w-md">
            <!-- Pulsing Ambient Circles -->
            <div class="absolute -top-10 -right-10 w-64 h-64 bg-cyan-400/20 dark:bg-cyan-500/10 rounded-full blur-3xl animate-pulse-slow"></div>
            <div class="absolute -bottom-10 -left-10 w-64 h-64 bg-blue-500/20 dark:bg-blue-600/10 rounded-full blur-3xl animate-pulse-slow" style="animation-delay: 1.5s;"></div>

            <!-- Floating Device Card -->
            <div class="relative bg-gradient-to-b from-white to-slate-100 dark:from-slate-800 dark:to-slate-900 border border-slate-200 dark:border-slate-700 rounded-3xl p-6 shadow-2xl shadow-brand-blue/20 animate-float">
              
              <!-- Device Top Bar -->
              <div class="flex items-center justify-between border-b border-slate-200 dark:border-slate-700/80 pb-4 mb-5">
                <div class="flex items-center gap-2">
                  <span class="w-3 h-3 rounded-full bg-emerald-500 shadow-md shadow-emerald-500/50 animate-ping"></span>
                  <span class="text-xs font-black text-slate-700 dark:text-slate-200">EARTH AL-KARAM • ONU ACTIVE</span>
                </div>
                <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-blue-50 dark:bg-blue-950 text-brand-blue dark:text-cyan-400 font-bold">GPON B+ CLASS</span>
              </div>

              <!-- Animated Signal Waves Device SVG -->
              <div class="relative h-48 bg-gradient-to-br from-slate-900 via-brand-dark to-slate-900 rounded-2xl p-4 flex flex-col justify-between overflow-hidden shadow-inner">
                <!-- Optical Fiber Line Animation -->
                <div class="absolute top-0 right-0 left-0 h-1 bg-gradient-to-r from-transparent via-cyan-400 to-transparent animate-pulse"></div>

                <div class="flex justify-between items-start">
                  <div>
                    <span class="text-[10px] tracking-wider text-slate-400 font-mono">RX POWER LEVEL</span>
                    <div class="text-2xl font-black text-cyan-400 font-mono flex items-baseline gap-1" id="heroRxDisplay">
                      -20.5 <span class="text-xs text-slate-400 font-sans">dBm (طبيعي)</span>
                    </div>
                  </div>
                  <span class="px-2.5 py-1 rounded-full text-[10px] font-black bg-emerald-500/20 text-emerald-400 border border-emerald-500/30 flex items-center gap-1">
                    <span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> الخدمة مستقرة
                  </span>
                </div>

                <!-- LEDs Row inside Device Mockup -->
                <div class="bg-black/40 backdrop-blur rounded-xl p-3 border border-slate-700/50 flex justify-between items-center text-center">
                  <div class="space-y-1">
                    <span class="text-[10px] text-slate-400 font-bold block">POWER</span>
                    <span class="w-3.5 h-3.5 rounded-full inline-block led on-green" id="heroLedPower"></span>
                  </div>
                  <div class="space-y-1">
                    <span class="text-[10px] text-slate-400 font-bold block">PON</span>
                    <span class="w-3.5 h-3.5 rounded-full inline-block led on-green" id="heroLedPon"></span>
                  </div>
                  <div class="space-y-1">
                    <span class="text-[10px] text-slate-400 font-bold block">LOS</span>
                    <span class="w-3.5 h-3.5 rounded-full inline-block led off" id="heroLedLos"></span>
                  </div>
                  <div class="space-y-1">
                    <span class="text-[10px] text-slate-400 font-bold block">LAN</span>
                    <span class="w-3.5 h-3.5 rounded-full inline-block led on-blue blink-fast" id="heroLedLan"></span>
                  </div>
                </div>

                <div class="flex justify-between items-center text-[11px] text-slate-400 pt-1">
                  <span>تزامن البيانات: <b>مستمر 1.25 Gbps</b></span>
                  <span class="font-mono text-cyan-400">FTTH ONLINE</span>
                </div>
              </div>

              <!-- Quick Action Inside Card -->
              <div class="mt-4 flex items-center justify-between text-xs text-slate-500 dark:text-slate-400">
                <span>تحديث الحالة الفوري: <b class="text-emerald-600 dark:text-emerald-400">متصل بالشبكة</b></span>
                <a href="#simulator" class="text-brand-blue dark:text-cyan-400 font-extrabold hover:underline">اختبر الأعطال هنا ←</a>
              </div>
            </div>

            <!-- Floating Mini Badges -->
            <div class="absolute -top-4 -left-4 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-2xl p-3 shadow-xl flex items-center gap-3">
              <span class="w-9 h-9 rounded-xl bg-blue-100 dark:bg-blue-900/50 text-brand-blue dark:text-cyan-400 flex items-center justify-center text-lg font-black">📶</span>
              <div>
                <b class="text-xs text-slate-800 dark:text-slate-100 block">Wi-Fi 6 & FTTH</b>
                <span class="text-[10px] text-slate-500 dark:text-slate-400">تشخيص التغطية والراوتر</span>
              </div>
            </div>

            <div class="absolute -bottom-4 -right-4 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-2xl p-3 shadow-xl flex items-center gap-3">
              <span class="w-9 h-9 rounded-xl bg-emerald-100 dark:bg-emerald-900/50 text-emerald-600 dark:text-emerald-400 flex items-center justify-center text-lg font-black">✓</span>
              <div>
                <b class="text-xs text-slate-800 dark:text-slate-100 block">تدريب عملي معتمد</b>
                <span class="text-[10px] text-slate-500 dark:text-slate-400">كول سنتر ودعم وصيانة</span>
              </div>
            </div>

          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ================= TRUST & VALUE STRIP ================= -->
  <section class="py-6 border-b border-slate-200 dark:border-slate-800 bg-white/60 dark:bg-slate-900/60 backdrop-blur-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-2 md:grid-cols-4 gap-4 text-center">
        <div class="flex items-center justify-center gap-2 text-slate-700 dark:text-slate-300 text-xs sm:text-sm font-extrabold p-2 rounded-xl hover:bg-slate-100 dark:hover:bg-slate-800/50 transition">
          <span class="w-7 h-7 rounded-lg bg-blue-100 dark:bg-blue-950 text-brand-blue flex items-center justify-center font-black">✦</span>
          شرح بصري فوري ومبسّط
        </div>
        <div class="flex items-center justify-center gap-2 text-slate-700 dark:text-slate-300 text-xs sm:text-sm font-extrabold p-2 rounded-xl hover:bg-slate-100 dark:hover:bg-slate-800/50 transition">
          <span class="w-7 h-7 rounded-lg bg-teal-100 dark:bg-teal-950 text-teal-600 flex items-center justify-center font-black">▧</span>
          محاكي لمبات ONU التفاعلي
        </div>
        <div class="flex items-center justify-center gap-2 text-slate-700 dark:text-slate-300 text-xs sm:text-sm font-extrabold p-2 rounded-xl hover:bg-slate-100 dark:hover:bg-slate-800/50 transition">
          <span class="w-7 h-7 rounded-lg bg-purple-100 dark:bg-purple-950 text-purple-600 flex items-center justify-center font-black">⌘</span>
          سيناريوهات كول سنتر حية
        </div>
        <div class="flex items-center justify-center gap-2 text-slate-700 dark:text-slate-300 text-xs sm:text-sm font-extrabold p-2 rounded-xl hover:bg-slate-100 dark:hover:bg-slate-800/50 transition">
          <span class="w-7 h-7 rounded-lg bg-amber-100 dark:bg-amber-950 text-amber-600 flex items-center justify-center font-black">↗</span>
          تحديث وتطوير مستمر للمحتوى
        </div>
      </div>
    </div>
  </section>

  <!-- ================= INTERACTIVE ONU & OPTICAL POWER SIMULATOR ================= -->
  <section id="simulator" class="py-16 sm:py-24 bg-gradient-to-b from-slate-100 via-white to-slate-50 dark:from-slate-900 dark:via-slate-950 dark:to-slate-900 border-b border-slate-200 dark:border-slate-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <!-- Heading -->
      <div class="text-center max-w-3xl mx-auto space-y-3 mb-14">
        <span class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full text-xs font-black bg-cyan-100 dark:bg-cyan-950 text-brand-blue dark:text-cyan-400">
          <span class="w-2 h-2 rounded-full bg-cyan-500 animate-ping"></span> أداة الفحص الحي
        </span>
        <h2 class="text-3xl sm:text-4xl font-black text-slate-900 dark:text-white">
          مختبر ومحاكي تشخيص أعطال الفايبر
        </h2>
        <p class="text-sm sm:text-base text-slate-600 dark:text-slate-400">
          اختر أي حالة عطل واقعية وشاهد تغيّر لمبات جهاز الـ ONU ومؤشرات القدرة الضوئية RX Power، مع الإجراء العملي الفوري المطلوب من موظف الكول سنتر وفني الصيانة.
        </p>
      </div>

      <!-- Simulator Interactive Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
        
        <!-- Interactive Controls (Left) -->
        <div class="lg:col-span-5 space-y-4">
          <h3 class="text-base font-extrabold text-slate-900 dark:text-white flex items-center justify-between">
            <span>اختر سيناريو العطل:</span>
            <span class="text-xs text-brand-blue dark:text-cyan-400 font-bold">تفاعل مباشر</span>
          </h3>

          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-1 gap-2.5" id="scenarioButtons">
            <button class="sim-btn active w-full p-3.5 rounded-2xl border-2 text-right transition flex items-center justify-between bg-white dark:bg-slate-800 border-brand-blue shadow-md shadow-brand-blue/15" data-scenario="normal">
              <div class="flex items-center gap-3">
                <span class="w-8 h-8 rounded-xl bg-emerald-100 dark:bg-emerald-950 text-emerald-600 flex items-center justify-center font-black">✓</span>
                <div>
                  <b class="text-sm block text-slate-900 dark:text-white font-extrabold">الوضع الطبيعي (الخدمة ممتازة)</b>
                  <small class="text-xs text-slate-500 dark:text-slate-400">كل اللمبات طبيعية والباور سليم</small>
                </div>
              </div>
              <span class="text-xs font-mono font-bold text-emerald-500">Normal</span>
            </button>

            <button class="sim-btn w-full p-3.5 rounded-2xl border-2 text-right transition flex items-center justify-between bg-white dark:bg-slate-800 border-slate-200 dark:border-slate-700 hover:border-red-400" data-scenario="cut">
              <div class="flex items-center gap-3">
                <span class="w-8 h-8 rounded-xl bg-red-100 dark:bg-red-950 text-red-600 flex items-center justify-center font-black">✕</span>
                <div>
                  <b class="text-sm block text-slate-900 dark:text-white font-extrabold">قطع بالفايبر / إشارة مفقودة (LOS)</b>
                  <small class="text-xs text-slate-500 dark:text-slate-400">انقطاع السلك الضوئي أو السبلتر</small>
                </div>
              </div>
              <span class="text-xs font-mono font-bold text-red-500">LOS Red</span>
            </button>

            <button class="sim-btn w-full p-3.5 rounded-2xl border-2 text-right transition flex items-center justify-between bg-white dark:bg-slate-800 border-slate-200 dark:border-slate-700 hover:border-amber-400" data-scenario="lowPower">
              <div class="flex items-center gap-3">
                <span class="w-8 h-8 rounded-xl bg-amber-100 dark:bg-amber-950 text-amber-600 flex items-center justify-center font-black">⚠️</span>
                <div>
                  <b class="text-sm block text-slate-900 dark:text-white font-extrabold">إشارة ضوئية ضعيفة (Low RX)</b>
                  <small class="text-xs text-slate-500 dark:text-slate-400">انحناء حاد في الفايبر أو اتساخ الكونكتر</small>
                </div>
              </div>
              <span class="text-xs font-mono font-bold text-amber-500">-29 dBm</span>
            </button>

            <button class="sim-btn w-full p-3.5 rounded-2xl border-2 text-right transition flex items-center justify-between bg-white dark:bg-slate-800 border-slate-200 dark:border-slate-700 hover:border-blue-400" data-scenario="powerOff">
              <div class="flex items-center gap-3">
                <span class="w-8 h-8 rounded-xl bg-slate-200 dark:bg-slate-700 text-slate-600 dark:text-slate-300 flex items-center justify-center font-black">🔌</span>
                <div>
                  <b class="text-sm block text-slate-900 dark:text-white font-extrabold">انقطاع الكهرباء / عطل المحوّل</b>
                  <small class="text-xs text-slate-500 dark:text-slate-400">الجهاز لا يصله تيار أو UPS فارغ</small>
                </div>
              </div>
              <span class="text-xs font-mono font-bold text-slate-500">No Power</span>
            </button>

            <button class="sim-btn w-full p-3.5 rounded-2xl border-2 text-right transition flex items-center justify-between bg-white dark:bg-slate-800 border-slate-200 dark:border-slate-700 hover:border-purple-400" data-scenario="lanCut">
              <div class="flex items-center gap-3">
                <span class="w-8 h-8 rounded-xl bg-purple-100 dark:bg-purple-950 text-purple-600 flex items-center justify-center font-black">🖧</span>
                <div>
                  <b class="text-sm block text-slate-900 dark:text-white font-extrabold">كيبل LAN مفصول أو تالف</b>
                  <small class="text-xs text-slate-500 dark:text-slate-400">النت واصل للـ ONU لكن لا يصل للراوتر</small>
                </div>
              </div>
              <span class="text-xs font-mono font-bold text-purple-500">LAN Down</span>
            </button>
          </div>

          <!-- Live Power dBm Slider Control -->
          <div class="p-5 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 space-y-3">
            <div class="flex justify-between items-center">
              <span class="text-xs font-extrabold text-slate-700 dark:text-slate-200">تحكّم يدوي بالقدرة الضوئية (dBm):</span>
              <span id="manualDbmBadge" class="font-mono text-sm font-black px-2 py-0.5 rounded bg-blue-100 dark:bg-blue-950 text-brand-blue dark:text-cyan-400">-21 dBm</span>
            </div>
            <input type="range" id="dbmSlider" min="-38" max="-5" value="-21" step="0.5" class="w-full h-2 bg-slate-200 dark:bg-slate-700 rounded-lg appearance-none cursor-pointer accent-brand-blue">
            <div class="flex justify-between text-[10px] text-slate-500 dark:text-slate-400 font-mono">
              <span>-38 (منقطع)</span>
              <span>-27 (الحد الأدنى)</span>
              <span>-19 (مثالي)</span>
              <span>-8 (قوي جداً)</span>
            </div>
          </div>
        </div>

        <!-- Simulator Device Preview & Action (Right) -->
        <div class="lg:col-span-7 space-y-6">
          
          <!-- Virtual ONU Graphic Card -->
          <div class="relative bg-gradient-to-br from-slate-900 via-slate-900 to-brand-navy rounded-3xl p-6 sm:p-8 text-white shadow-2xl border border-slate-700/80 overflow-hidden">
            
            <div class="flex flex-wrap justify-between items-center gap-3 border-b border-slate-700 pb-4 mb-6">
              <div class="flex items-center gap-3">
                <span class="w-4 h-4 rounded-full bg-cyan-500 shadow-md shadow-cyan-500/50 animate-ping"></span>
                <span class="font-mono text-sm tracking-wider font-bold text-slate-200">EARTH AL-KARAM GPON UNIT</span>
              </div>
              <div class="flex items-center gap-2">
                <span id="simStatusPill" class="px-3 py-1 rounded-full text-xs font-black bg-emerald-500/20 text-emerald-400 border border-emerald-500/40">الحالة: طبيعية وممتازة</span>
              </div>
            </div>

            <!-- Front Bezel of ONU with Glowing Lights -->
            <div class="bg-black/60 rounded-2xl p-6 border border-slate-700/80 mb-6 backdrop-blur">
              <div class="grid grid-cols-4 gap-2 sm:gap-6 text-center">
                
                <!-- Power LED -->
                <div class="space-y-2.5">
                  <span class="text-xs font-extrabold text-slate-400 font-mono">POWER</span>
                  <div class="flex justify-center">
                    <span id="simLedPower" class="w-6 h-6 rounded-full led on-green"></span>
                  </div>
                  <span id="simPowerTxt" class="text-[11px] block text-emerald-400 font-medium">مشتغلة ثابت</span>
                </div>

                <!-- PON LED -->
                <div class="space-y-2.5">
                  <span class="text-xs font-extrabold text-slate-400 font-mono">PON</span>
                  <div class="flex justify-center">
                    <span id="simLedPon" class="w-6 h-6 rounded-full led on-green"></span>
                  </div>
                  <span id="simPonTxt" class="text-[11px] block text-emerald-400 font-medium">تسجيل ناجح</span>
                </div>

                <!-- LOS LED -->
                <div class="space-y-2.5">
                  <span class="text-xs font-extrabold text-slate-400 font-mono">LOS</span>
                  <div class="flex justify-center">
                    <span id="simLedLos" class="w-6 h-6 rounded-full led off"></span>
                  </div>
                  <span id="simLosTxt" class="text-[11px] block text-slate-500 font-medium">مطفأة (سليمة)</span>
                </div>

                <!-- LAN LED -->
                <div class="space-y-2.5">
                  <span class="text-xs font-extrabold text-slate-400 font-mono">LAN</span>
                  <div class="flex justify-center">
                    <span id="simLedLan" class="w-6 h-6 rounded-full led on-blue blink-fast"></span>
                  </div>
                  <span id="simLanTxt" class="text-[11px] block text-cyan-400 font-medium">نقل بيانات</span>
                </div>

              </div>
            </div>

            <!-- Optical Power Live Bar -->
            <div class="space-y-2 bg-slate-800/60 p-4 rounded-xl border border-slate-700/60">
              <div class="flex justify-between items-center text-xs">
                <span class="text-slate-300 font-bold">مستوى القدرة الضوئية الحالي (RX Optical Power):</span>
                <span id="simRxMeterVal" class="font-mono text-base font-black text-cyan-400">-21.0 dBm</span>
              </div>
              <div class="w-full h-3 rounded-full bg-slate-700 overflow-hidden p-0.5">
                <div id="simMeterBar" class="h-full rounded-full bg-gradient-to-r from-emerald-400 to-cyan-400 transition-all duration-300" style="width: 75%;"></div>
              </div>
              <div id="simMeterVerdict" class="text-xs text-emerald-400 font-bold flex items-center gap-1.5">
                <span>✓</span> القراءة ضمن المجال القياسي المعتمد لشركة أرض الكرم (-8 dBm إلى -27 dBm).
              </div>
            </div>

          </div>

          <!-- Dynamic Diagnosis & Action Box -->
          <div class="p-6 rounded-3xl bg-white dark:bg-slate-800 border-2 border-brand-blue/30 shadow-lg space-y-4 transition-all" id="simActionCard">
            <div class="flex items-center gap-2.5">
              <span class="w-8 h-8 rounded-xl bg-brand-blue/10 dark:bg-cyan-950 text-brand-blue dark:text-cyan-400 flex items-center justify-center font-black text-lg">💡</span>
              <h4 class="text-base font-black text-slate-900 dark:text-white" id="simActionTitle">التشخيص الفوري لحالة الخدمة:</h4>
            </div>

            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-300 leading-relaxed" id="simActionDesc">
              الاتصال الضوئي مستقر تماماً. جهاز الـ ONU متصل بالسيرفر والـ OLT بنجاح، وكيبل الشبكة ينقل البيانات بصورة ممتازة للراوتر.
            </p>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 pt-2">
              <div class="p-3.5 rounded-xl bg-slate-50 dark:bg-slate-900 border border-slate-200 dark:border-slate-700">
                <b class="text-xs text-slate-900 dark:text-white block font-extrabold mb-1">إجراء موظف الكول سنتر:</b>
                <span class="text-xs text-slate-600 dark:text-slate-400" id="simCallAction">اطمئن، الخدمة سليمة. إذا اشتكى المشترك فركّز على تغطية الواي فاي وإعدادات الراوتر.</span>
              </div>
              <div class="p-3.5 rounded-xl bg-slate-50 dark:bg-slate-900 border border-slate-200 dark:border-slate-700">
                <b class="text-xs text-slate-900 dark:text-white block font-extrabold mb-1">إجراء فني الصيانة:</b>
                <span class="text-xs text-slate-600 dark:text-slate-400" id="simFieldAction">تأكد فقط من تثبيت الجهاز بمكان جيد التهوية، ولا داعي لتدخل فني بالمسار.</span>
              </div>
            </div>
          </div>

        </div>

      </div>

    </div>
  </section>

  <!-- ================= DEPARTMENTS SECTION ================= -->
  <section class="py-16 sm:py-24 bg-white dark:bg-slate-950 border-b border-slate-200 dark:border-slate-800" id="departments">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-4 mb-12">
        <div>
          <span class="text-xs font-black text-brand-blue dark:text-cyan-400 uppercase tracking-widest block mb-2">بوابتك العملية للمعرفة</span>
          <h2 class="text-3xl sm:text-4xl font-black text-slate-900 dark:text-white">الأقسام التدريبية الخمسة</h2>
          <p class="text-slate-600 dark:text-slate-400 text-sm mt-1 max-w-xl">
            كل بطاقة تحتوي على دليل عملي كامل، سيناريوهات مكالمات، خطوات فحص، وإرشادات التصعيد المعتمدة في أرض الكرم.
          </p>
        </div>
        <button id="searchFilterReset" class="text-xs font-bold text-brand-blue dark:text-cyan-400 hover:underline self-start md:self-auto">إعادة ضبط الكل ←</button>
      </div>

      <!-- Department Cards Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        
        <!-- Support Card -->
        <article class="tilt-card rounded-3xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 overflow-hidden shadow-sm hover:shadow-xl hover:border-brand-blue/50 flex flex-col justify-between">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-center">
              <span class="px-3 py-1 rounded-full text-[11px] font-black bg-blue-50 dark:bg-blue-950 text-brand-blue dark:text-cyan-300">الشبكات والتقنيات</span>
              <span class="text-sm font-black font-mono text-slate-400">01</span>
            </div>
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-brand-blue to-cyan-400 text-white flex items-center justify-center text-2xl font-black shadow-md shadow-brand-blue/20">
              🛠️
            </div>
            <h3 class="text-xl font-black text-slate-900 dark:text-white">الدعم الفني والتشخيص</h3>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed">
              أساسيات الشبكات الضوئية، تشخيص أعطال ONU، قراءة مؤشرات RX Power، فحص التوصيل السلكي، وفصل مشاكل الشبكة عن مشاكل الراوتر.
            </p>
          </div>
          <div class="p-6 pt-0">
            <button class="w-full py-3 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-brand-blue hover:text-white dark:hover:bg-brand-blue text-brand-blue dark:text-cyan-400 text-xs font-extrabold transition flex items-center justify-center gap-2 group" data-open="support">
              <span>افتح الدليل الكامل للدعم الفني</span>
              <span class="group-hover:translate-x-1 transition-transform">←</span>
            </button>
          </div>
        </article>

        <!-- Service Card -->
        <article class="tilt-card rounded-3xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 overflow-hidden shadow-sm hover:shadow-xl hover:border-purple-500/50 flex flex-col justify-between">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-center">
              <span class="px-3 py-1 rounded-full text-[11px] font-black bg-purple-50 dark:bg-purple-950 text-purple-600 dark:text-purple-300">التواصل وتجربة المشترك</span>
              <span class="text-sm font-black font-mono text-slate-400">02</span>
            </div>
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-purple-600 to-indigo-400 text-white flex items-center justify-center text-2xl font-black shadow-md shadow-purple-500/20">
              🎧
            </div>
            <h3 class="text-xl font-black text-slate-900 dark:text-white">خدمة العملاء والكول سنتر</h3>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed">
              إدارة المكالمة باحتراف، نصوص الرد باللهجة العراقية، الأسئلة التشخيصية الدقيقة، احتواء غضب المشترك، وتوثيق التذاكر بدون وعود وهمية.
            </p>
          </div>
          <div class="p-6 pt-0">
            <button class="w-full py-3 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-purple-600 hover:text-white dark:hover:bg-purple-600 text-purple-600 dark:text-purple-400 text-xs font-extrabold transition flex items-center justify-center gap-2 group" data-open="service">
              <span>افتح سيناريوهات المكالمات</span>
              <span class="group-hover:translate-x-1 transition-transform">←</span>
            </button>
          </div>
        </article>

        <!-- Sales Card -->
        <article class="tilt-card rounded-3xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 overflow-hidden shadow-sm hover:shadow-xl hover:border-emerald-500/50 flex flex-col justify-between">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-center">
              <span class="px-3 py-1 rounded-full text-[11px] font-black bg-emerald-500/10 text-emerald-600 dark:text-emerald-400">العروض والنمو</span>
              <span class="text-sm font-black font-mono text-slate-400">03</span>
            </div>
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-emerald-500 to-teal-400 text-white flex items-center justify-center text-2xl font-black shadow-md shadow-emerald-500/20">
              📈
            </div>
            <h3 class="text-xl font-black text-slate-900 dark:text-white">المبيعات والعروض</h3>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed">
              فهم احتياج المشترك الحقيقي، شرح باقة الـ 35,000 د.ع والباقات المعتمدة، معالجة الاعتراضات بثقة، وتقديم العروض الرسمية دون مبالغات.
            </p>
          </div>
          <div class="p-6 pt-0">
            <button class="w-full py-3 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-emerald-600 hover:text-white dark:hover:bg-emerald-600 text-emerald-600 dark:text-emerald-400 text-xs font-extrabold transition flex items-center justify-center gap-2 group" data-open="sales">
              <span>افتح دليل المبيعات والعروض</span>
              <span class="group-hover:translate-x-1 transition-transform">←</span>
            </button>
          </div>
        </article>

        <!-- Training Card -->
        <article class="tilt-card rounded-3xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 overflow-hidden shadow-sm hover:shadow-xl hover:border-amber-500/50 flex flex-col justify-between">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-center">
              <span class="px-3 py-1 rounded-full text-[11px] font-black bg-amber-500/10 text-amber-600 dark:text-amber-400">التطوير المهني</span>
              <span class="text-sm font-black font-mono text-slate-400">04</span>
            </div>
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-amber-500 to-orange-400 text-white flex items-center justify-center text-2xl font-black shadow-md shadow-amber-500/20">
              🎓
            </div>
            <h3 class="text-xl font-black text-slate-900 dark:text-white">التدريب ومسار الموظف</h3>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed">
              خطة تأهيل الموظف الجديد خلال أول أسبوعين، مرافقة الزملاء، محاكاة السيناريوهات، واختبارات الجاهزية قبل بدء العمل المباشر.
            </p>
          </div>
          <div class="p-6 pt-0">
            <button class="w-full py-3 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-amber-600 hover:text-white dark:hover:bg-amber-600 text-amber-600 dark:text-amber-400 text-xs font-extrabold transition flex items-center justify-center gap-2 group" data-open="training">
              <span>افتح مسار تدريب الموظف</span>
              <span class="group-hover:translate-x-1 transition-transform">←</span>
            </button>
          </div>
        </article>

        <!-- Field Maintenance Card -->
        <article class="tilt-card rounded-3xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 overflow-hidden shadow-sm hover:shadow-xl hover:border-blue-500/50 flex flex-col justify-between md:col-span-2 lg:col-span-1">
          <div class="p-6 space-y-4">
            <div class="flex justify-between items-center">
              <span class="px-3 py-1 rounded-full text-[11px] font-black bg-cyan-50 dark:bg-cyan-950 text-brand-blue dark:text-cyan-400">الفحص الميداني</span>
              <span class="text-sm font-black font-mono text-slate-400">05</span>
            </div>
            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-blue-600 to-teal-500 text-white flex items-center justify-center text-2xl font-black shadow-md shadow-blue-500/20">
              ⚡
            </div>
            <h3 class="text-xl font-black text-slate-900 dark:text-white">الصيانة الميدانية والفحص</h3>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 leading-relaxed">
              خطوات الفحص بموقع المشترك: قياس الباور بالـ Optical Power Meter، فحص التوصيلات، التحقق من UPS ومغذيات الطاقة، وتشخيص عوائق الواي فاي.
            </p>
          </div>
          <div class="p-6 pt-0">
            <button class="w-full py-3 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-blue-600 hover:text-white dark:hover:bg-blue-600 text-brand-blue dark:text-cyan-400 text-xs font-extrabold transition flex items-center justify-center gap-2 group" data-open="maintenance">
              <span>افتح دليل الصيانة الميدانية</span>
              <span class="group-hover:translate-x-1 transition-transform">←</span>
            </button>
          </div>
        </article>

      </div>

    </div>
  </section>

  <!-- ================= FIBER DEVICES SECTION ================= -->
  <section class="py-16 sm:py-24 bg-slate-50 dark:bg-slate-900/60 border-b border-slate-200 dark:border-slate-800" id="devices">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-2xl mx-auto mb-12 space-y-2">
        <span class="text-xs font-black text-brand-blue dark:text-cyan-400 uppercase tracking-widest">مختبر الأجهزة الميدانية</span>
        <h2 class="text-3xl sm:text-4xl font-black text-slate-900 dark:text-white">أجهزة الفايبر وتوصيلاتها</h2>
        <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400">
          افهم الجهاز قبل شروعه بالعطل؛ كل عنصر له دور محدد ومؤشرات دقيقة يجب فحصها وتوثيقها.
        </p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        
        <!-- ONU Card -->
        <div class="tilt-card bg-white dark:bg-slate-800 rounded-3xl p-6 border border-slate-200 dark:border-slate-700 space-y-4 hover:shadow-xl transition">
          <div class="h-36 rounded-2xl bg-gradient-to-br from-blue-50 to-cyan-50 dark:from-slate-900 dark:to-slate-950 flex items-center justify-center relative overflow-hidden group">
            <span class="text-5xl group-hover:scale-110 transition duration-300">📟</span>
            <span class="absolute bottom-2 left-2 text-[10px] font-mono px-2 py-0.5 rounded bg-white/80 dark:bg-slate-800/80 text-brand-blue font-bold">ONU / ONT</span>
          </div>
          <h3 class="text-lg font-black text-slate-900 dark:text-white">جهاز الـ ONU ومؤشراته</h3>
          <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed">
            محول الإشارة الضوئية إلى كهربائية. الفرق بين دلالات لمبة PON ولمبة LOS بالغة الأهمية لتحديد مكان العطل.
          </p>
          <button class="text-xs font-black text-brand-blue dark:text-cyan-400 hover:underline flex items-center gap-1" data-open="onu">
            <span>تفاصيل لمبات ONU</span> <span>←</span>
          </button>
        </div>

        <!-- Router Card -->
        <div class="tilt-card bg-white dark:bg-slate-800 rounded-3xl p-6 border border-slate-200 dark:border-slate-700 space-y-4 hover:shadow-xl transition">
          <div class="h-36 rounded-2xl bg-gradient-to-br from-cyan-50 to-teal-50 dark:from-slate-900 dark:to-slate-950 flex items-center justify-center relative overflow-hidden group">
            <span class="text-5xl group-hover:scale-110 transition duration-300">📡</span>
            <span class="absolute bottom-2 left-2 text-[10px] font-mono px-2 py-0.5 rounded bg-white/80 dark:bg-slate-800/80 text-teal-600 font-bold">Dual Band</span>
          </div>
          <h3 class="text-lg font-black text-slate-900 dark:text-white">الراوتر وبث الواي فاي</h3>
          <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed">
            توزيع الإشارة لاسلكياً. كيفية فحص التغطية والفرق بين تردد 2.4GHz للأماكن البعيدة و5GHz للسرعات العالية.
          </p>
          <button class="text-xs font-black text-brand-blue dark:text-cyan-400 hover:underline flex items-center gap-1" data-open="router">
            <span>تشخيص الواي فاي</span> <span>←</span>
          </button>
        </div>

        <!-- LAN Cable Card -->
        <div class="tilt-card bg-white dark:bg-slate-800 rounded-3xl p-6 border border-slate-200 dark:border-slate-700 space-y-4 hover:shadow-xl transition">
          <div class="h-36 rounded-2xl bg-gradient-to-br from-amber-50 to-orange-50 dark:from-slate-900 dark:to-slate-950 flex items-center justify-center relative overflow-hidden group">
            <span class="text-5xl group-hover:scale-110 transition duration-300">🔌</span>
            <span class="absolute bottom-2 left-2 text-[10px] font-mono px-2 py-0.5 rounded bg-white/80 dark:bg-slate-800/80 text-amber-600 font-bold">Cat5e / Cat6</span>
          </div>
          <h3 class="text-lg font-black text-slate-900 dark:text-white">كيبل الـ LAN والتوصيلات</h3>
          <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed">
            الرابط السلكي بين ONU والراوتر. فحص رؤوس RJ45 والتأكد من عدم كسر الكلبسة أو هبوط السرعة إلى 100Mbps.
          </p>
          <button class="text-xs font-black text-brand-blue dark:text-cyan-400 hover:underline flex items-center gap-1" data-open="lan">
            <span>فحص كيبل الشبكة</span> <span>←</span>
          </button>
        </div>

        <!-- UPS Card -->
        <div class="tilt-card bg-white dark:bg-slate-800 rounded-3xl p-6 border border-slate-200 dark:border-slate-700 space-y-4 hover:shadow-xl transition">
          <div class="h-36 rounded-2xl bg-gradient-to-br from-purple-50 to-pink-50 dark:from-slate-900 dark:to-slate-950 flex items-center justify-center relative overflow-hidden group">
            <span class="text-5xl group-hover:scale-110 transition duration-300">🔋</span>
            <span class="absolute bottom-2 left-2 text-[10px] font-mono px-2 py-0.5 rounded bg-white/80 dark:bg-slate-800/80 text-purple-600 font-bold">Power Backup</span>
          </div>
          <h3 class="text-lg font-black text-slate-900 dark:text-white">جهاز الـ UPS والطاقة</h3>
          <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed">
            تأمين استمرارية الخدمة أثناء التحويل بين الشبكة والمولد، والتأكد من جهد وتيار المحولات المعتمدة.
          </p>
          <button class="text-xs font-black text-brand-blue dark:text-cyan-400 hover:underline flex items-center gap-1" data-open="ups">
            <span>فحص التغذية والـ UPS</span> <span>←</span>
          </button>
        </div>

      </div>

    </div>
  </section>

  <!-- ================= ROUTERS DIRECTORY & PASSWORD CHANGE GUIDE ================= -->
  <section class="py-16 sm:py-24 bg-white dark:bg-slate-950 border-b border-slate-200 dark:border-slate-800" id="routers">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-4 mb-12">
        <div>
          <span class="text-xs font-black text-brand-blue dark:text-cyan-400 uppercase tracking-widest block mb-1">دليل المشترك والفني</span>
          <h2 class="text-3xl sm:text-4xl font-black text-slate-900 dark:text-white">أنواع الراوترات وعناوين الدخول (IP)</h2>
          <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400 mt-1 max-w-2xl">
            اختر نوع الراوتر لعرض خطوات تسجيل الدخول، عناوين IP الافتراضية، وطريقة تغيير اسم الشبكة (SSID) ورمز المرور بأمان.
          </p>
        </div>
        <div class="text-xs px-3 py-1.5 rounded-xl bg-slate-100 dark:bg-slate-800 font-bold text-slate-600 dark:text-slate-300">
          🔒 تحذير: لا تقم بعمل Reset إلا بعد توفر إعدادات الخدمة
        </div>
      </div>

      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4">
        
        <!-- TP-Link -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-brand-blue/50 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-cyan-100 dark:bg-cyan-950 text-brand-blue dark:text-cyan-400 flex items-center justify-center text-2xl font-black mb-3">📡</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">TP-Link</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.0.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-brand-blue dark:text-cyan-400 border border-slate-200 dark:border-slate-700 group-hover:bg-brand-blue group-hover:text-white transition" data-open="router-tplink">طريقة التغيير ←</button>
        </div>

        <!-- Huawei -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-red-400 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-red-100 dark:bg-red-950 text-red-500 flex items-center justify-center text-2xl font-black mb-3">📶</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">Huawei</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.3.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-red-500 border border-slate-200 dark:border-slate-700 group-hover:bg-red-500 group-hover:text-white transition" data-open="router-huawei">طريقة التغيير ←</button>
        </div>

        <!-- ZTE -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-blue-400 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-blue-100 dark:bg-blue-950 text-blue-500 flex items-center justify-center text-2xl font-black mb-3">🌐</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">ZTE</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.1.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-blue-500 border border-slate-200 dark:border-slate-700 group-hover:bg-blue-500 group-hover:text-white transition" data-open="router-zte">طريقة التغيير ←</button>
        </div>

        <!-- Tenda -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-orange-400 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-orange-100 dark:bg-orange-950 text-orange-500 flex items-center justify-center text-2xl font-black mb-3">📶</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">Tenda</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.0.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-orange-500 border border-slate-200 dark:border-slate-700 group-hover:bg-orange-500 group-hover:text-white transition" data-open="router-tenda">طريقة التغيير ←</button>
        </div>

        <!-- D-Link -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-teal-400 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-teal-100 dark:bg-teal-950 text-teal-600 flex items-center justify-center text-2xl font-black mb-3">🛜</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">D-Link</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.0.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-teal-600 border border-slate-200 dark:border-slate-700 group-hover:bg-teal-600 group-hover:text-white transition" data-open="router-dlink">طريقة التغيير ←</button>
        </div>

        <!-- Xiaomi -->
        <div class="p-4 rounded-2xl border border-slate-200 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 text-center hover:border-amber-400 hover:-translate-y-1 transition group">
          <div class="w-12 h-12 mx-auto rounded-xl bg-amber-100 dark:bg-amber-950 text-amber-500 flex items-center justify-center text-2xl font-black mb-3">📡</div>
          <b class="text-sm block text-slate-900 dark:text-white font-extrabold mb-1">Xiaomi</b>
          <span class="text-[11px] font-mono text-slate-500 dark:text-slate-400 block mb-3">192.168.31.1</span>
          <button class="w-full py-1.5 rounded-lg bg-white dark:bg-slate-800 text-xs font-bold text-amber-500 border border-slate-200 dark:border-slate-700 group-hover:bg-amber-500 group-hover:text-white transition" data-open="router-xiaomi">طريقة التغيير ←</button>
        </div>

      </div>

      <!-- Quick Steps Banner -->
      <div class="mt-8 p-6 rounded-3xl bg-slate-50 dark:bg-slate-900 border border-slate-200 dark:border-slate-800">
        <h4 class="text-sm font-black text-slate-900 dark:text-white mb-3">القواعد الست لتغيير باسورد الواي فاي بأمان:</h4>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-3 text-xs text-slate-600 dark:text-slate-300">
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">1</span>
            <span>الاتصال بالراوتر سلكياً أو عبر الواي فاي قبل فتح المتصفح.</span>
          </div>
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">2</span>
            <span>كتابة الـ IP الصحيح بشريط العنوان وليس بمحرك بحث Google.</span>
          </div>
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">3</span>
            <span>استخدام بيانات الدخول المطبوعة أسفل الراوتر أو المجهزة من المسؤول.</span>
          </div>
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">4</span>
            <span>تعديل SSID لاسم الشبكة و WPA2/WPA3 Pre-Shared Key لكلمة السر.</span>
          </div>
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">5</span>
            <span>تجنب تغيير أي إعداد يخص WAN / VLAN حتى لا تنقطع الخدمة.</span>
          </div>
          <div class="flex items-start gap-2">
            <span class="w-5 h-5 rounded-full bg-blue-100 dark:bg-blue-950 text-brand-blue font-bold flex items-center justify-center flex-shrink-0">6</span>
            <span>الضغط على Save / Apply وإعادة الاتصال بالرمز الجديد فوراً.</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- ================= OFFERS & SPEED TEST SIMULATOR ================= -->
  <section class="py-16 sm:py-24 bg-gradient-to-b from-slate-50 to-white dark:from-slate-900 dark:to-slate-950 border-b border-slate-200 dark:border-slate-800" id="offers">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-2xl mx-auto mb-12 space-y-2">
        <span class="text-xs font-black text-brand-blue dark:text-cyan-400 uppercase tracking-widest">باقات وعروض أرض الكرم</span>
        <h2 class="text-3xl sm:text-4xl font-black text-slate-900 dark:text-white">باقات المشتركين وفحص السرعة</h2>
        <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-400">
          التسعير الرسمي المعتمد للباقة الأساسية ومحاكي قياس سرعة فايبر أرض الكرم التفاعلي.
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
        
        <!-- Interactive Speed Test Mockup (6 cols) -->
        <div class="lg:col-span-6 p-6 sm:p-8 rounded-3xl bg-slate-900 text-white border border-slate-800 shadow-2xl space-y-6">
          <div class="flex justify-between items-center border-b border-slate-800 pb-4">
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full bg-teal-400 animate-ping"></span>
              <span class="text-xs font-bold font-mono tracking-wider text-slate-300">EARTH AL-KARAM SPEED SIMULATOR</span>
            </div>
            <span class="text-[10px] font-mono px-2 py-0.5 rounded bg-slate-800 text-teal-400">Baghdad Server</span>
          </div>

          <!-- Speed Meter Display -->
          <div class="text-center py-6 space-y-2">
            <div class="text-5xl sm:text-6xl font-black text-transparent bg-gradient-to-r from-cyan-400 to-teal-400 bg-clip-text font-mono" id="speedNumDisplay">
              0.0
            </div>
            <span class="text-xs text-slate-400 font-bold block uppercase tracking-widest">Mbps Download Speed</span>
          </div>

          <!-- Progress Animation Bar -->
          <div class="w-full bg-slate-800 h-2.5 rounded-full overflow-hidden">
            <div id="speedMeterBar" class="h-full bg-gradient-to-r from-brand-blue via-cyan-400 to-teal-400 transition-all duration-200" style="width: 0%;"></div>
          </div>

          <div class="grid grid-cols-3 gap-2 text-center text-xs pt-2 font-mono">
            <div class="p-2.5 rounded-xl bg-slate-800/60 border border-slate-700/60">
              <span class="text-[10px] text-slate-400 block font-sans">Ping</span>
              <b class="text-cyan-400 font-bold" id="pingDisplay">-- ms</b>
            </div>
            <div class="p-2.5 rounded-xl bg-slate-800/60 border border-slate-700/60">
              <span class="text-[10px] text-slate-400 block font-sans">Jitter</span>
              <b class="text-teal-400 font-bold" id="jitterDisplay">-- ms</b>
            </div>
            <div class="p-2.5 rounded-xl bg-slate-800/60 border border-slate-700/60">
              <span class="text-[10px] text-slate-400 block font-sans">Loss</span>
              <b class="text-emerald-400 font-bold">0.0%</b>
            </div>
          </div>

          <button id="startSpeedTestBtn" class="w-full py-3.5 rounded-xl font-black text-sm bg-gradient-to-r from-brand-blue to-teal-500 hover:opacity-95 transition shadow-lg shadow-teal-500/20 active:scale-98">
            🚀 ابدأ محاكاة فحص سرعة الفايبر
          </button>
        </div>

        <!-- Official Offer Cards (6 cols) -->
        <div class="lg:col-span-6 space-y-4">
          
          <!-- Featured Basic Plan -->
          <div class="p-6 rounded-3xl bg-gradient-to-br from-blue-50 to-cyan-50 dark:from-slate-800 dark:to-slate-850 border-2 border-brand-blue shadow-lg space-y-3">
            <div class="flex justify-between items-start">
              <div>
                <span class="px-3 py-1 rounded-full text-[10px] font-black bg-brand-blue text-white">الباقة المعتمدة الأساسية</span>
                <h3 class="text-2xl font-black text-slate-900 dark:text-white mt-2">Basic — الباقة الأساسية</h3>
              </div>
              <div class="text-left font-mono" dir="ltr">
                <span class="text-3xl font-black text-brand-blue dark:text-cyan-400">35,000</span>
                <span class="text-xs text-slate-500 dark:text-slate-400 font-sans block">د.ع / شهرياً</span>
              </div>
            </div>
            <p class="text-xs sm:text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
              مدة الاشتراك شهر تقويمي كامل. سرعة مستقرة ومثالية للتصفح، البث عالي الدقة (HD/4K)، والألعاب الإلكترونية مع بينغ منخفض عبر شبكة الفايبر المباشرة.
            </p>
            <div class="flex items-center gap-2 text-xs text-slate-500 dark:text-slate-400 pt-1">
              <span>✓ دعم فني 24/7</span> • <span>✓ توصيل ضوئي مباشر</span> • <span>✓ إمكانية الترقية فوراً</span>
            </div>
          </div>

          <!-- Renewal Card -->
          <div class="p-5 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 flex items-center justify-between">
            <div class="space-y-1">
              <b class="text-sm text-slate-900 dark:text-white block font-extrabold">عروض التجديد وإعادة التفعيل</b>
              <p class="text-xs text-slate-500 dark:text-slate-400">التأكد من رصيد الحساب وتاريخ الانتهاء وإشعار المشترك قبل موعد التجديد بوقت كافٍ.</p>
            </div>
            <span class="text-2xl">↻</span>
          </div>

          <!-- Promo Note -->
          <div class="p-4 rounded-xl bg-amber-50 dark:bg-amber-950/40 border border-amber-200 dark:border-amber-800/60 text-xs text-amber-800 dark:text-amber-300 leading-relaxed">
            <b>ملاحظة رسمية:</b> الأسعار المذكورة هي المعتمدة رسمياً ضمن بيانات تدريب شركة أرض الكرم. بقية الباقات والعروض الخاصة تُحدّث دورياً من قبل إدارة المبيعات.
          </div>

        </div>

      </div>

    </div>
  </section>

  <!-- ================= ABOUT & AUTHOR BANNER ================= -->
  <section class="py-16 bg-slate-100 dark:bg-slate-900/40" id="about">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-6">
      
      <div class="w-16 h-16 mx-auto rounded-3xl bg-gradient-to-tr from-brand-blue to-teal-400 p-1 shadow-xl">
        <div class="w-full h-full bg-white dark:bg-slate-900 rounded-[20px] flex items-center justify-center text-3xl">
          📚
        </div>
      </div>

      <h2 class="text-2xl sm:text-3xl font-black text-slate-900 dark:text-white">
        أكاديمية أرض الكرم — المعرفة تكبر بالمشاركة
      </h2>

      <p class="text-sm text-slate-600 dark:text-slate-400 max-w-2xl mx-auto leading-relaxed">
        تم إعداد هذه الموسوعة التدريبية وتطويرها لتكون مرجعاً موحداً وعملياً وسريعاً لكل فني وموظف كول سنتر ومبيعات بشركة أرض الكرم، لتسهيل خدمة المشترك العراقي بأعلى دقة واحترافية.
      </p>

      <div class="inline-flex items-center gap-3 px-5 py-2.5 rounded-2xl bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-sm">
        <span class="text-xs text-slate-500 dark:text-slate-400">إعداد وتطوير المنصة والمحتوى:</span>
        <b class="text-sm font-black text-brand-blue dark:text-cyan-400">علي وجدي</b>
      </div>

    </div>
  </section>

</main>

<!-- ================= FOOTER ================= -->
<footer class="border-t border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-950 py-8 text-xs text-slate-500 dark:text-slate-400">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4">
    <div class="flex items-center gap-3">
      <span class="font-extrabold text-slate-700 dark:text-slate-200">شركة أرض الكرم للاتصالات وتكنولوجيا المعلومات</span>
      <span>•</span>
      <span>إعداد المحتوى: <b>علي وجدي</b></span>
    </div>
    <div class="flex items-center gap-4">
      <span>© <span id="currentYear"></span> جميع الحقوق محفوظة</span>
      <a href="#home" class="font-bold text-brand-blue dark:text-cyan-400 hover:underline">العودة للأعلى ↑</a>
    </div>
  </div>
</footer>

<!-- ================= SEARCH MODAL (CTRL+K) ================= -->
<div id="searchModal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center p-4">
  <div class="bg-white dark:bg-slate-900 rounded-3xl max-w-lg w-full p-6 shadow-2xl border border-slate-200 dark:border-slate-800 space-y-4">
    <div class="flex justify-between items-center border-b border-slate-100 dark:border-slate-800 pb-3">
      <h3 class="font-black text-sm text-slate-900 dark:text-white flex items-center gap-2">
        <span>🔍</span> بحث سريع في أدلة أرض الكرم
      </h3>
      <button id="closeSearchModal" class="w-8 h-8 rounded-lg bg-slate-100 dark:bg-slate-800 text-slate-500 hover:bg-slate-200 text-base font-bold">×</button>
    </div>
    <input type="text" id="searchInput" placeholder="اكتب للبحث (مثل: LOS, راوتر, TP-Link, باور, كول سنتر)..." class="w-full px-4 py-3 rounded-xl bg-slate-50 dark:bg-slate-800 border border-slate-200 dark:border-slate-700 text-sm text-slate-800 dark:text-slate-100 focus:outline-none focus:ring-2 focus:ring-brand-blue font-medium">
    <div id="searchResults" class="max-h-60 overflow-y-auto space-y-2 text-xs">
      <!-- Search hits will appear here -->
    </div>
    <p class="text-[11px] text-slate-400 text-center">اضغط Esc أو × للإغلاق</p>
  </div>
</div>

<!-- ================= RICH LESSON MODAL ================= -->
<div id="lessonModal" class="fixed inset-0 z-50 bg-slate-950/70 backdrop-blur-md hidden items-center justify-center p-4 sm:p-6" role="dialog" aria-modal="true">
  <div class="relative bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-800 rounded-3xl max-w-2xl w-full max-h-[88vh] flex flex-col shadow-2xl overflow-hidden animate-pop">
    
    <!-- Modal Header -->
    <div class="p-6 border-b border-slate-100 dark:border-slate-800 flex items-start justify-between bg-slate-50/70 dark:bg-slate-900/70 backdrop-blur">
      <div class="space-y-1">
        <span id="modalKicker" class="text-xs font-black text-brand-blue dark:text-cyan-400 px-2.5 py-0.5 rounded-full bg-blue-50 dark:bg-blue-950">دليل القسم</span>
        <h2 id="modalTitle" class="text-xl sm:text-2xl font-black text-slate-900 dark:text-white">عنوان الدليل</h2>
      </div>
      <button id="modalClose" class="w-9 h-9 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-slate-200 dark:hover:bg-slate-700 text-slate-600 dark:text-slate-300 font-black text-lg flex items-center justify-center transition" aria-label="إغلاق">×</button>
    </div>

    <!-- Modal Body -->
    <div class="p-6 overflow-y-auto space-y-4">
      <p id="modalIntro" class="text-xs sm:text-sm text-slate-600 dark:text-slate-300 leading-relaxed"></p>
      
      <div id="modalTopics" class="grid grid-cols-1 sm:grid-cols-2 gap-3 pt-2">
        <!-- Injected Topics -->
      </div>

      <div class="p-3.5 rounded-xl bg-amber-50 dark:bg-amber-950/40 border border-amber-200 dark:border-amber-800 text-[11px] text-amber-800 dark:text-amber-300 leading-relaxed">
        <b>تنبيه فني:</b> راجع دائماً تعليمات الشركة وإجراءات الفحص المعتمدة قبل تطبيق أي إجراء في كابينة الفايبر أو جهاز المشترك.
      </div>
    </div>

    <!-- Modal Footer -->
    <div class="p-4 border-t border-slate-100 dark:border-slate-800 bg-slate-50 dark:bg-slate-900 flex justify-between items-center text-xs text-slate-500">
      <span>أكاديمية أرض الكرم • تدريب مستمر</span>
      <button id="modalCloseBtn" class="px-4 py-2 rounded-xl bg-brand-blue text-white font-bold hover:bg-blue-600 transition">إغلاق الدليل</button>
    </div>

  </div>
</div>

<!-- ================= JAVASCRIPT LOGIC & SIMULATOR ================= -->
<script>
/* 1. Canvas Interactive Glowing Fiber Mesh Animation */
(function initFiberCanvas() {
  const canvas = document.getElementById('fiberCanvas');
  if (!canvas) return;
  const ctx = canvas.getContext('2d');
  let width, height;
  let particles = [];
  let mouse = { x: null, y: null, maxDist: 150 };

  function resize() {
    width = canvas.width = canvas.parentElement.offsetWidth;
    height = canvas.height = canvas.parentElement.offsetHeight;
  }
  window.addEventListener('resize', resize);
  resize();

  window.addEventListener('mousemove', e => {
    const rect = canvas.getBoundingClientRect();
    mouse.x = e.clientX - rect.left;
    mouse.y = e.clientY - rect.top;
  });
  window.addEventListener('mouseleave', () => { mouse.x = null; mouse.y = null; });

  class FiberParticle {
    constructor() {
      this.reset();
    }
    reset() {
      this.x = Math.random() * width;
      this.y = Math.random() * height;
      this.vx = (Math.random() - 0.5) * 0.9;
      this.vy = (Math.random() - 0.5) * 0.9;
      this.radius = Math.random() * 2 + 1;
      this.baseColor = Math.random() > 0.5 ? '#00c2cb' : '#0785ce';
    }
    update() {
      this.x += this.vx;
      this.y += this.vy;
      if (this.x < 0 || this.x > width) this.vx *= -1;
      if (this.y < 0 || this.y > height) this.vy *= -1;

      // Mouse interactive push/pull
      if (mouse.x !== null) {
        let dx = mouse.x - this.x;
        let dy = mouse.y - this.y;
        let dist = Math.sqrt(dx * dx + dy * dy);
        if (dist < mouse.maxDist) {
          this.x -= (dx / dist) * 1.5;
          this.y -= (dy / dist) * 1.5;
        }
      }
    }
    draw() {
      ctx.beginPath();
      ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
      ctx.fillStyle = this.baseColor;
      ctx.shadowBlur = 8;
      ctx.shadowColor = this.baseColor;
      ctx.fill();
      ctx.shadowBlur = 0;
    }
  }

  const count = Math.min(Math.floor((window.innerWidth * 700) / 16000), 55);
  for (let i = 0; i < count; i++) {
    particles.push(new FiberParticle());
  }

  function animate() {
    ctx.clearRect(0, 0, width, height);

    // Draw connecting fiber lines
    for (let i = 0; i < particles.length; i++) {
      for (let j = i + 1; j < particles.length; j++) {
        let dx = particles[i].x - particles[j].x;
        let dy = particles[i].y - particles[j].y;
        let dist = Math.sqrt(dx * dx + dy * dy);
        if (dist < 110) {
          ctx.beginPath();
          ctx.moveTo(particles[i].x, particles[i].y);
          ctx.lineTo(particles[j].x, particles[j].y);
          ctx.strokeStyle = `rgba(7, 133, 206, ${0.28 * (1 - dist / 110)})`;
          ctx.lineWidth = 1;
          ctx.stroke();
        }
      }
    }

    particles.forEach(p => {
      p.update();
      p.draw();
    });

    requestAnimationFrame(animate);
  }
  animate();
})();

/* 2. Reading Scroll Progress Bar */
window.addEventListener('scroll', () => {
  const winScroll = document.documentElement.scrollTop || document.body.scrollTop;
  const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  const scrolled = (winScroll / height) * 100;
  const bar = document.getElementById('scrollProgress');
  if (bar) bar.style.width = scrolled + '%';
});

/* 3. Dark / Light Mode Switcher with Persistence */
const themeToggle = document.getElementById('themeToggle');
const themeIcon = document.getElementById('themeIcon');
function applyTheme(isDark) {
  if (isDark) {
    document.documentElement.classList.add('dark');
    if (themeIcon) themeIcon.textContent = '☀️';
    localStorage.setItem('ak_theme', 'dark');
  } else {
    document.documentElement.classList.remove('dark');
    if (themeIcon) themeIcon.textContent = '🌙';
    localStorage.setItem('ak_theme', 'light');
  }
}
const savedTheme = localStorage.getItem('ak_theme') || (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
applyTheme(savedTheme === 'dark');
themeToggle?.addEventListener('click', () => {
  const isDark = document.documentElement.classList.contains('dark');
  applyTheme(!isDark);
});

/* 4. Rich Training Lessons Database (Earth Al-Karam) */
const lessonData = {
  support: {
    kicker: 'الدعم الفني والتشخيص',
    title: 'دليل تشخيص العطل عن بُعد للمشترك',
    intro: 'اجمع معلومات دقيقة وواضحة من المشترك قبل توجيه الحالة للميدان. استمع للأعراض ولا تغيّر إعدادات حساسة دون فحص منهجي.',
    topics: [
      ['تحديد نطاق المشكلة بدقة', 'اسأل المشترك: هل يفصل الاتصال بكل الأجهزة أم هاتف واحد فقط؟ هل يفصل النت بالكامل أم أن الواي فاي يختفي بغرف محددة؟'],
      ['مراجعة حالة الشبكة العامة', 'تحقق من نظام إدارة الشبكة (NMS) الداخلي لمعرفة إذا كان هناك قطع عام على مسار الـ OLT أو السبلتر بالحي.'],
      ['فحص لمبات جهاز ONU', 'تأكد من لمبة POWER (طاقة) وPON (تسجيل ضوئي) وLOS (إشارة حمراء منقطعة) وLAN (رابط الراوتر).'],
      ['التفريق بين الفايبر والواي فاي', 'إذا كان الاتصال السلكي من الراوتر باللابتوب يعمل بصورة ممتازة بينما الواي فاي بطيء، فالعطل محلي بالتغطية والتردد وليس بالفايبر.'],
      ['قراءة وفحص الـ RX Power', 'سجّل قراءة الاستقبال بوحدة dBm وقارنها بمعيار الشركة (-8 dBm إلى -27 dBm). إذا تجاوزت -28 dBm صعّد للفني لإصلاح العقدة.'],
      ['تدوين بطاقة البلاغ الاحترافية', 'دوّن: رقم المشترك، اللمبات، قراءة الباور، طراز الراوتر، نتيجة الفحص السلكي، والوقت بدقة دون طلب كلمات المرور الخاصة.']
    ]
  },
  service: {
    kicker: 'خدمة العملاء والكول سنتر',
    title: 'دليل إدارة المكالمة باحترافية وهدوء',
    intro: 'نصوص وسيناريوهات عراقية مهذبة للتعامل مع المشتركين واستيعاب انزعاجهم والوصول للحل دون وعود مضللة.',
    topics: [
      ['التحية الافتتاحية المعتمدة', '«السلام عليكم، وياك [اسمك] من مركز خدمة عملاء أرض الكرم، تفضل أستاذي شلون نكدر نساعدك اليوم؟»'],
      ['استيعاب انفعال المشترك', '«حقك علينا وأتفهّم انزعاجك جداً.. تدلل هسه أفحص خطك وياك خطوة بخطوة وما ننهي المكالمة إلا والأمر واضح وموثّق.»'],
      ['السؤال التشخيصي للـ ONU', '«أستاذي بلا زحمة عليك، ممكن تنظر لجهاز الفايبر الصغير (الـ ONU) وتكلي يا لمبة مشتغلة؟ أكو لمبة حمرة باسم LOS تومض؟»'],
      ['فحص الراوتر والتوصيلات', '«إذا تقترب من الراوتر، الإشارة تقوى عندك؟ والكيبل الواصل بين الجهازين مكبوس بشكل محكم وبيه ضوء صغير؟»'],
      ['إنهاء المكالمة وتوثيق التذكرة', '«سجلت لحضرتك بلاغ صيانة برقم [1234]، والفريق الميداني راح يتابع مسار الإشارة ويباركلك بالحل بأسرع وقت. شكراً لاتصالك بأرض الكرم.»'],
      ['المحظورات الخمسة في الكول سنتر', 'ممنوع إلقاء اللوم على المشترك، ممنوع إعطاء وقت إصلاح غير مؤكد، وممنوع طلب باسورد الراوتر أو الرموز السرية إطلاقاً.']
    ]
  },
  sales: {
    kicker: 'المبيعات والعروض',
    title: 'دليل مبيعات الباقات وإقناع المشترك',
    intro: 'ركز على احتياج العائلة بدلاً من الحديث بالأرقام الجافة، وقدّم الباقات الرسمية بأسلوب جذاب وصادق.',
    topics: [
      ['اكتشاف احتياج العائلة', 'اسأل المشترك: كم جهاز متصل بالبيت؟ هل لديكم ألعاب بلايستيشن، بثوث تلفزيونية 4K، أم تصفح واستخدام يومي؟'],
      ['شرح باقة Basic (35 ألف د.ع)', '«الباقة الأساسية من أرض الكرم بـ 35,000 دينار شهرياً توفرلك فايبر ضوئي مكرّس وسرعة تضمن مشاهدة وبث مستقر بدون تقطيع.»'],
      ['توضيح ميزة الفايبر الضوئي', '«الإنترنت الضوئي من أرض الكرم ما يتأثر بالمطر أو العواصف أو أبراج الوايرلس، لأن الإشارة توصلك بكيبل ضوئي مخصص لحد بيتك.»'],
      ['عروض التجديد والمتابعة', 'وضّح للمشترك كيفية التجديد قبل انتهاء الاشتراك بيومين لضمان عدم توقف الخدمة عن أجهزة البيت.'],
      ['التعامل مع اعتراض السعر', 'قارن استقرار الفايبر بسرعات الأبراج القديمة التي تتذبذب عند الضغط؛ الفايبر يمنح قيمة حقيقية مقابل المبلغ المدفوع.']
    ]
  },
  training: {
    kicker: 'التطوير المهني',
    title: 'مسار تأهيل الموظف الجديد (Onboarding)',
    intro: 'خطة تدريبية متكاملة تنقل الموظف من مرحلة التعلم إلى الممارسة بثقة وإتقان.',
    topics: [
      ['الأسبوع الأول: الأساسيات النظرية', 'دراسة مصطلحات الـ FTTH، تقنية GPON، هيكلية شبكة أرض الكرم، ومهام كل قسم بالشركة.'],
      ['الأسبوع الثاني: الملاحظة المباشرة', 'الجلوس بجانب موظف متمرس، الاستماع للمكالمات الحية، ومتابعة كيفية توثيق الحالات في النظام.'],
      ['محاكاة سيناريوهات الأعطال', 'التدريب العملي على فحص لمبات الـ ONU، قراءة الـ Power Meter، وتشخيص مختلف مشاكل الراوترات.'],
      ['اختبار الجاهزية والجودة', 'مراجعة المشرف لأسلوب التواصل والدقة التقنية قبل السماح بالرد المستقل على المشتركين.'],
      ['التحديث المستمر للمعرفة', 'حضور ورش العمل التقنية الدورية والاطلاع على كل راوتر أو جهاز جديد يتم اعتماده بالشركة.']
    ]
  },
  maintenance: {
    kicker: 'الصيانة الميدانية',
    title: 'دليل الفحص الميداني الاحترافي بالموقع',
    intro: 'خطوات الفني المعتمدة عند زيارة منزل المشترك لضمان سلامة التوصيل وجودة الإشارة الضوئية.',
    topics: [
      ['١ — معاينة المسار الخارجي (Drop Cable)', 'فحص مسار الكيبل من السبلتر بالكابينة إلى منزل المشترك والتأكد من عدم وجود شد أو انحناء حاد أو تمزق.'],
      ['٢ — قياس الباور بالـ Optical Meter', 'فصل الكونكتر وقياس القدرة الضوئية RX Power، والتأكد أنها تقع بين -15 dBm و -24 dBm لمثالية الخدمة.'],
      ['٣ — تنظيف الكونكترات الضوئية', 'استخدام مناديل كحولية مخصصة للفايبر لتنظيف رؤوس SC/APC قبل ربطها بالـ ONU.'],
      ['٤ — فحص لمبات وحالة الـ ONU', 'التأكد من ثبات PON وانطفاء LOS التام، ومراجعة عمل منفذ الـ LAN مع الراوتر.'],
      ['٥ — فحص تغطية الواي فاي ومكان الراوتر', 'نصح المشترك بوضع الراوتر بمكان وسطي ومرتفع، وتجنب وضعه داخل مكتبات خشبية مغلقة أو قرب المايكروويف.'],
      ['٦ — إغلاق أمر العمل والتوثيق', 'تصوير قراءة الباور بجهاز الفحص، تسجيل القياسات بتقرير الصيانة، وأخذ توقيع المشترك برضاه عن الخدمة.']
    ]
  },
  onu: {
    kicker: 'مختبر الأجهزة',
    title: 'شرح لمبات جهاز ONU ودلالاتها الفنية',
    intro: 'دليل تفصيلي لكل مؤشر ضوئي على واجهة جهاز الـ ONU الشائع في شبكات GPON.',
    topics: [
      ['POWER (الطاقة)', 'أخضر ثابت: التغذية الكهربائية سليمة تماماً. مطفأة: تأكد من المحول والـ UPS أو مقبس الكهرباء.'],
      ['PON (Passive Optical Network)', 'أخضر ثابت: تم التعرف والتسجيل مع سيرفر الـ OLT بنجاح. تومض: الجهاز يحاول المزامنة والارتباط. مطفأة: لا يوجد تسجيل.'],
      ['LOS (Loss of Signal)', 'مطفأة: الإشارة ممتازة ولا يوجد فقدان. أحمر يرمش أو ثابت: قطع تام بالإشارة الضوئية بالفايبر أو انحناء حاد جداً.'],
      ['LAN / ETH (الشبكة المحلية)', 'أخضر/أزرق يرمش: نقل بيانات نشط مع الراوتر. مطفأة: كيبل الـ LAN مفصول أو تالف أو الراوتر مطفأ.'],
      ['معايير السلامة البصرية', 'تحذير شديد: لا تنظر أبداً بالعين المجردة داخل بورت الفايبر أو رأس الكيبل، لأن أشعة الليزر غير مرئية وقد تضر العين.']
    ]
  },
  router: {
    kicker: 'شبكة المشترك',
    title: 'تشخيص مشاكل الراوتر وتغطية الواي فاي',
    intro: 'أكثر من 70% من شكاوى المشتركين ناتجة عن التغطية اللاسلكية وليس من خط الفايبر.',
    topics: [
      ['تردد 2.4GHz مقابل 5GHz', 'نطاق 2.4GHz يغطي مسافات أبعد ويخترق الجدران، بينما 5GHz يعطي سرعات فائقة جداً ولكن بمدى أقصر.'],
      ['تأثير مكان الراوتر', 'وضع الراوتر على الأرض أو داخل خزانة يضعف الإشارة بنسبة تزيد عن 50%. يجب رفعه لمستوى متر ونصف على الأقل.'],
      ['التداخل اللاسلكي والقنوات', 'في المناطق المزدحمة بالشبكات، يجب اختيار قناة بث أقل ازدحاماً من إعدادات الراوتر (مثل القنوات 1، 6، 11).'],
      ['التجربة السلكية للفصل', 'دائماً اطلب من المشترك فحص السرعة بكيبل LAN، إذا كانت السرعة كاملة فالفايبر سليم والمشكلة بإشارة الواي فاي.']
    ]
  },
  lan: {
    kicker: 'التوصيلات السلكية',
    title: 'فحص كيبل الشبكة LAN ورؤوس RJ45',
    intro: 'سلامة الكيبل تضمن نقل السرعة كاملة من الـ ONU إلى الراوتر بدون هبوط مفاجئ.',
    topics: [
      ['فئة الكيبل (Cat5e / Cat6)', 'تأكد من استخدام كيبل Cat5e أو Cat6 يدعم سرعة 1000Mbps (Gigabit) للاستفادة الكاملة من باقة الفايبر.'],
      ['فحص كلبسة رأس RJ45', 'تأكد أن رأس الكيبل يركب بصوت نقرة واضحة، حيث أن ارتخاء الكلبسة يسبب انقطاعاً لحظياً بالخدمة.'],
      ['ترتيب ألوان الأسلاك (T568B)', 'التأكد من كبس الأطراف وفق المعيار القياسي T568B لمنع فقدان الحزم وتداخل الإشارات.'],
      ['تجنب الشد والتمديد بجانب الكهرباء', 'لا تمدد كيبل الشبكة ملاصقاً لأسلاك الكهرباء ذات الجهد العالي لتفادي التشويش الكهرومغناطيسي.']
    ]
  },
  ups: {
    kicker: 'الطاقة المستمرة',
    title: 'فحص جهاز الـ UPS ومصادر التغذية',
    intro: 'استقرار الإنترنت يعتمد كلياً على ثبات الطاقة المجهزة للـ ONU والراوتر.',
    topics: [
      ['وظيفة الـ UPS الميداني', 'منع إعادة تشغيل الـ ONU والراوتر أثناء التحويل بين الكهرباء الوطنية ومولدات الحي.'],
      ['مطابقة الفولتية والتيار (Volt/Amp)', 'تأكد من أن مخرج الـ UPS يعطي 12V أو 9V وفق متطلبات الجهاز، لتفادي احتراق البورد أو إعادة التشغيل المستمر.'],
      ['فحص كفاءة البطارية', 'إذا انطفأ الجهاز فور انقطاع الكهرباء، فهذا يعني تلف بطارية الـ UPS وتحتاج إلى استبدال.']
    ]
  },
  'router-tplink': {
    kicker: 'إعدادات راوتر TP-Link',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر TP-Link',
    intro: 'العناوين الافتراضية الشائعة: 192.168.0.1 أو 192.168.1.1 أو tplinkwifi.net.',
    topics: [
      ['١ — تسجيل الدخول', 'اتصل بالراوتر وافتح المتصفح واكتب 192.168.0.1 واكتب admin / admin أو الباسورد الخاص بك.'],
      ['٢ — تغيير اسم الشبكة', 'ادخل إلى قائمة Wireless ثم Wireless Settings وعدّل اسم الشبكة في خانة Wireless Network Name (SSID).'],
      ['٣ — تغيير الرمز السري', 'ادخل إلى Wireless Security واختر WPA/WPA2-Personal ثم اكتب رمزاً قوياً في خانة Wireless Password.'],
      ['٤ — الحفظ وإعادة الاتصال', 'اضغط Save بالأسفل، وسينقطع اتصالك؛ ابحث عن الشبكة بالاسم الجديد واكتب الرمز السري.']
    ]
  },
  'router-huawei': {
    kicker: 'إعدادات راوتر Huawei',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر Huawei',
    intro: 'العنوان الشائع: 192.168.3.1 أو 192.168.8.1.',
    topics: [
      ['١ — فتح صفحة الإدارة', 'افتح المتصفح واكتب 192.168.3.1 وسجل الدخول بالمعلومات المكتوبة على الملصق الخلفي.'],
      ['٢ — الإعدادات اللاسلكية', 'من القائمة العلوية أو الجانبية اختر Wi-Fi Settings ثم Wi-Fi Basic Settings.'],
      ['٣ — تعديل البيانات', 'عدّل Wi-Fi Name (SSID) لتغيير الاسم، و Wi-Fi Password لتغيير رمز المرور.'],
      ['٤ — الحفظ', 'اضغط Save أو Apply وانتظر دقيقة لإعادة بث الشبكة بالبيانات الجديدة.']
    ]
  },
  'router-zte': {
    kicker: 'إعدادات راوتر ZTE',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر ZTE',
    intro: 'العنوان الشائع: 192.168.1.1.',
    topics: [
      ['١ — الدخول للنظام', 'افتح 192.168.1.1 واكتب اسم المستخدم وكلمة المرور المخصصة.'],
      ['٢ — إعدادات WLAN', 'انتقل إلى Local Network ثم WLAN ثم WLAN Basic أو SSID Configuration.'],
      ['٣ — كلمة المرور', 'اكتب الباسورد الجديد في خانة WPA Passphrase مع التأكد من قوة الرمز.'],
      ['٤ — التأكيد', 'اضغط Apply أسفل الصفحة لتطبيق التغييرات.']
    ]
  },
  'router-tenda': {
    kicker: 'إعدادات راوتر Tenda',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر Tenda',
    intro: 'العنوان الشائع: 192.168.0.1 أو tendawifi.com.',
    topics: [
      ['١ — الدخول السريع', 'افتح tendawifi.com أو 192.168.0.1 وسجل دخولك.'],
      ['٢ — خيار Wireless Settings', 'من القائمة الجانبية اضغط مباشرة على Wireless Settings.'],
      ['٣ — التعديل بخطوة واحدة', 'ستجد WiFi Name و WiFi Password في نفس الصفحة، قم بتعديلها.'],
      ['٤ — الحفظ', 'اضغط OK أسفل الشاشة، وسيعيد الراوتر تشغيل بث الواي فاي.']
    ]
  },
  'router-dlink': {
    kicker: 'إعدادات راوتر D-Link',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر D-Link',
    intro: 'العنوان الشائع: 192.168.0.1 أو 192.168.1.1.',
    topics: [
      ['١ — تسجيل الدخول', 'ادخل لعنوان الراوتر واكتب اسم المستخدم admin.'],
      ['٢ — Wireless Setup', 'من تبويب Setup اختر Wireless Settings ثم Manual Wireless Network Setup.'],
      ['٣ — ضبط الأمان', 'عدّل Wireless Network Name واكتب الرمز الجديد في Pre-Shared Key.'],
      ['٤ — حفظ الإعدادات', 'اضغط Save Settings لإتمام التعديل.']
    ]
  },
  'router-xiaomi': {
    kicker: 'إعدادات راوتر Xiaomi',
    title: 'تغيير اسم الشبكة ورمز المرور لراوتر Xiaomi',
    intro: 'العنوان الشائع: 192.168.31.1 أو miwifi.com أو عبر تطبيق Mi Home.',
    topics: [
      ['١ — صفحة الإدارة', 'افتح 192.168.31.1 أو تطبيق Mi Wi-Fi بالهاتف.'],
      ['٢ — Settings', 'انتقل إلى Settings ثم تبويب Wi-Fi.'],
      ['٣ — تحديث البيانات', 'عدّل Name و Password للترددين 2.4G و 5G.'],
      ['٤ — الحفظ التلقائي', 'اضغط Save وسيعيد الراوتر الاتصال خلال ثوانٍ.']
    ]
  }
};

/* 5. Rich Modal Open & Close System */
const lessonModal = document.getElementById('lessonModal');
const modalClose = document.getElementById('modalClose');
const modalCloseBtn = document.getElementById('modalCloseBtn');
const modalKicker = document.getElementById('modalKicker');
const modalTitle = document.getElementById('modalTitle');
const modalIntro = document.getElementById('modalIntro');
const modalTopics = document.getElementById('modalTopics');

function openLessonModal(key) {
  const data = lessonData[key];
  if (!data || !lessonModal) return;
  modalKicker.textContent = data.kicker;
  modalTitle.textContent = data.title;
  modalIntro.textContent = data.intro;
  modalTopics.innerHTML = '';

  data.topics.forEach((t, idx) => {
    const card = document.createElement('div');
    card.className = 'p-3.5 rounded-2xl bg-slate-50 dark:bg-slate-800/80 border border-slate-200 dark:border-slate-700 space-y-1';
    card.innerHTML = `
      <div class="flex items-center gap-2">
        <span class="w-5 h-5 rounded-lg bg-blue-100 dark:bg-blue-950 text-brand-blue dark:text-cyan-400 font-black text-xs flex items-center justify-center">${idx + 1}</span>
        <b class="text-xs font-bold text-slate-900 dark:text-white">${t[0]}</b>
      </div>
      <p class="text-xs text-slate-600 dark:text-slate-400 leading-relaxed pr-7">${t[1]}</p>
    `;
    modalTopics.appendChild(card);
  });

  lessonModal.classList.remove('hidden');
  lessonModal.classList.add('flex');
  document.body.style.overflow = 'hidden';
}

function closeLessonModal() {
  if (!lessonModal) return;
  lessonModal.classList.add('hidden');
  lessonModal.classList.remove('flex');
  document.body.style.overflow = '';
}

document.querySelectorAll('[data-open]').forEach(btn => {
  btn.addEventListener('click', e => {
    e.preventDefault();
    openLessonModal(btn.getAttribute('data-open'));
  });
});

modalClose?.addEventListener('click', closeLessonModal);
modalCloseBtn?.addEventListener('click', closeLessonModal);
lessonModal?.addEventListener('click', e => { if (e.target === lessonModal) closeLessonModal(); });
document.addEventListener('keydown', e => { if (e.key === 'Escape') closeLessonModal(); });

/* 6. Live Interactive ONU & Optical Power Simulator Logic */
const simLedPower = document.getElementById('simLedPower');
const simLedPon = document.getElementById('simLedPon');
const simLedLos = document.getElementById('simLedLos');
const simLedLan = document.getElementById('simLedLan');
const simPowerTxt = document.getElementById('simPowerTxt');
const simPonTxt = document.getElementById('simPonTxt');
const simLosTxt = document.getElementById('simLosTxt');
const simLanTxt = document.getElementById('simLanTxt');
const simStatusPill = document.getElementById('simStatusPill');
const simRxMeterVal = document.getElementById('simRxMeterVal');
const simMeterBar = document.getElementById('simMeterBar');
const simMeterVerdict = document.getElementById('simMeterVerdict');
const simActionTitle = document.getElementById('simActionTitle');
const simActionDesc = document.getElementById('simActionDesc');
const simCallAction = document.getElementById('simCallAction');
const simFieldAction = document.getElementById('simFieldAction');
const dbmSlider = document.getElementById('dbmSlider');
const manualDbmBadge = document.getElementById('manualDbmBadge');

const scenarios = {
  normal: {
    power: 'on-green', powerTxt: 'مشتغلة ثابت',
    pon: 'on-green', ponTxt: 'تسجيل ناجح',
    los: 'off', losTxt: 'مطفأة (سليمة)',
    lan: 'on-blue blink-fast', lanTxt: 'نقل بيانات',
    dbm: -20.5,
    statusText: 'الحالة: طبيعية وممتازة',
    statusClass: 'bg-emerald-500/20 text-emerald-400 border-emerald-500/40',
    title: 'تشخيص الخدمة: مستقرة وسليمة 100%',
    desc: 'جهاز الـ ONU متصل بالسيرفر والـ OLT بنجاح، ومستوى القدرة الضوئية مثالي تماماً، وكيبل الشبكة ينقل البيانات بدون أي فقدان.',
    callAction: 'الخدمة سليمة؛ إذا كان المشترك يشتكي من بطء، وجّهه لاختبار المسافة من الراوتر أو فصل الأجهزة التي تحمل ملفات ضخمة.',
    fieldAction: 'تأكد فقط من سلامة تثبيت الجهاز وعدم تعرض الكيبل للحرارة أو الضغط المنزلي.'
  },
  cut: {
    power: 'on-green', powerTxt: 'مشتغلة ثابت',
    pon: 'off', ponTxt: 'لا يوجد اتصال',
    los: 'on-red blink-slow', losTxt: 'أحمر يرمش (قطع!)',
    lan: 'on-blue', lanTxt: 'ثابت / متصل',
    dbm: -37.0,
    statusText: 'الحالة: قطع بالإشارة الضوئية (LOS RED)',
    statusClass: 'bg-red-500/20 text-red-400 border-red-500/40',
    title: 'تشخيص الخدمة: إشارة الفايبر مفقودة تماماً',
    desc: 'لمبة الـ LOS تومض باللون الأحمر أو ثابتة، ولمبة PON مطفأة. هذا يدل على انقطاع الشعيرة الضوئية بين السبلتر الخارجي وجهاز المشترك.',
    callAction: 'تأكد من عدم كسر الكيبل الأصفر الصغير داخل البيت، ثم افتح تذكرة صيانة ميدانية عاجلة فوراً مع توثيق (LOS Red).',
    fieldAction: 'افحص السبلتر بالشارع بالـ VFL (قلم الليزر الأحمر)، وحدد نقطة القطع لإعادة اللحام بالفيوجن (Fusion Splicer).'
  },
  lowPower: {
    power: 'on-green', powerTxt: 'مشتغلة ثابت',
    pon: 'on-green blink-slow', ponTxt: 'تذبذب مستمر',
    los: 'off', losTxt: 'مطفأة',
    lan: 'on-blue blink-fast', lanTxt: 'نقل متقطع',
    dbm: -29.5,
    statusText: 'الحالة: إشارة حرجة وضعيفة جداً (-29 dBm)',
    statusClass: 'bg-amber-500/20 text-amber-400 border-amber-500/40',
    title: 'تشخيص الخدمة: قدرة ضوئية منخفضة (High Attenuation)',
    desc: 'القراءة تجاوزت الحد المقبول (-27 dBm)، مما يسبب فقدان حزم (Packet Loss)، بطء شديد، وفصل متكرر كل بضع دقائق.',
    callAction: 'أبلغ المشترك بأن الإشارة الواصلة ضعيفة وتحتاج لوزن وضبط من الفني الميداني، ولا ينفع تغيير الباسورد.',
    fieldAction: 'افحص انحناء الكيبل في مسار النزول، ونظّف كونكتر SC/APC أو أعد تركيب رأس الفاست كونكتر.'
  },
  powerOff: {
    power: 'off', powerTxt: 'مطفأة تماماً',
    pon: 'off', ponTxt: 'مطفأة',
    los: 'off', losTxt: 'مطفأة',
    lan: 'off', lanTxt: 'مطفأة',
    dbm: -38.0,
    statusText: 'الحالة: الجهاز لا يصله تيار كهربائي',
    statusClass: 'bg-slate-500/20 text-slate-400 border-slate-500/40',
    title: 'تشخيص الخدمة: انقطاع الطاقة أو تلف المحوّل',
    desc: 'جميع لمبات الجهاز مطفأة تماماً، وهذا يدل على انقطاع التيار الكهربائي أو تلف محول الـ 12V أو تفريغ بطارية الـ UPS.',
    callAction: 'اطلب من المشترك التحقق من مقبس الكهرباء وزر التشغيل بالـ ONU وتجربة شاحن الـ UPS بمقبس آخر.',
    fieldAction: 'قس جهد الخرج من المحول بالمولتميتر وتأكد من أنه يخرج 12V / 1A بثبات.'
  },
  lanCut: {
    power: 'on-green', powerTxt: 'مشتغلة ثابت',
    pon: 'on-green', ponTxt: 'تسجيل ناجح',
    los: 'off', losTxt: 'مطفأة',
    lan: 'off', lanTxt: 'مطفأة (مفصول)',
    dbm: -19.5,
    statusText: 'الحالة: الفايبر واصل، لكن كيبل الراوتر مفصول',
    statusClass: 'bg-purple-500/20 text-purple-400 border-purple-500/40',
    title: 'تشخيص الخدمة: انقطاع الرابط بين الـ ONU والراوتر',
    desc: 'الفايبر واصل والخدمة فعالة 100% داخل الـ ONU، لكن لمبة الـ LAN مطفأة؛ الراوتر لا يصله إنترنت بسبب كيبل الشبكة.',
    callAction: 'اطلب من المشترك التأكد من أن كيبل الـ LAN مشكوك بمنفذ WAN الأزرق بالراوتر ومكبوس بإحكام من الطرفين.',
    fieldAction: 'استخدم تيستر الشبكة (Cable Tester) لفحص الأسلاك الثمانية أو استبدل كيبل الـ Patch Cord.'
  }
};

function updateSimulator(state) {
  // LEDs
  simLedPower.className = `w-6 h-6 rounded-full led ${state.power}`;
  simLedPon.className = `w-6 h-6 rounded-full led ${state.pon}`;
  simLedLos.className = `w-6 h-6 rounded-full led ${state.los}`;
  simLedLan.className = `w-6 h-6 rounded-full led ${state.lan}`;

  simPowerTxt.textContent = state.powerTxt;
  simPonTxt.textContent = state.ponTxt;
  simLosTxt.textContent = state.losTxt;
  simLanTxt.textContent = state.lanTxt;

  // Status
  simStatusPill.className = `px-3 py-1 rounded-full text-xs font-black border ${state.statusClass}`;
  simStatusPill.textContent = state.statusText;

  // Rx Meter
  simRxMeterVal.textContent = state.dbm <= -37 ? 'No Signal (-∞)' : `${state.dbm.toFixed(1)} dBm`;
  let percent = Math.min(Math.max(((state.dbm - (-38)) / ((-8) - (-38))) * 100, 5), 100);
  simMeterBar.style.width = percent + '%';

  // Slider sync
  if (dbmSlider) dbmSlider.value = state.dbm;
  if (manualDbmBadge) manualDbmBadge.textContent = `${state.dbm.toFixed(1)} dBm`;

  // Verdict text
  if (state.dbm > -8) {
    simMeterVerdict.className = 'text-xs text-amber-400 font-bold';
    simMeterVerdict.textContent = '⚠️ تنبيه: الإشارة قوية جداً وقد تسبب تشويشاً على الحساس الضوئي.';
  } else if (state.dbm >= -27 && state.dbm <= -8) {
    simMeterVerdict.className = 'text-xs text-emerald-400 font-bold';
    simMeterVerdict.textContent = '✓ القراءة ضمن المجال القياسي المعتمد لشركة أرض الكرم (-8 إلى -27 dBm).';
  } else if (state.dbm < -27 && state.dbm > -35) {
    simMeterVerdict.className = 'text-xs text-amber-400 font-bold';
    simMeterVerdict.textContent = '⚠️ القراءة حرجة وضعيفة (-28 إلى -34 dBm) وتسبب تقطيعاً مستمراً.';
  } else {
    simMeterVerdict.className = 'text-xs text-red-400 font-bold';
    simMeterVerdict.textContent = '✕ لا توجد إشارة ضوئية (قطع تام بالفايبر أو انكسار الشعيرة).';
  }

  // Action box
  simActionTitle.textContent = state.title;
  simActionDesc.textContent = state.desc;
  simCallAction.textContent = state.callAction;
  simFieldAction.textContent = state.fieldAction;
}

// Button Clicks
document.querySelectorAll('.sim-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.sim-btn').forEach(b => {
      b.classList.remove('border-brand-blue', 'shadow-md', 'shadow-brand-blue/15');
      b.classList.add('border-slate-200', 'dark:border-slate-700');
    });
    btn.classList.remove('border-slate-200', 'dark:border-slate-700');
    btn.classList.add('border-brand-blue', 'shadow-md', 'shadow-brand-blue/15');

    const sc = scenarios[btn.getAttribute('data-scenario')];
    if (sc) updateSimulator(sc);
  });
});

// Slider Input
dbmSlider?.addEventListener('input', e => {
  const val = parseFloat(e.target.value);
  manualDbmBadge.textContent = `${val.toFixed(1)} dBm`;

  let customState;
  if (val < -32) {
    customState = { ...scenarios.cut, dbm: val };
  } else if (val < -27) {
    customState = { ...scenarios.lowPower, dbm: val };
  } else {
    customState = { ...scenarios.normal, dbm: val };
  }
  updateSimulator(customState);
});

// Initialize with normal
updateSimulator(scenarios.normal);

/* 7. Speed Test Simulator */
const startSpeedBtn = document.getElementById('startSpeedTestBtn');
const speedNumDisplay = document.getElementById('speedNumDisplay');
const speedMeterBar = document.getElementById('speedMeterBar');
const pingDisplay = document.getElementById('pingDisplay');
const jitterDisplay = document.getElementById('jitterDisplay');

let isTesting = false;
startSpeedBtn?.addEventListener('click', () => {
  if (isTesting) return;
  isTesting = true;
  startSpeedBtn.disabled = true;
  startSpeedBtn.textContent = '⏳ جاري القياس الفعلي للإشارة...';
  speedMeterBar.style.width = '0%';
  speedNumDisplay.textContent = '0.0';
  pingDisplay.textContent = '4 ms';
  jitterDisplay.textContent = '1 ms';

  let current = 0;
  const target = 295.4; // Target speed Mbps
  const interval = setInterval(() => {
    current += Math.random() * 25 + 10;
    if (current >= target) {
      current = target;
      clearInterval(interval);
      startSpeedBtn.disabled = false;
      startSpeedBtn.textContent = '✓ اكتمل الفحص! إعادة الاختبار ↺';
      isTesting = false;
    }
    speedNumDisplay.textContent = current.toFixed(1);
    speedMeterBar.style.width = Math.min((current / 350) * 100, 100) + '%';
  }, 70);
});

/* 8. Quick Search System (Ctrl+K or Button) */
const quickSearchBtn = document.getElementById('quickSearchBtn');
const mobileSearchTrigger = document.getElementById('mobileSearchTrigger');
const searchModal = document.getElementById('searchModal');
const closeSearchModal = document.getElementById('closeSearchModal');
const searchInput = document.getElementById('searchInput');
const searchResults = document.getElementById('searchResults');

function openSearch() {
  searchModal.classList.remove('hidden');
  searchModal.classList.add('flex');
  searchInput.focus();
}
function closeSearch() {
  searchModal.classList.add('hidden');
  searchModal.classList.remove('flex');
  searchInput.value = '';
  searchResults.innerHTML = '';
}

quickSearchBtn?.addEventListener('click', openSearch);
mobileSearchTrigger?.addEventListener('click', () => {
  mobileMenu?.classList.add('hidden');
  openSearch();
});
closeSearchModal?.addEventListener('click', closeSearch);
searchModal?.addEventListener('click', e => { if (e.target === searchModal) closeSearch(); });

document.addEventListener('keydown', e => {
  if ((e.ctrlKey || e.metaKey) && e.key.toLowerCase() === 'k') {
    e.preventDefault();
    openSearch();
  }
  if (e.key === 'Escape' && !searchModal.classList.contains('hidden')) {
    closeSearch();
  }
});

searchInput?.addEventListener('input', e => {
  const query = e.target.value.trim().toLowerCase();
  searchResults.innerHTML = '';
  if (!query) return;

  const hits = [];
  Object.keys(lessonData).forEach(key => {
    const item = lessonData[key];
    const matchTitle = item.title.toLowerCase().includes(query) || item.kicker.toLowerCase().includes(query);
    const matchTopic = item.topics.some(t => t[0].toLowerCase().includes(query) || t[1].toLowerCase().includes(query));
    if (matchTitle || matchTopic) {
      hits.push({ key, title: item.title, kicker: item.kicker });
    }
  });

  if (hits.length === 0) {
    searchResults.innerHTML = `<div class="p-3 text-slate-400 text-center">لا توجد نتائج مطابقة لـ "${query}"</div>`;
    return;
  }

  hits.forEach(hit => {
    const el = document.createElement('div');
    el.className = 'p-3 rounded-xl bg-slate-50 dark:bg-slate-800 hover:bg-brand-blue/10 dark:hover:bg-slate-700 cursor-pointer flex justify-between items-center transition';
    el.innerHTML = `
      <div>
        <b class="text-xs text-slate-900 dark:text-white block">${hit.title}</b>
        <span class="text-[10px] text-brand-blue dark:text-cyan-400 font-bold">${hit.kicker}</span>
      </div>
      <span class="text-xs text-slate-400">فتح ←</span>
    `;
    el.addEventListener('click', () => {
      closeSearch();
      openLessonModal(hit.key);
    });
    searchResults.appendChild(el);
  });
});

/* 9. Mobile Navbar Toggle */
const mobileMenuBtn = document.getElementById('mobileMenuBtn');
const mobileMenu = document.getElementById('mobileMenu');
mobileMenuBtn?.addEventListener('click', () => {
  mobileMenu?.classList.toggle('hidden');
});
mobileMenu?.querySelectorAll('a').forEach(a => {
  a.addEventListener('click', () => mobileMenu.classList.add('hidden'));
});

/* 10. Dynamic Current Year */
const yr = document.getElementById('currentYear');
if (yr) yr.textContent = new Date().getFullYear();
</script>
</body>
</html>
