<template>
  <div id="top" class="min-h-screen bg-slate-50 text-slate-900 font-sans scroll-smooth">
    <header class="bg-white/90 backdrop-blur-md border-b sticky top-0 z-50">
      <div class="container mx-auto px-4 md:px-6 py-4 flex justify-between items-center">
        <div @click="scrollToTop" class="text-xl md:text-2xl font-bold text-blue-700 tracking-tight uppercase cursor-pointer hover:opacity-80 transition">
          Нейроинспектор
        </div>
        <nav class="hidden xl:flex space-x-6 font-medium text-[11px] uppercase tracking-wider">
          <a href="#problems" class="hover:text-blue-600 transition text-slate-600">Проблемы</a>
          <a href="#capabilities" class="hover:text-blue-600 transition text-slate-600">Возможности</a>
          <a href="#setup" class="hover:text-blue-600 transition text-slate-600">Настройка</a>
          <a href="#integration" class="hover:text-blue-600 transition text-slate-600">IT-Контур</a>
          <a href="#economy" class="hover:text-blue-600 transition text-slate-600">Экономика</a>
          <a href="#pilot" class="hover:text-blue-600 transition text-slate-600">Пилот</a>
        </nav>
        <button @click="scrollToContact" class="bg-blue-600 text-white px-5 py-2.5 rounded-lg hover:bg-blue-700 transition font-bold text-sm shadow-lg shadow-blue-200 uppercase">
          Запустить пилот
        </button>
      </div>
    </header>

    <section class="relative bg-slate-900 text-white py-20 lg:py-32 overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute inset-0" style="background-image: radial-gradient(#3b82f6 1px, transparent 1px); background-size: 40px 40px;"></div>
      </div>
      <div class="container mx-auto px-6 relative z-10">
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <div>
            <h1 class="text-4xl md:text-5xl lg:text-7xl font-extrabold mb-8 leading-[1.1]">
              Интеллектуальный <br> <span class="text-blue-500">контроль брака</span>
            </h1>
            <p class="text-lg md:text-xl text-slate-400 mb-10 leading-relaxed max-w-xl">
              Система компьютерного зрения для автоматизации контроля качества на скоростях до 120 FPS с точностью детекции 98%+.
            </p>
            <div class="flex flex-col sm:flex-row gap-4">
              <button @click="scrollToContact" class="bg-blue-600 px-8 py-4 rounded-xl font-bold text-lg hover:bg-blue-500 transition-all shadow-xl shadow-blue-900/40">
                Внедрить пилот бесплатно
              </button>
              <div class="flex items-center gap-4 px-6 py-4 bg-slate-800/50 rounded-xl border border-slate-700">
                <div class="text-blue-400 font-bold text-2xl">2-4</div>
                <div class="text-slate-400 text-xs leading-tight uppercase font-semibold">Недели на<br>внедрение</div>
              </div>
            </div>
          </div>
          <div class="relative mt-12 lg:mt-0">
            <div class="rounded-3xl overflow-hidden border-[12px] border-slate-800 shadow-2xl relative bg-slate-800">
              <img src="/images/factory-line.png" alt="Промышленная линия" class="w-full opacity-80" />
              <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-48 h-48 border-2 border-blue-500/50 rounded-full animate-ping"></div>
              <div class="absolute bottom-6 left-6 bg-slate-900/90 backdrop-blur-xl p-5 rounded-2xl border border-blue-500/30">
                <div class="text-3xl font-black text-blue-500 leading-none">98.7%</div>
                <div class="text-[10px] text-slate-300 uppercase font-bold tracking-widest mt-1">Accuracy Score</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="problems" class="py-24 bg-white border-b">
      <div class="container mx-auto px-6">
        <div class="text-center max-w-3xl mx-auto mb-20">
          <h2 class="text-3xl md:text-4xl font-bold mb-6 italic text-slate-900">Почему ручной контроль — <span class="text-blue-600">это убытки?</span></h2>
          <p class="text-slate-500 text-lg md:text-xl">Человеческий фактор на высоких скоростях линии неизбежно приводит к финансовым и репутационным потерям.</p>
        </div>
        <div class="grid md:grid-cols-3 gap-10 mb-20">
          <div v-for="(problem, i) in problems" :key="i" class="group p-10 bg-slate-50 rounded-[2.5rem] border border-transparent hover:border-blue-200 hover:bg-white hover:shadow-2xl transition-all duration-500">
            <div class="w-16 h-16 bg-blue-600/10 rounded-2xl flex items-center justify-center mb-8 group-hover:bg-blue-600 group-hover:text-white transition-colors">
              <component :is="problem.icon" class="w-8 h-8 text-blue-600 group-hover:text-white" />
            </div>
            <h3 class="text-2xl font-bold mb-4 text-slate-800 uppercase tracking-tight">{{ problem.title }}</h3>
            <p class="text-slate-600 text-lg leading-relaxed">{{ problem.text }}</p>
          </div>
        </div>

        <div class="bg-slate-900 rounded-[3rem] p-8 md:p-16 text-white overflow-hidden relative">
          <div class="grid lg:grid-cols-2 gap-16 items-center relative z-10">
            <div>
              <h2 class="text-3xl md:text-4xl font-bold mb-8 italic text-blue-400">Сколько это стоит заводу?</h2>
              <div class="space-y-8">
                <div class="flex items-center gap-6 border-b border-slate-700 pb-6">
                  <div class="text-blue-500 text-3xl md:text-4xl font-bold">80 000</div>
                  <div class="text-slate-300 text-lg uppercase font-bold tracking-tighter">единиц продукции в сутки</div>
                </div>
                <div class="flex items-center gap-6 border-b border-slate-700 pb-6">
                  <div class="text-blue-500 text-3xl md:text-4xl font-bold">1.6 млн ₽</div>
                  <div class="text-slate-300 text-lg uppercase font-bold tracking-tighter">прямых потерь в месяц</div>
                </div>
                <p class="text-slate-400 italic text-lg leading-relaxed border-l-2 border-blue-600 pl-4">
                  "Даже снижение брака на 0,3% окупает внедрение системы за 2-4 месяца эксплуатации."
                </p>
              </div>
            </div>
            <div class="bg-slate-800 p-8 md:p-12 rounded-[2.5rem] border border-slate-700 shadow-2xl">
              <h4 class="text-blue-400 font-bold mb-8 uppercase tracking-widest text-xs">Пример расчета (Типовой FMCG-завод)</h4>
              <div class="space-y-6">
                <div class="flex justify-between items-center text-lg">
                  <span class="text-slate-400">Потери в день:</span>
                  <span class="font-bold">16 000 — 56 000 ₽</span>
                </div>
                <div class="flex justify-between items-center text-xl md:text-2xl border-t border-slate-700 pt-6">
                  <span class="text-slate-400">Потери в месяц:</span>
                  <span class="font-bold text-blue-400">0.5 — 1.6 млн ₽</span>
                </div>
                <div class="mt-8 p-6 bg-blue-600 rounded-2xl text-center shadow-lg shadow-blue-600/20">
                  <span class="text-lg font-bold uppercase tracking-tight">Окупаемость: 2-4 месяца</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="capabilities" class="py-24 bg-slate-50">
      <div class="container mx-auto px-6">
        <h2 class="text-3xl md:text-4xl font-bold mb-16 text-center italic">Что именно находит <span class="text-blue-600">НейроИнспектор?</span></h2>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-6">
          <div v-for="defect in defects" :key="defect.name" class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200 hover:shadow-md transition">
            <div class="w-10 h-10 bg-slate-100 rounded-lg flex items-center justify-center mb-4">
              <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
            </div>
            <div class="font-bold text-slate-800 text-lg leading-snug">{{ defect.name }}</div>
          </div>
        </div>
      </div>
    </section>

    <section id="setup" class="py-24 bg-white border-y">
      <div class="container mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl md:text-4xl font-bold mb-4 italic">Настройка и <span class="text-blue-600">обучение</span></h2>
          <p class="text-slate-500 text-lg">Гибкое управление ИИ и создание моделей за 15 минут</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-16 items-center mb-24">
          <div class="rounded-3xl overflow-hidden shadow-2xl border border-slate-300 bg-white p-2">
            <img src="/images/setup-screen.png" alt="Интерфейс настройки" class="w-full rounded-2xl" />
          </div>
          <div class="space-y-6">
            <h3 class="text-2xl font-bold mb-6 text-slate-800 uppercase tracking-tight">Параметры детекции</h3>
            <div class="grid gap-4">
              <div v-for="block in setupBlocks" :key="block.color" :class="`p-5 bg-white rounded-xl border-l-4 ${block.borderClass} shadow-sm`">
                <p class="text-lg leading-relaxed"><span :class="`font-bold uppercase text-xs block mb-1 ${block.textClass}`">{{ block.label }}:</span> {{ block.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <div class="order-2 lg:order-1">
            <h3 class="text-3xl font-bold mb-6 italic text-slate-800">Обучение через эталоны</h3>
            <p class="text-slate-600 mb-8 text-lg leading-relaxed">
              Система самостоятельно строит математическую модель «идеального продукта». Для запуска точной модели достаточно от 10 эталонных снимков.
            </p>
            <div class="grid grid-cols-3 gap-4">
              <div v-for="feat in trainingFeatures" :key="feat.title" class="bg-blue-50 p-4 rounded-2xl text-center border border-blue-100">
                <div class="font-bold text-blue-600 mb-1 uppercase text-[10px] tracking-widest">{{ feat.title }}</div>
                <div class="text-xs text-slate-500">{{ feat.desc }}</div>
              </div>
            </div>
          </div>
          <div class="order-1 lg:order-2 rounded-3xl overflow-hidden shadow-2xl border p-2 bg-slate-50">
            <img src="/images/training-ui.png" alt="Обучение ИИ" class="w-full rounded-2xl" />
          </div>
        </div>
      </div>
    </section>

    <section id="integration" class="py-24 bg-slate-900 text-white relative">
      <div class="container mx-auto px-6 relative z-10">
        <div class="text-center mb-20">
          <h2 class="text-3xl md:text-4xl font-bold mb-6 italic">Безопасная интеграция в <span class="text-blue-500">ИТ-ландшафт</span></h2>
          <p class="text-slate-400 text-lg max-w-2xl mx-auto">Мы понимаем требования промышленной безопасности. Система адаптируется под любые регламенты данных.</p>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-12">
          <div class="grid gap-6">
            <div class="bg-slate-800 p-8 rounded-3xl border border-slate-700 hover:border-blue-500/50 transition">
              <div class="flex items-start gap-6">
                <div class="w-14 h-14 bg-blue-600/20 rounded-2xl flex items-center justify-center shrink-0">
                  <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" /></svg>
                </div>
                <div>
                  <h4 class="text-2xl font-bold mb-2 uppercase tracking-tighter">On-Premise / Локально</h4>
                  <p class="text-slate-400 leading-relaxed text-lg">
                    Максимальная безопасность: все вычисления происходят на сервере внутри вашей сети. Видеопоток не покидает периметр завода, обеспечивая полную изоляцию данных.
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-slate-800 p-8 rounded-3xl border border-slate-700 hover:border-blue-500/50 transition">
              <div class="flex items-start gap-6">
                <div class="w-14 h-14 bg-blue-600/20 rounded-2xl flex items-center justify-center shrink-0">
                  <svg class="w-8 h-8 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 01-2-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" /></svg>
                </div>
                <div>
                  <h4 class="text-2xl font-bold mb-2 uppercase tracking-tighter">Cloud / Облако</h4>
                  <p class="text-slate-400 leading-relaxed text-lg">
                    Устанавливается камера, данные через шифратор передаются в наш защищенный ЦОД. Нейросеть обрабатывает поток и возвращает сигнал на шифратор для мгновенной реакции линии.
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-blue-900/30 p-6 rounded-2xl border-l-4 border-blue-500">
              <div class="flex items-center gap-4">
                <div class="text-blue-500 font-bold uppercase text-xs tracking-widest">Система уведомлений:</div>
                <p class="text-slate-300 text-sm">Результаты обработки мгновенно транслируются в систему управления для оператора и записи в базу событий.</p>
              </div>
            </div>
          </div>
          <div class="bg-blue-600 rounded-[2.5rem] p-10 flex flex-col justify-center items-center text-center overflow-hidden relative shadow-2xl">
            <div class="relative z-10">
              <div class="text-7xl font-black mb-4">100%</div>
              <div class="text-xl font-bold uppercase tracking-widest mb-6">Владение данными</div>
              <p class="text-blue-100 text-lg opacity-90 max-w-sm">
                Согласно регламенту, все собранные данные и статистика являются исключительной собственностью Заказчика.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="economy" class="py-24 bg-white">
      <div class="container mx-auto px-6">
        <h2 class="text-3xl font-bold mb-16 text-center italic uppercase tracking-widest">Экономика внедрения</h2>
        <div class="grid md:grid-cols-3 gap-8 text-center max-w-5xl mx-auto">
          <div class="p-12 bg-slate-50 rounded-[3rem] border border-slate-100 transition-all hover:shadow-2xl hover:-translate-y-2">
            <div class="text-4xl md:text-5xl font-bold text-blue-600 mb-4">1.6 млн ₽</div>
            <p class="text-slate-500 uppercase text-xs font-bold tracking-widest">Средняя экономия в месяц</p>
          </div>
          <div class="p-12 bg-blue-600 text-white rounded-[3rem] shadow-2xl md:scale-110 z-10 relative">
             <div class="absolute -top-4 left-1/2 -translate-x-1/2 bg-yellow-400 text-slate-900 px-4 py-1 rounded-full text-xs font-black uppercase">Выгодно</div>
            <div class="text-4xl md:text-5xl font-bold mb-4">0 ₽</div>
            <p class="text-blue-100 uppercase text-xs font-bold tracking-widest">Бесплатный пилотный проект</p>
          </div>
          <div class="p-12 bg-slate-50 rounded-[3rem] border border-slate-100 transition-all hover:shadow-2xl hover:-translate-y-2">
            <div class="text-4xl md:text-5xl font-bold text-blue-600 mb-4">6-12 мес</div>
            <p class="text-slate-500 uppercase text-xs font-bold tracking-widest">Полная окупаемость (ROI)</p>
          </div>
        </div>
      </div>
    </section>

    <section id="pilot" class="py-24 bg-slate-50 border-y">
      <div class="container mx-auto px-6 text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-6 italic">Как проходит <span class="text-blue-600">Пилотный проект?</span></h2>
        <p class="text-slate-500 text-lg mb-16 max-w-2xl mx-auto italic">«Если система не дает измеримого эффекта — вы ничего не платите»</p>
        <div class="grid md:grid-cols-4 gap-6 text-left">
          <div v-for="(step, i) in pilotSteps" :key="i" class="bg-white p-8 rounded-3xl border border-slate-200 relative group hover:border-blue-500 transition-all">
            <div class="text-blue-600 font-black text-5xl opacity-10 absolute top-4 right-6 group-hover:opacity-20 transition-opacity">{{ i + 1 }}</div>
            <h5 class="font-bold text-xl mb-3 text-slate-800">{{ step.title }}</h5>
            <p class="text-slate-500 text-sm leading-relaxed">{{ step.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="py-24 bg-white overflow-hidden relative">
      <div class="container mx-auto px-6 relative z-10">
        <div class="max-w-4xl mx-auto bg-slate-900 rounded-[3rem] p-12 md:p-20 text-center text-white shadow-2xl shadow-blue-900/20">
          <h2 class="text-3xl md:text-5xl font-bold mb-8 italic">Готовы оцифровать качество?</h2>
          <p class="text-slate-400 text-lg md:text-xl mb-12">Оставьте заявку на бесплатный пилот на вашу производственную линию.</p>
          <div class="flex flex-col md:flex-row gap-6 justify-center">
             <a href="mailto:info@neuroinspector.ru" class="bg-blue-600 px-10 py-5 rounded-2xl font-bold text-xl hover:bg-blue-500 transition shadow-lg shadow-blue-900/40">info@neuroinspector.ru</a>
             <a href="tel:+78000000000" class="bg-slate-800 px-10 py-5 rounded-2xl font-bold text-xl hover:bg-slate-700 transition border border-slate-700">+7 (800) 000-00-00</a>
          </div>
        </div>
      </div>
    </section>

    <footer class="bg-slate-900 text-slate-500 py-16 text-center border-t border-slate-800">
      <div class="container mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-8">
        <div class="text-left">
          <div class="text-sm font-bold text-slate-400 uppercase tracking-widest">ООО «НЕЙРОИНСПЕКТР»</div>
        </div>
        <div class="text-sm opacity-50">&copy; 2026 Все права защищены.</div>
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
  { title: "Оценка ROI", desc: "Через 1-2 месяца совместно считаем реальную экономию и принимаем решение о масштабировании." }
];

const scrollToContact = () => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' });
const scrollToTop = () => window.scrollTo({ top: 0, behavior: 'smooth' });
</script>

<style>
html { scroll-behavior: smooth; }
@keyframes pulse-slow {
  0%, 100% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.05); opacity: 0.8; }
}
.animate-pulse-slow { animation: pulse-slow 3s infinite ease-in-out; }
</style>