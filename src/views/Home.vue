<template>
  <div id="top" class="min-h-screen bg-slate-50 text-slate-900 font-sans scroll-smooth">
    <header class="bg-white/80 backdrop-blur-md border-b sticky top-0 z-50">
      <div class="container mx-auto px-4 md:px-6 py-4 flex justify-between items-center">
        <div 
          @click="scrollToTop" 
          class="text-xl md:text-2xl font-bold text-blue-700 tracking-tight uppercase cursor-pointer hover:opacity-80 transition"
        >
          Нейроинспектор
        </div>
        <nav class="hidden lg:flex space-x-8 font-medium">
          <a href="#problems" class="hover:text-blue-600 transition text-slate-600">Проблемы</a>
          <a href="#config" class="hover:text-blue-600 transition text-slate-600">Настройка</a>
          <a href="#training" class="hover:text-blue-600 transition text-slate-600">Обучение</a>
          <a href="#economy" class="hover:text-blue-600 transition text-slate-600">Экономика</a>
        </nav>
        <button @click="scrollToContact" class="bg-blue-600 text-white px-4 py-2 md:px-6 md:py-2 rounded-lg hover:bg-blue-700 transition font-semibold text-sm md:text-base">
          Запустить пилот
        </button>
      </div>
    </header>

    <section class="relative bg-slate-900 text-white py-16 lg:py-32 overflow-hidden">
      <div class="container mx-auto px-6 relative z-10">
        <div class="grid lg:grid-cols-2 gap-12 items-center">
          <div>
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold mb-6 leading-tight">
              Промышленный <br> <span class="text-blue-500">контроль продукции</span>
            </h1>
            <p class="text-lg md:text-xl text-slate-300 mb-8 leading-relaxed">
              Система автоматического распознавания брака на базе ИИ. Интеграция в линию для контроля на скоростях до 120 FPS.
            </p>
            <button @click="scrollToContact" class="w-full sm:w-auto bg-blue-600 px-8 py-4 rounded-xl font-bold text-lg hover:bg-blue-500 transition shadow-lg shadow-blue-900/20">
              Связаться с нами
            </button>
          </div>
          <div class="relative group mt-10 lg:mt-0">
            <div class="rounded-2xl overflow-hidden border-4 border-slate-800 shadow-2xl relative">
              <img src="/images/factory-line.png" alt="Линия контроля" class="w-full h-auto object-cover bg-slate-800" />
              <div class="absolute bottom-4 left-4 bg-white/90 backdrop-blur p-4 rounded-xl shadow-xl border border-blue-100 animate-pulse-slow">
                <div class="text-2xl font-black text-blue-600">98%</div>
                <div class="text-[10px] text-slate-500 uppercase font-bold tracking-wider">Точность детекции</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="problems" class="py-20 md:py-24 bg-white">
      <div class="container mx-auto px-6">
        <div class="max-w-3xl mb-16">
          <h2 class="text-3xl md:text-4xl font-bold mb-6 italic">Почему ручной контроль <br><span class="text-blue-600 text-shadow-sm">малоэффективен?</span></h2>
          <p class="text-slate-600 text-lg md:text-xl">На скоростях 60-120 FPS человек физически не способен заметить дефекты. Это ведет к системным потерям.</p>
        </div>
        <div class="grid md:grid-cols-3 gap-8">
          <div class="p-8 bg-slate-50 rounded-3xl border border-slate-100 hover:border-blue-200 transition-colors">
            <div class="text-blue-600 mb-6">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
              </svg>
            </div>
            <h3 class="text-xl md:text-2xl font-bold mb-4 uppercase tracking-tight text-slate-800">Пропуск брака</h3>
            <p class="text-slate-600 text-base md:text-lg leading-relaxed">Выборочный контроль пропускает <b>1-3% дефектов</b>, которые уходят конечному клиенту и портят партию.</p>
          </div>
          <div class="p-8 bg-slate-50 rounded-3xl border border-slate-100 hover:border-blue-200 transition-colors">
            <div class="text-blue-600 mb-6">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl md:text-2xl font-bold mb-4 uppercase tracking-tight text-slate-800">Позднее обнаружение</h3>
            <p class="text-slate-600 text-base md:text-lg leading-relaxed">Брак обнаруживается только на складе или при возврате. Время, сырье и логистика уже потрачены впустую.</p>
          </div>
          <div class="p-8 bg-slate-50 rounded-3xl border border-slate-100 hover:border-blue-200 transition-colors">
            <div class="text-blue-600 mb-6">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 17h8m0 0V9m0 8l-8-8-4 4-6-6" />
              </svg>
            </div>
            <h3 class="text-xl md:text-2xl font-bold mb-4 uppercase tracking-tight text-slate-800">Репутация</h3>
            <p class="text-slate-600 text-base md:text-lg leading-relaxed">Крупные списания, штрафы со стороны ритейлеров и серьезные риски полного отзыва продукции с рынка.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="py-24 bg-slate-900 text-white overflow-hidden relative">
      <div class="container mx-auto px-6 relative z-10">
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <div>
            <h2 class="text-3xl md:text-4xl font-bold mb-8 italic text-blue-400">Сколько это стоит заводу?</h2>
            <div class="space-y-8">
              <div class="flex items-center gap-6 border-b border-slate-700 pb-6">
                <div class="text-blue-500 text-3xl md:text-4xl font-bold">80 000</div>
                <div class="text-slate-300 text-lg">единиц продукции в сутки</div>
              </div>
              <div class="flex items-center gap-6 border-b border-slate-700 pb-6">
                <div class="text-blue-500 text-3xl md:text-4xl font-bold">1.6 млн ₽</div>
                <div class="text-slate-300 text-lg">прямых потерь в месяц</div>
              </div>
              <p class="text-slate-400 italic text-lg leading-relaxed border-l-2 border-blue-600 pl-4">
                "Даже снижение брака на 0,3% окупает внедрение системы за 2-4 месяца эксплуатации."
              </p>
            </div>
          </div>
          <div class="bg-slate-800 p-8 md:p-12 rounded-[2.5rem] border border-slate-700 shadow-inner">
            <h4 class="text-blue-400 font-bold mb-8 uppercase tracking-widest text-sm">Пример расчета (FMCG)</h4>
            <div class="space-y-6">
              <div class="flex justify-between items-center text-lg">
                <span class="text-slate-400">Потери в день:</span>
                <span class="font-bold">16к — 56к ₽</span>
              </div>
              <div class="flex justify-between items-center text-xl md:text-2xl">
                <span class="text-slate-400">Потери в месяц:</span>
                <span class="font-bold text-blue-400">0.5 — 1.6 млн ₽</span>
              </div>
              <div class="mt-8 p-6 bg-blue-600 rounded-2xl text-center shadow-lg shadow-blue-600/20">
                <span class="text-lg font-bold">Окупаемость: 2-4 месяца</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="config" class="py-24 bg-slate-50 border-y">
      <div class="container mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold mb-4">Настройка параметров детекции</h2>
          <p class="text-slate-500 text-lg">Гибкое управление визуальными фильтрами ИИ</p>
        </div>
        <div class="grid lg:grid-cols-3 gap-12 items-start">
          <div class="lg:col-span-2 rounded-2xl overflow-hidden shadow-2xl border border-slate-300 bg-white p-2">
            <img src="/images/setup-screen.png" alt="Настройки" class="w-full rounded-lg" />
          </div>
          <div class="space-y-6">
            <div class="p-6 bg-white rounded-xl border-l-4 border-blue-500 shadow-sm">
              <p class="text-base md:text-lg leading-relaxed"><span class="font-bold text-blue-600 uppercase text-xs block mb-1">Синий блок:</span> Настройки тона, насыщенности и яркости.</p>
            </div>
            <div class="p-6 bg-white rounded-xl border-l-4 border-slate-400 shadow-sm">
              <p class="text-base md:text-lg leading-relaxed"><span class="font-bold text-slate-600 uppercase text-xs block mb-1">Серый блок:</span> Параметр эрозии контуров для изоляции продукта.</p>
            </div>
            <div class="p-6 bg-white rounded-xl border-l-4 border-yellow-500 shadow-sm">
              <p class="text-base md:text-lg leading-relaxed"><span class="font-bold text-yellow-600 uppercase text-xs block mb-1">Желтый блок:</span> Определение минимального порога размера объекта.</p>
            </div>
            <div class="p-6 bg-white rounded-xl border-l-4 border-green-500 shadow-sm">
              <p class="text-base md:text-lg font-bold text-green-700 mb-2 uppercase tracking-wide">Зеленый блок:</p>
              <ul class="text-base space-y-2 text-slate-600">
                <li class="flex items-center gap-2">✓ Видео с камеры (прямой поток)</li>
                <li class="flex items-center gap-2">✓ Чёрно-белое бинарное видео</li>
                <li class="flex items-center gap-2">✓ Видео контура объекта</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="training" class="py-24 bg-white">
      <div class="container mx-auto px-6">
        <div class="grid lg:grid-cols-2 gap-16 items-center mb-16">
          <div>
            <h2 class="text-3xl md:text-4xl font-bold mb-6 italic text-slate-800">Обучение через эталоны</h2>
            <p class="text-slate-600 mb-8 text-lg md:text-xl leading-relaxed">
              Забудьте о сложных настройках. Система самостоятельно строит математическую модель «идеального продукта», с которой будут сравниваться все объекты на линии.
            </p>
          </div>
          <div class="rounded-3xl overflow-hidden shadow-2xl border p-2 bg-slate-50">
            <img src="/images/training-ui.png" alt="Обучение" class="w-full rounded-2xl" />
          </div>
        </div>

        <div class="grid md:grid-cols-3 gap-8">
          <div class="bg-blue-50 p-8 rounded-[2.5rem] text-center border border-blue-100 hover:shadow-xl transition-shadow">
            <div class="w-14 h-14 bg-blue-600 rounded-2xl flex items-center justify-center mx-auto mb-6 text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
            </div>
            <h4 class="font-bold text-xl mb-4 uppercase">Простота</h4>
            <p class="text-base md:text-lg text-slate-600 leading-relaxed">Не нужны специалисты по данным. Обучение доступно любому оператору линии.</p>
          </div>
          <div class="bg-blue-50 p-8 rounded-[2.5rem] text-center border border-blue-100 hover:shadow-xl transition-shadow">
            <div class="w-14 h-14 bg-blue-600 rounded-2xl flex items-center justify-center mx-auto mb-6 text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h4 class="font-bold text-xl mb-4 uppercase">Скорость</h4>
            <p class="text-base md:text-lg text-slate-600 leading-relaxed">Создание новой модели под новый артикул продукции за 15-20 минут.</p>
          </div>
          <div class="bg-blue-50 p-8 rounded-[2.5rem] text-center border border-blue-100 hover:shadow-xl transition-shadow">
            <div class="w-14 h-14 bg-blue-600 rounded-2xl flex items-center justify-center mx-auto mb-6 text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
              </svg>
            </div>
            <h4 class="font-bold text-xl mb-4 uppercase">Эталоны</h4>
            <p class="text-base md:text-lg text-slate-600 leading-relaxed">Для обучения точной модели достаточно всего 10 эталонных снимков.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="economy" class="py-24 bg-slate-900 text-white">
      <div class="container mx-auto px-6">
        <h2 class="text-3xl font-bold mb-16 text-center italic uppercase tracking-widest">Экономика внедрения</h2>
        <div class="grid md:grid-cols-3 gap-8 text-center max-w-5xl mx-auto">
          <div class="p-10 bg-slate-800 rounded-3xl border border-slate-700">
            <div class="text-4xl md:text-5xl font-bold text-blue-400 mb-4">1.6 млн ₽</div>
            <p class="text-slate-400 uppercase text-xs font-bold tracking-widest">Экономия в месяц</p>
          </div>
          <div class="p-10 bg-blue-600 rounded-3xl shadow-xl md:scale-110 z-10">
            <div class="text-4xl md:text-5xl font-bold mb-4">0 ₽</div>
            <p class="text-blue-100 uppercase text-xs font-bold tracking-widest">Бесплатный пилот</p>
          </div>
          <div class="p-10 bg-slate-800 rounded-3xl border border-slate-700">
            <div class="text-4xl md:text-5xl font-bold text-blue-400 mb-4">2-4 нед</div>
            <p class="text-slate-400 uppercase text-xs font-bold tracking-widest">Срок запуска</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="py-24 bg-white">
      <div class="container mx-auto px-6">
        <h2 class="text-4xl font-bold mb-16 text-center italic">Свяжитесь с нами</h2>
        <div class="grid md:grid-cols-3 gap-10 max-w-5xl mx-auto">
          <div class="bg-slate-50 p-8 rounded-[2.5rem] border border-slate-100 text-center hover:shadow-2xl transition group">
            <div class="w-16 h-16 bg-blue-100 rounded-2xl flex items-center justify-center mx-auto mb-6 group-hover:bg-blue-600 transition">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-600 group-hover:text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <a href="mailto:info@neuroinspector.ru" class="text-lg md:text-xl font-bold text-slate-800 break-words">info@neuroinspector.ru</a>
          </div>

          <div class="bg-slate-50 p-8 rounded-[2.5rem] border border-slate-100 text-center hover:shadow-2xl transition group">
            <div class="w-16 h-16 bg-blue-100 rounded-2xl flex items-center justify-center mx-auto mb-6 group-hover:bg-blue-600 transition">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-600 group-hover:text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
              </svg>
            </div>
            <a href="tel:+78000000000" class="text-lg md:text-xl font-bold text-slate-800">+7 (800) 000-00-00</a>
          </div>

          <div class="bg-slate-50 p-8 rounded-[2.5rem] border border-slate-100 text-center hover:shadow-2xl transition group">
            <div class="w-16 h-16 bg-sky-100 rounded-2xl flex items-center justify-center mx-auto mb-6 group-hover:bg-sky-500 transition">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-sky-500 group-hover:text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm4.462 8.249c.235 2.268-1.29 10.718-2.112 11.816-.33.44-.763.441-1.226.041-1.209-1.047-3.411-2.924-4.227-3.606-.694-.582-.249-1.037.128-1.385.253-.234 3.197-2.934 3.738-3.46.216-.211.236-.319.108-.432-.128-.113-.369-.071-.563.003-1.025.394-3.52 1.956-4.512 2.624-.657.443-1.364.632-2.12.569-.757-.063-1.503-.312-2.091-.531-.41-.153-.736-.234-.702-.54.017-.159.232-.323.645-.492 2.541-1.103 6.136-2.522 10.75-4.218 1.077-.395 1.954-.153 2.147.111z"/>
              </svg>
            </div>
            <a href="#" class="text-lg md:text-xl font-bold text-slate-800">@neuro_inspector</a>
          </div>
        </div>
      </div>
    </section>

    <footer class="bg-slate-900 text-slate-500 py-12 border-t border-slate-800 text-center">
      <div class="container mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="font-bold text-slate-300 uppercase tracking-widest">ООО «НЕЙРОИНСПЕКТОР»</div>
        <div class="text-sm">Все права защищены &copy; 2026</div>
      </div>
    </footer>
  </div>
</template>

<script setup>
const scrollToContact = () => {
  document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' });
};
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};
</script>

<style>
html { scroll-behavior: smooth; }

@keyframes pulse-slow {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.05); opacity: 0.9; }
}
.animate-pulse-slow { animation: pulse-slow 3s infinite ease-in-out; }

.text-shadow-sm {
  text-shadow: 0 1px 2px rgba(0,0,0,0.05);
}
</style>