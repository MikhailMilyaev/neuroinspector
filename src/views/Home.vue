<template>
  <div id="top" class="min-h-screen bg-slate-50 text-slate-900 font-sans scroll-smooth overflow-x-hidden w-full">
<header class="bg-white/90 backdrop-blur-md border-b sticky top-0 z-50 w-full">
  <div class="container mx-auto px-3 sm:px-4 md:px-6 py-3 sm:py-4 flex justify-between items-center gap-1 sm:gap-2">
    
    <div @click="scrollToTop" class="flex items-center gap-1.5 sm:gap-3 cursor-pointer hover:opacity-80 transition shrink-0">
      <img 
        src="/images/logo.png" 
        alt="Нейроинспектор" 
        class="h-4 sm:h-5 md:h-6 w-auto object-contain"
      />
      <span class="text-[15px] sm:text-xl md:text-2xl font-bold text-blue-700 tracking-tighter sm:tracking-tight uppercase">
        Нейроинспектор
      </span>
    </div>

    <nav class="hidden lg:flex items-center space-x-4 xl:space-x-8 font-bold text-[10px] xl:text-xs uppercase tracking-widest text-slate-600">
      <a href="#problems" class="cursor-pointer hover:text-blue-600 transition-colors">Проблемы</a>
      <a href="#capabilities" class="cursor-pointer hover:text-blue-600 transition-colors">Возможности</a>
      <a href="#setup" class="cursor-pointer hover:text-blue-600 transition-colors">Настройка</a>
      <a href="#integration" class="cursor-pointer hover:text-blue-600 transition-colors">Безопасность</a>
      <a href="#economy" class="cursor-pointer hover:text-blue-600 transition-colors">Экономика</a>
    </nav>

    <button 
      @click="scrollToContact" 
      class="cursor-pointer bg-blue-600 text-white px-2.5 py-2 sm:px-5 sm:py-3 rounded-lg hover:bg-blue-700 active:scale-95 transition-all font-bold text-[9px] xs:text-[10px] sm:text-xs uppercase whitespace-nowrap shrink-0 shadow-sm"
    >
      Запустить пилот
    </button>
    
  </div>
</header>

    <section class="relative bg-slate-900 text-white py-12 md:py-20 lg:py-32 overflow-hidden w-full">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute inset-0" style="background-image: radial-gradient(#3b82f6 1px, transparent 1px); background-size: 40px 40px;"></div>
      </div>
      <div class="container mx-auto px-4 sm:px-6 relative z-10">
        <div class="grid lg:grid-cols-2 gap-10 lg:gap-16 items-center">
          <div class="w-full">
            <h1 class="text-[28px] xs:text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold mb-6 leading-tight tracking-tight">
              ИИ-контроль <span class="text-blue-500">брака</span>
            </h1>
            <p class="text-base sm:text-lg md:text-xl text-slate-400 mb-8 sm:mb-10 leading-relaxed max-w-xl">
              Система компьютерного зрения для автоматизации контроля качества на скоростях до 120 FPS с точностью детекции 98%+.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 w-full">
              <button @click="scrollToContact" class="cursor-pointer w-full sm:w-auto text-center bg-blue-600 px-6 sm:px-8 py-4 rounded-xl font-bold text-base sm:text-lg hover:bg-blue-500 transition-all shadow-xl shadow-blue-900/40">
                Внедрить пилот бесплатно
              </button>
              <div class="w-full sm:w-auto flex items-center justify-center sm:justify-start gap-4 px-4 sm:px-6 py-4 bg-slate-800/50 rounded-xl border border-slate-700 shrink-0">
                <div class="text-blue-400 font-bold text-xl sm:text-2xl">2-4</div>
                <div class="text-slate-400 text-[10px] sm:text-xs leading-tight uppercase font-semibold text-left">Недели на<br>внедрение</div>
              </div>
            </div>
          </div>
          <div class="relative mt-8 sm:mt-12 lg:mt-0 w-full">
            <div class="rounded-2xl md:rounded-3xl overflow-hidden border-4 sm:border-8 md:border-[12px] border-slate-800 shadow-2xl relative bg-slate-800 w-full">
              <img src="/images/factory-line.png" alt="Промышленная линия" class="w-full opacity-80" />
              <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-16 h-16 xs:w-24 xs:h-24 md:w-48 md:h-48 border-2 border-blue-500/50 rounded-full animate-ping"></div>
              <div class="absolute bottom-3 left-3 sm:bottom-4 sm:left-4 md:bottom-6 md:left-6 bg-slate-900/90 backdrop-blur-xl p-2 sm:p-3 md:p-5 rounded-lg sm:rounded-xl md:rounded-2xl border border-blue-500/30">
                <div class="text-lg sm:text-xl md:text-3xl font-black text-blue-500 leading-none">98.7%</div>
                <div class="text-[7px] sm:text-[8px] md:text-[10px] text-slate-300 uppercase font-bold tracking-widest mt-1">Точность модели</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="problems" class="py-16 md:py-24 bg-white border-b w-full">
      <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center max-w-3xl mx-auto mb-10 sm:mb-12 md:mb-20">
          <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-4 sm:mb-6 italic text-slate-900 leading-tight">Почему ручной контроль — <span class="text-blue-600">это убытки?</span></h2>
          <p class="text-slate-500 text-base sm:text-lg md:text-xl">Человеческий фактор на высоких скоростях линии неизбежно приводит к финансовым и репутационным потерям.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 md:gap-10 mb-12 md:mb-20">
          <div v-for="(problem, i) in problems" :key="i" class="group p-6 sm:p-8 md:p-10 bg-slate-50 rounded-2xl md:rounded-[2.5rem] border border-transparent hover:border-blue-200 hover:bg-white hover:shadow-2xl transition-all duration-500">
            <div class="w-12 h-12 sm:w-16 sm:h-16 bg-blue-600/10 rounded-2xl flex items-center justify-center mb-6 sm:mb-8 group-hover:bg-blue-600 group-hover:text-white transition-colors">
              <component :is="problem.icon" class="w-6 h-6 sm:w-8 sm:h-8 text-blue-600 group-hover:text-white" />
            </div>
            <h3 class="text-lg sm:text-xl md:text-2xl font-bold mb-3 sm:mb-4 text-slate-800 uppercase tracking-tight">{{ problem.title }}</h3>
            <p class="text-slate-600 text-sm sm:text-base md:text-lg leading-relaxed">{{ problem.text }}</p>
          </div>
        </div>

        <div class="bg-slate-900 rounded-2xl md:rounded-[3rem] p-5 sm:p-8 md:p-16 text-white overflow-hidden relative">
          <div class="grid lg:grid-cols-2 gap-8 sm:gap-10 md:gap-16 items-center relative z-10 w-full">
            <div class="w-full">
              <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-6 sm:mb-8 italic text-blue-400">Сколько это стоит заводу?</h2>
              <div class="space-y-6 md:space-y-8 w-full">
                <div class="flex flex-col sm:flex-row sm:items-center gap-2 sm:gap-4 md:gap-6 border-b border-slate-700 pb-4 sm:pb-6">
                  <div class="text-blue-500 text-2xl sm:text-3xl md:text-4xl font-bold">80 000</div>
                  <div class="text-slate-300 text-sm sm:text-base md:text-lg uppercase font-bold tracking-tighter">единиц продукции в сутки</div>
                </div>
                <div class="flex flex-col sm:flex-row sm:items-center gap-2 sm:gap-4 md:gap-6 border-b border-slate-700 pb-4 sm:pb-6">
                  <div class="text-blue-500 text-2xl sm:text-3xl md:text-4xl font-bold">1.6 млн ₽</div>
                  <div class="text-slate-300 text-sm sm:text-base md:text-lg uppercase font-bold tracking-tighter">прямых потерь в месяц</div>
                </div>
                <p class="text-slate-400 italic text-sm sm:text-base md:text-lg leading-relaxed border-l-2 border-blue-600 pl-4">
                  "Даже снижение брака на 0,3% окупает внедрение системы за 2-4 месяца эксплуатации."
                </p>
              </div>
            </div>
            <div class="bg-slate-800 p-5 sm:p-6 md:p-12 rounded-2xl md:rounded-[2.5rem] border border-slate-700 shadow-2xl w-full">
              <h4 class="text-blue-400 font-bold mb-4 sm:mb-6 md:mb-8 uppercase tracking-widest text-[10px] sm:text-xs leading-snug">Пример расчета (Типовой FMCG-завод)</h4>
              <div class="space-y-4 md:space-y-6 w-full">
                <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-1 sm:gap-0 text-sm sm:text-base md:text-lg w-full">
                  <span class="text-slate-400">Потери в день:</span>
                  <span class="font-bold text-white">16 000 — 56 000 ₽</span>
                </div>
                <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-1 sm:gap-0 text-base sm:text-lg md:text-2xl border-t border-slate-700 pt-4 sm:pt-6 w-full">
                  <span class="text-slate-400">Потери в месяц:</span>
                  <span class="font-bold text-blue-400">0.5 — 1.6 млн ₽</span>
                </div>
                <div class="mt-6 md:mt-8 p-4 md:p-6 bg-blue-600 rounded-xl md:rounded-2xl text-center shadow-lg shadow-blue-600/20 w-full">
                  <span class="text-sm sm:text-base md:text-lg font-bold uppercase tracking-tight text-white">Окупаемость: 2-4 месяца</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="capabilities" class="py-16 md:py-24 bg-slate-50 w-full">
      <div class="container mx-auto px-4 sm:px-6">
        <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-10 sm:mb-12 md:mb-16 text-center italic leading-tight">Что именно находит <span class="text-blue-600">НейроИнспектор?</span></h2>
        <div class="grid grid-cols-1 xs:grid-cols-2 sm:grid-cols-2 lg:grid-cols-4 gap-3 sm:gap-4 md:gap-6">
          <div v-for="defect in defects" :key="defect.name" class="bg-white p-4 sm:p-5 md:p-6 rounded-xl md:rounded-2xl shadow-sm border border-slate-200 hover:shadow-md transition flex items-center gap-3">
            <div class="w-8 h-8 sm:w-10 sm:h-10 bg-slate-100 rounded-lg flex items-center justify-center shrink-0">
              <svg class="w-5 h-5 sm:w-6 sm:h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
            </div>
            <div class="font-bold text-slate-800 text-sm sm:text-base md:text-lg leading-snug">{{ defect.name }}</div>
          </div>
        </div>
      </div>
    </section>

    <section id="setup" class="py-16 md:py-24 bg-white border-y w-full">
      <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-10 sm:mb-12 md:mb-16">
          <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-3 sm:mb-4 italic">Настройка и <span class="text-blue-600">обучение</span></h2>
          <p class="text-slate-500 text-sm sm:text-base md:text-lg">Гибкое управление ИИ и создание моделей за 15 минут</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-8 sm:gap-10 lg:gap-16 items-center mb-12 sm:mb-16 md:mb-24 w-full">
          <div class="rounded-xl sm:rounded-2xl md:rounded-3xl overflow-hidden shadow-2xl border border-slate-300 bg-white p-2 w-full">
            <img src="/images/setup-screen.png" alt="Интерфейс настройки" class="w-full h-auto rounded-lg sm:rounded-xl md:rounded-2xl" />
          </div>
          <div class="space-y-4 md:space-y-6 w-full">
            <h3 class="text-lg sm:text-xl md:text-2xl font-bold mb-4 md:mb-6 text-slate-800 uppercase tracking-tight text-center lg:text-left">Параметры детекции</h3>
            <div class="grid gap-3 sm:gap-4 w-full">
              <div v-for="block in setupBlocks" :key="block.color" :class="`p-4 md:p-5 bg-white rounded-xl border-l-4 ${block.borderClass} shadow-sm w-full`">
                <p class="text-sm sm:text-base md:text-lg leading-relaxed"><span :class="`font-bold uppercase text-[10px] md:text-xs block mb-1 ${block.textClass}`">{{ block.label }}:</span> {{ block.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <div class="grid lg:grid-cols-2 gap-8 sm:gap-10 lg:gap-16 items-center w-full">
          <div class="order-2 lg:order-1 w-full">
            <h3 class="text-xl sm:text-2xl md:text-3xl font-bold mb-4 sm:mb-6 italic text-slate-800 text-center lg:text-left leading-tight">Обучение через эталоны</h3>
            <p class="text-slate-600 mb-6 sm:mb-8 text-sm sm:text-base md:text-lg leading-relaxed text-center lg:text-left">
              Система самостоятельно строит математическую модель «идеального продукта». Для запуска точной модели достаточно от 10 эталонных снимков.
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-3 sm:gap-4 w-full">
              <div v-for="feat in trainingFeatures" :key="feat.title" class="bg-blue-50 p-4 sm:p-4 rounded-xl md:rounded-2xl text-center border border-blue-100">
                <div class="font-bold text-blue-600 mb-1 uppercase text-[10px] tracking-widest">{{ feat.title }}</div>
                <div class="text-[11px] sm:text-xs text-slate-500">{{ feat.desc }}</div>
              </div>
            </div>
          </div>
          <div class="order-1 lg:order-2 rounded-xl sm:rounded-2xl md:rounded-3xl overflow-hidden shadow-2xl border p-2 bg-slate-50 w-full">
            <img src="/images/training-ui.png" alt="Обучение ИИ" class="w-full h-auto rounded-lg sm:rounded-xl md:rounded-2xl" />
          </div>
        </div>
      </div>
    </section>

    <section id="integration" class="py-16 md:py-24 bg-slate-900 text-white relative w-full">
      <div class="container mx-auto px-4 sm:px-6 relative z-10">
        <div class="text-center mb-10 sm:mb-12 md:mb-20">
          <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-4 sm:mb-6 italic leading-tight">Безопасная интеграция в <span class="text-blue-500">ИТ-ландшафт</span></h2>
          <p class="text-slate-400 text-sm sm:text-base md:text-lg max-w-2xl mx-auto">Мы понимаем требования промышленной безопасности. Система адаптируется под любые регламенты данных.</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-6 sm:gap-8 md:gap-12 w-full">
          <div class="grid gap-4 sm:gap-6 w-full">
            <div class="bg-slate-800 p-5 sm:p-6 md:p-8 rounded-xl sm:rounded-2xl md:rounded-3xl border border-slate-700 hover:border-blue-500/50 transition w-full">
              <div class="flex flex-col sm:flex-row items-start gap-4 md:gap-6 w-full">
                <div class="w-10 h-10 sm:w-12 sm:h-12 md:w-14 md:h-14 bg-blue-600/20 rounded-lg sm:rounded-xl md:rounded-2xl flex items-center justify-center shrink-0">
                  <svg class="w-5 h-5 sm:w-6 sm:h-6 md:w-8 md:h-8 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" /></svg>
                </div>
                <div class="w-full">
                  <h4 class="text-lg sm:text-xl md:text-2xl font-bold mb-2 uppercase tracking-tighter text-white">On-Premise / Локально</h4>
                  <p class="text-slate-400 leading-relaxed text-xs sm:text-sm md:text-lg">
                    Максимальная безопасность: все вычисления происходят на сервере внутри вашей сети. Видеопоток не покидает периметр завода.
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-slate-800 p-5 sm:p-6 md:p-8 rounded-xl sm:rounded-2xl md:rounded-3xl border border-slate-700 hover:border-blue-500/50 transition w-full">
              <div class="flex flex-col sm:flex-row items-start gap-4 md:gap-6 w-full">
                <div class="w-10 h-10 sm:w-12 sm:h-12 md:w-14 md:h-14 bg-blue-600/20 rounded-lg sm:rounded-xl md:rounded-2xl flex items-center justify-center shrink-0">
                  <svg class="w-5 h-5 sm:w-6 sm:h-6 md:w-8 md:h-8 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 01-2-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>
                </div>
                <div class="w-full">
                  <h4 class="text-lg sm:text-xl md:text-2xl font-bold mb-2 uppercase tracking-tighter text-white">Cloud / Облако</h4>
                  <p class="text-slate-400 leading-relaxed text-xs sm:text-sm md:text-lg">
                    Устанавливается камера, данные через шифратор передаются в наш защищенный ЦОД для мгновенной реакции линии.
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-blue-900/30 p-4 md:p-6 rounded-xl md:rounded-2xl border-l-4 border-blue-500 w-full">
              <div class="flex flex-col md:flex-row md:items-center gap-1 sm:gap-2 md:gap-4 w-full">
                <div class="text-blue-500 font-bold uppercase text-[10px] md:text-xs tracking-widest shrink-0">Уведомления:</div>
                <p class="text-slate-300 text-[11px] sm:text-xs md:text-sm">Результаты мгновенно транслируются в систему управления для оператора.</p>
              </div>
            </div>
          </div>
          <div class="bg-blue-600 rounded-xl sm:rounded-2xl md:rounded-[2.5rem] p-6 sm:p-8 md:p-10 flex flex-col justify-center items-center text-center overflow-hidden relative shadow-2xl min-h-[250px] sm:min-h-[300px] w-full">
            <div class="relative z-10 w-full">
              <div class="text-5xl sm:text-6xl md:text-7xl font-black mb-2 sm:mb-4 text-white">100%</div>
              <div class="text-base sm:text-lg md:text-xl font-bold uppercase tracking-widest mb-4 sm:mb-6 text-white">Владение данными</div>
              <p class="text-blue-100 text-xs sm:text-sm md:text-lg opacity-90 w-full">
                Согласно регламенту, все собранные данные и статистика являются исключительной собственностью Заказчика.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="economy" class="py-16 md:py-24 bg-white w-full">
      <div class="container mx-auto px-4 sm:px-6">
        <h2 class="text-xl sm:text-2xl font-bold mb-10 sm:mb-12 md:mb-16 text-center italic uppercase tracking-widest leading-tight">Экономика внедрения</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-5 sm:gap-6 md:gap-8 text-center max-w-5xl mx-auto items-center w-full">
          <div class="p-6 sm:p-8 md:p-12 bg-slate-50 rounded-2xl md:rounded-[3rem] border border-slate-100 transition-all hover:shadow-2xl w-full">
            <div class="text-2xl sm:text-3xl md:text-5xl font-bold text-blue-600 mb-2 sm:mb-4">1.6 млн ₽</div>
            <p class="text-slate-500 uppercase text-[9px] sm:text-[10px] md:text-xs font-bold tracking-widest">Средняя экономия в месяц</p>
          </div>
          <div class="p-6 sm:p-8 md:p-12 bg-blue-600 text-white rounded-2xl md:rounded-[3rem] shadow-2xl md:scale-110 z-10 relative w-full">
             <div class="absolute -top-3 sm:-top-4 left-1/2 -translate-x-1/2 bg-yellow-400 text-slate-900 px-3 sm:px-4 py-1 rounded-full text-[9px] sm:text-[10px] font-black uppercase whitespace-nowrap">Выгодно</div>
            <div class="text-3xl sm:text-4xl md:text-5xl font-bold mb-2 sm:mb-4 text-white">0 ₽</div>
            <p class="text-blue-100 uppercase text-[9px] sm:text-[10px] md:text-xs font-bold tracking-widest">Бесплатный пилотный проект</p>
          </div>
          <div class="p-6 sm:p-8 md:p-12 bg-slate-50 rounded-2xl md:rounded-[3rem] border border-slate-100 transition-all hover:shadow-2xl w-full">
            <div class="text-2xl sm:text-3xl md:text-5xl font-bold text-blue-600 mb-2 sm:mb-4">6-12 мес</div>
            <p class="text-slate-500 uppercase text-[9px] sm:text-[10px] md:text-xs font-bold tracking-widest">Полная окупаемость (ROI)</p>
          </div>
        </div>
      </div>
    </section>

    <section id="pilot" class="py-16 md:py-24 bg-slate-50 border-y w-full">
      <div class="container mx-auto px-4 sm:px-6 text-center">
        <h2 class="text-[22px] sm:text-2xl md:text-4xl font-bold mb-4 sm:mb-6 italic leading-tight">Как проходит <span class="text-blue-600">Пилотный проект?</span></h2>
        <p class="text-slate-500 text-sm sm:text-base md:text-lg mb-10 sm:mb-12 md:mb-16 max-w-2xl mx-auto italic">«Если система не дает измеримого эффекта — вы ничего не платите»</p>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 sm:gap-6 text-left w-full">
          <div v-for="(step, i) in pilotSteps" :key="i" class="bg-white p-5 sm:p-6 md:p-8 rounded-xl sm:rounded-2xl md:rounded-3xl border border-slate-200 relative group hover:border-blue-500 transition-all w-full">
            <div class="text-blue-600 font-black text-3xl sm:text-4xl md:text-5xl opacity-10 absolute top-4 right-5 sm:right-6 group-hover:opacity-20 transition-opacity">{{ i + 1 }}</div>
            <h5 class="font-bold text-base sm:text-lg md:text-xl mb-2 sm:mb-3 text-slate-800">{{ step.title }}</h5>
            <p class="text-slate-500 text-[11px] sm:text-xs md:text-sm leading-relaxed">{{ step.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="py-16 md:py-24 bg-white overflow-hidden relative w-full">
      <div class="container mx-auto px-4 sm:px-6 relative z-10 w-full">
        <div class="max-w-4xl mx-auto bg-slate-900 rounded-2xl md:rounded-[3rem] p-6 sm:p-8 md:p-20 text-center text-white shadow-2xl shadow-blue-900/20 w-full">
          <h2 class="text-[22px] sm:text-2xl md:text-5xl font-bold mb-6 sm:mb-8 italic leading-tight text-white">Готовы оцифровать качество?</h2>
          <p class="text-slate-400 text-sm sm:text-base md:text-xl mb-8 sm:mb-12">Оставьте заявку на бесплатный пилот на вашу производственную линию.</p>
          <div class="flex flex-col sm:flex-row gap-3 sm:gap-4 justify-center items-center w-full">
            <a href="mailto:info@neuroinspector.ru" 
              class="w-full flex items-center justify-center sm:w-auto bg-blue-600 px-4 sm:px-6 py-4 md:px-10 md:py-5 rounded-xl md:rounded-2xl font-bold text-xs sm:text-sm md:text-xl hover:bg-blue-500 transition shadow-lg shadow-blue-900/40 break-all text-white">
              info@neuroinspector.ru
            </a>
            <a href="tel:+78000000000" 
              class="w-full flex items-center justify-center sm:w-auto bg-slate-800 px-4 sm:px-6 py-4 md:px-10 md:py-5 rounded-xl md:rounded-2xl font-bold text-xs sm:text-sm md:text-xl hover:bg-slate-700 transition border border-slate-700 whitespace-nowrap text-white">
              +7 (800) 000-00-00
            </a>
          </div>
        </div>
      </div>
    </section>

    <footer class="bg-slate-900 text-slate-500 py-4 sm:py-6 md:py-8 text-center border-t border-slate-800 w-full">
      <div class="container mx-auto px-4 sm:px-6 flex flex-col md:flex-row justify-between items-center gap-4 sm:gap-6 md:gap-8 w-full">
        <div class="text-center md:text-left">
          <div class="text-[10px] sm:text-xs md:text-sm font-bold text-slate-400 uppercase tracking-widest">ООО «НЕЙРОИНСПЕКТОР»</div>
        </div>
        <div class="text-[9px] sm:text-[10px] md:text-sm opacity-50">&copy; 2026 Все права защищены.</div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { 
  ExclamationTriangleIcon as WarningIcon, 
  ClockIcon, 
  ShieldCheckIcon 
} from '@heroicons/vue/24/outline';

const problems = [
  {
    title: "Пропуск брака",
    text: "Выборочный контроль пропускает 1–3% дефектов. При скоростях 60+ FPS глаз человека физически не успевает фиксировать отклонения.",
    icon: WarningIcon
  },
  {
    title: "Позднее эхо",
    text: "Брак обнаруживается на складе или у ритейлера. Ресурсы на логистику и упаковку уже потрачены, а партия подлежит списанию.",
    icon: ClockIcon
  },
  {
    title: "Риски бренда",
    text: "Штрафы сетей и риск отзыва продукции. Один дефектный продукт в партии может остановить отгрузки на миллионы рублей.",
    icon: ShieldCheckIcon
  }
];

const defects = [
  { name: "Нарушение геометрии" },
  { name: "Сколы и трещины" },
  { name: "Цветовые отклонения" },
  { name: "Посторонние включения" },
  { name: "Отсутствие элементов" },
  { name: "Дефекты упаковки" },
  { name: "Смещение маркировки" },
  { name: "Контроль наполнения" }
];

const setupBlocks = [
  { label: "Синий блок", desc: "Настройки тона, насыщенности и яркости для адаптации к освещению цеха.", borderClass: "border-blue-500", textClass: "text-blue-600" },
  { label: "Красный блок", desc: "Параметр эрозии контуров для четкой изоляции продукта от фона.", borderClass: "border-red-400", textClass: "text-red-600" },
  { label: "Желтый блок", desc: "Определение минимального порога размера объекта для фильтрации шумов.", borderClass: "border-yellow-500", textClass: "text-yellow-600" },
  { label: "Зеленый блок", desc: "Выбор режима видео: прямой поток, бинарный вид или контур объекта.", borderClass: "border-green-500", textClass: "text-green-700" }
];

const trainingFeatures = [
  { title: "Простота", desc: "Доступно оператору линии" },
  { title: "Скорость", desc: "Новая модель за 15-20 минут" },
  { title: "Точность", desc: "Нужно от 10 эталонных фото" }
];

const pilotSteps = [
  { title: "Аудит линии", desc: "Анализируем освещение, скорость и типы дефектов на вашем производстве." },
  { title: "Монтаж", desc: "Устанавливаем камеры и компактный вычислительный модуль." },
  { title: "Обучение модели", desc: "Системе загружаем эталоны и она строит математическую модель качества." },
  { title: "Оценка ROI", desc: "Через 1-2 месяца совместно считаем реальную экономию." }
];

const scrollToContact = () => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' });
const scrollToTop = () => window.scrollTo({ top: 0, behavior: 'smooth' });
</script>

<style>
html { 
  scroll-behavior: smooth; 
}
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  width: 100%;
}
@keyframes pulse-slow {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.05); opacity: 0.8; }
}
.animate-pulse-slow { animation: pulse-slow 3s infinite ease-in-out; }
</style>