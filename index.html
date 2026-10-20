import React, { useState, useEffect, useRef } from 'react';
import { 
  BookOpen, 
  MessageSquare, 
  Bot, 
  CheckCircle2, 
  GraduationCap, 
  Volume2, 
  ChevronRight, 
  Sparkles, 
  RotateCcw, 
  Award, 
  Send, 
  User, 
  Check, 
  X, 
  HelpCircle,
  Play,
  Flame,
  BarChart3,
  Lightbulb,
  ArrowRight,
  Layers,
  VolumeX
} from 'lucide-react';

// Main App Component
export default function App() {
  const [activeTab, setActiveTab] = useState('grammar');
  const [progress, setProgress] = useState({
    completedGrammar: [],
    quizScores: {},
    passedExam: false,
    streak: 3
  });

  // Load progress from local storage
  useEffect(() => {
    const saved = localStorage.getItem('german_a1_progress');
    if (saved) {
      try {
        setProgress(JSON.parse(saved));
      } catch (e) {
        console.error('Error loading saved progress', e);
      }
    }
  }, []);

  // Save progress
  const saveProgress = (newProgress) => {
    setProgress(newProgress);
    localStorage.setItem('german_a1_progress', JSON.stringify(newProgress));
  };

  // Helper function for Speech Synthesis
  const speakGerman = (text) => {
    if ('speechSynthesis' in window) {
      window.speechSynthesis.cancel(); // Stop ongoing speech
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = 'de-DE';
      utterance.rate = 0.85; // Slightly slower for A1 learners
      window.speechSynthesis.speak(utterance);
    } else {
      alert('عذراً، ميزة النطق الصوتي غير مدعومة في متصفحك.');
    }
  };

  return (
    <div dir="rtl" className="min-h-screen bg-slate-50 text-slate-800 font-sans flex flex-col selection:bg-amber-100 selection:text-amber-900">
      {/* Header */}
      <header className="bg-gradient-to-r from-amber-600 via-red-600 to-slate-900 text-white shadow-lg sticky top-0 z-50">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3 flex justify-between items-center">
          <div className="flex items-center gap-3">
            <div className="w-10 h-10 rounded-xl bg-white/10 backdrop-blur-md flex items-center justify-center border border-white/20 text-xl font-bold shadow-inner">
              🇩🇪
            </div>
            <div>
              <h1 className="text-xl sm:text-2xl font-black tracking-tight leading-none flex items-center gap-2">
                Deutsch A1 <span className="text-xs font-semibold px-2 py-0.5 bg-amber-400 text-slate-950 rounded-full">بالعربي</span>
              </h1>
              <p className="text-xs text-slate-200 mt-1 font-medium">طريقك الذهبي لاجتياز مستوى A1 بسهولة</p>
            </div>
          </div>

          <div className="flex items-center gap-4">
            {/* Streak Counter */}
            <div className="hidden sm:flex items-center gap-1.5 bg-white/10 backdrop-blur-md px-3 py-1.5 rounded-full border border-white/15 text-xs font-bold">
              <Flame className="w-4 h-4 text-amber-400 fill-amber-400 animate-pulse" />
              <span>{progress.streak} أيام حماس!</span>
            </div>

            {/* Progress Badge */}
            <div className="flex items-center gap-2 bg-slate-900/40 backdrop-blur-md px-3 py-1.5 rounded-full border border-white/15 text-xs">
              <BarChart3 className="w-4 h-4 text-emerald-400" />
              <span className="font-semibold hidden md:inline">الإنجاز:</span>
              <span className="font-bold text-amber-300">
                {Math.round((progress.completedGrammar.length / 6) * 100)}%
              </span>
            </div>
          </div>
        </div>

        {/* Navigation Tabs */}
        <nav className="bg-slate-900/90 backdrop-blur-md border-t border-white/10 px-2 sm:px-6 overflow-x-auto scrollbar-none">
          <div className="max-w-7xl mx-auto flex gap-1 sm:gap-2 py-2">
            {[
              { id: 'grammar', label: 'القواعد الأساسية', icon: BookOpen },
              { id: 'phrases', label: 'الجمل والعبارات', icon: MessageSquare },
              { id: 'ai-tutor', label: 'المعلم الذكي AI', icon: Bot, badge: 'جديد' },
              { id: 'exercises', label: 'التدريبات والتمارين', icon: Layers },
              { id: 'exam', label: 'الامتحان النهائي', icon: GraduationCap }
            ].map((tab) => {
              const Icon = tab.icon;
              const isActive = activeTab === tab.id;
              return (
                <button
                  key={tab.id}
                  onClick={() => setActiveTab(tab.id)}
                  className={`flex items-center gap-2 px-3 sm:px-4 py-2 rounded-xl text-xs sm:text-sm font-bold whitespace-nowrap transition-all duration-200 relative ${
                    isActive
                      ? 'bg-amber-500 text-slate-950 shadow-md shadow-amber-500/20 scale-105'
                      : 'text-slate-300 hover:text-white hover:bg-white/10'
                  }`}
                >
                  <Icon className={`w-4 h-4 ${isActive ? 'text-slate-950' : 'text-slate-400'}`} />
                  <span>{tab.label}</span>
                  {tab.badge && (
                    <span className="text-[10px] bg-red-500 text-white px-1.5 py-0.2 rounded-full font-extrabold animate-bounce">
                      {tab.badge}
                    </span>
                  )}
                </button>
              );
            })}
          </div>
        </nav>
      </header>

      {/* Main Content Area */}
      <main className="flex-1 max-w-7xl w-full mx-auto p-4 sm:p-6 lg:p-8">
        {activeTab === 'grammar' && (
          <GrammarSection 
            progress={progress} 
            saveProgress={saveProgress} 
            speak={speakGerman} 
          />
        )}
        {activeTab === 'phrases' && <PhrasesSection speak={speakGerman} />}
        {activeTab === 'ai-tutor' && <AITutorSection speak={speakGerman} />}
        {activeTab === 'exercises' && <ExercisesSection speak={speakGerman} />}
        {activeTab === 'exam' && (
          <ExamSection 
            progress={progress} 
            saveProgress={saveProgress} 
            speak={speakGerman} 
          />
        )}
      </main>

      {/* Footer */}
      <footer className="bg-slate-900 text-slate-400 py-6 border-t border-slate-800 mt-auto text-center text-xs sm:text-sm">
        <div className="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row justify-between items-center gap-3">
          <p>❤️ منصة تعلم ألماني A1 بالتفاعل والذكاء الاصطناعي - مخصصة للناطقين بالعربية</p>
          <p className="text-slate-500">Viel Erfolg beim Lernen! بالتوفيق في رحلتك الدراسية</p>
        </div>
      </footer>
    </div>
  );
}

// ==========================================
// 1. GRAMMAR SECTION (القواعد الأساسية)
// ==========================================
function GrammarSection({ progress, saveProgress, speak }) {
  const [selectedTopic, setSelectedTopic] = useState(0);

  const grammarTopics = [
    {
      id: 'alphabet',
      title: '1. الأبجدية والنطق الصحيح (Das Alphabet)',
      desc: 'تعلم كيف تنطق الحروف الألمانية مع الأصوات الخاصة مثل Ä, Ö, Ü و ß',
      content: (
        <div className="space-y-6">
          <div className="p-4 bg-amber-50 rounded-2xl border border-amber-200 text-amber-900">
            <h4 className="font-bold mb-1 flex items-center gap-2">
              <Lightbulb className="w-5 h-5 text-amber-600" /> معلومة ذهبية للمبتدئين:
            </h4>
            <p className="text-sm">اللغة الألمانية تُكتب كما تُنطق بنسبة كبيرة! تعلم قواعد الحروف المركبة وسيصبح نطق أي كلمة سهلاً جداً.</p>
          </div>

          <h4 className="font-bold text-slate-800 text-base">الحروف الخاصة (Umlaute & Eszett):</h4>
          <div className="grid grid-cols-2 sm:grid-cols-4 gap-3">
            {[
              { char: 'Ä ä', sound: 'مثل e في كلمة Red', ex: 'Äpfel', tr: 'تفاح' },
              { char: 'Ö ö', sound: 'ضم الشفتين ونطق e', ex: 'Öl', tr: 'زيت' },
              { char: 'Ü ü', sound: 'ضم الشفتين ونطق i', ex: 'Über', tr: 'عبر/فوق' },
              { char: 'ß', sound: 's مشددة (Eszett)', ex: 'Straße', tr: 'شارع' }
            ].map((item, idx) => (
              <div key={idx} className="p-3 bg-white border border-slate-200 rounded-xl hover:shadow-md transition">
                <div className="flex justify-between items-center mb-1">
                  <span className="text-2xl font-black text-amber-600">{item.char}</span>
                  <button onClick={() => speak(item.ex)} className="p-1 text-slate-400 hover:text-amber-600">
                    <Volume2 className="w-5 h-5" />
                  </button>
                </div>
                <p className="text-xs text-slate-500 mb-2">{item.sound}</p>
                <div className="text-xs font-semibold bg-slate-50 p-1.5 rounded flex justify-between">
                  <span>{item.ex}</span>
                  <span className="text-slate-400">({item.tr})</span>
                </div>
              </div>
            ))}
          </div>

          <h4 className="font-bold text-slate-800 text-base mt-4">تركيبات الحروف الهامة (Vokalverbindungen):</h4>
          <div className="space-y-2">
            {[
              { combination: 'ei', sound: 'تُنطق مثل "أي" (like My)', ex: 'Nein', tr: 'لا' },
              { combination: 'ie', sound: 'تُنطق "إي" ممدودة (like Bee)', ex: 'Sie', tr: 'حضرتك / هم' },
              { combination: 'eu / äu', sound: 'تُنطق "أوي" (like Boy)', ex: 'Neu', tr: 'جديد' },
              { combination: 'sch', sound: 'تُنطق "ش" صريحة', ex: 'Schule', tr: 'مدرسة' },
              { combination: 'st / sp', sound: 'تُنطق "شت" / "شب" في أول الكلمة', ex: 'Sprechen', tr: 'يتحدث' }
            ].map((rule, idx) => (
              <div key={idx} className="flex items-center justify-between p-3 bg-white border border-slate-200 rounded-xl">
                <div>
                  <span className="font-bold text-red-600 text-sm ml-2">[{rule.combination}]</span>
                  <span className="text-xs text-slate-600">{rule.sound}</span>
                </div>
                <button 
                  onClick={() => speak(rule.ex)} 
                  className="flex items-center gap-2 bg-slate-100 hover:bg-amber-100 text-slate-800 px-3 py-1 rounded-lg text-xs font-semibold transition"
                >
                  <span>مثال: {rule.ex} ({rule.tr})</span>
                  <Volume2 className="w-4 h-4 text-amber-600" />
                </button>
              </div>
            ))}
          </div>
        </div>
      )
    },
    {
      id: 'articles',
      title: '2. أدوات التعريف والتنكير (Artikel)',
      desc: 'فهم جنس الأسماء في الألمانية: المذكر (der)، المؤنث (die)، المحايد (das)، والجمع (die)',
      content: (
        <div className="space-y-6">
          <p className="text-sm text-slate-600 leading-relaxed">
            في اللغة الألمانية، لكل اسم جنس خاص به ولا يعتمد بالضرورة على المعنى الحقيقي بل هو مجرد تصنيف جراماتيكي. يجب حفظ كل كلمة بأداتها!
          </p>

          <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
            <div className="bg-blue-50 border border-blue-200 rounded-2xl p-4">
              <span className="text-xs font-bold text-blue-600 bg-blue-100 px-2 py-0.5 rounded-full">مذكر (Maskulin)</span>
              <h4 className="text-2xl font-black text-blue-700 my-2">der</h4>
              <p className="text-xs text-slate-600 mb-3">النكرة: <span className="font-bold">ein</span> | النفي: <span className="font-bold">kein</span></p>
              <div className="space-y-1 text-xs">
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('der Mann')}>
                  <span>der Mann</span> <span className="text-slate-400">الرجل</span>
                </div>
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('der Tisch')}>
                  <span>der Tisch</span> <span className="text-slate-400">الطاولة</span>
                </div>
              </div>
            </div>

            <div className="bg-emerald-50 border border-emerald-200 rounded-2xl p-4">
              <span className="text-xs font-bold text-emerald-600 bg-emerald-100 px-2 py-0.5 rounded-full">محايد (Neutral)</span>
              <h4 className="text-2xl font-black text-emerald-700 my-2">das</h4>
              <p className="text-xs text-slate-600 mb-3">النكرة: <span className="font-bold">ein</span> | النفي: <span className="font-bold">kein</span></p>
              <div className="space-y-1 text-xs">
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('das Kind')}>
                  <span>das Kind</span> <span className="text-slate-400">الطفل</span>
                </div>
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('das Buch')}>
                  <span>das Buch</span> <span className="text-slate-400">الكتاب</span>
                </div>
              </div>
            </div>

            <div className="bg-pink-50 border border-pink-200 rounded-2xl p-4">
              <span className="text-xs font-bold text-pink-600 bg-pink-100 px-2 py-0.5 rounded-full">مؤنث (Feminin) / الجمع</span>
              <h4 className="text-2xl font-black text-pink-700 my-2">die</h4>
              <p className="text-xs text-slate-600 mb-3">النكرة: <span className="font-bold">eine</span> | النفي: <span className="font-bold">keine</span></p>
              <div className="space-y-1 text-xs">
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('die Frau')}>
                  <span>die Frau</span> <span className="text-slate-400">المرأة</span>
                </div>
                <div className="flex justify-between p-1 bg-white rounded cursor-pointer" onClick={() => speak('die Kinder')}>
                  <span>die Kinder (جمع)</span> <span className="text-slate-400">الأطفال</span>
                </div>
              </div>
            </div>
          </div>

          <div className="p-4 bg-slate-100 rounded-2xl border border-slate-200 text-xs space-y-2">
            <h5 className="font-bold text-slate-800">💡 نصيحة ذهبية لمعرفة الأداة:</h5>
            <ul className="list-disc list-inside space-y-1 text-slate-600">
              <li>الكلمات التي تنتهي بـ <span className="font-bold text-red-600">-ung, -heit, -keit, -schaft, -ei</span> تكون دائمًا مؤنث <span className="font-bold">(die)</span>.</li>
              <li>الكلمات التي تنتهي بـ <span className="font-bold text-red-600">-chen, -lein</span> (التصغير) تكون دائمًا محايد <span className="font-bold">(das)</span>.</li>
            </ul>
          </div>
        </div>
      )
    },
    {
      id: 'verbs',
      title: '3. تصريف الأفعال في المضارع (Verbkonjugation)',
      desc: 'كيف تصرف الأفعال العادية والشاذة وأهم أفعال A1 مثل sein و haben',
      content: (
        <div className="space-y-6">
          <p className="text-sm text-slate-600">
            يتغير آخر الفعل في الألمانية حسب الضمير. نحذف الـ <span className="font-bold text-red-600">-en</span> من نهاية مصدر الفعل ونضيف النهايات المخصصة.
          </p>

          {/* Endings summary */}
          <div className="bg-slate-900 text-white p-4 rounded-2xl">
            <h4 className="font-bold text-amber-400 text-sm mb-3">نهايات تصريف الأفعال المنتظمة:</h4>
            <div className="grid grid-cols-2 sm:grid-cols-4 gap-2 text-xs">
              <div className="bg-slate-800 p-2 rounded">ich → <span className="text-amber-300 font-bold">-e</span></div>
              <div className="bg-slate-800 p-2 rounded">du → <span className="text-amber-300 font-bold">-st</span></div>
              <div className="bg-slate-800 p-2 rounded">er/sie/es → <span className="text-amber-300 font-bold">-t</span></div>
              <div className="bg-slate-800 p-2 rounded">wir → <span className="text-amber-300 font-bold">-en</span></div>
              <div className="bg-slate-800 p-2 rounded">ihr → <span className="text-amber-300 font-bold">-t</span></div>
              <div className="bg-slate-800 p-2 rounded">sie/Sie → <span className="text-amber-300 font-bold">-en</span></div>
            </div>
          </div>

          <h4 className="font-bold text-slate-800">أهم فعلين في اللغة الألمانية (مهمين جداً للحفظ):</h4>
          <div className="grid grid-cols-1 sm:grid-cols-2 gap-4">
            {/* Sein */}
            <div className="border border-slate-200 rounded-2xl p-4 bg-white shadow-sm">
              <div className="flex justify-between items-center mb-3">
                <span className="font-bold text-slate-800">فعل يكون (sein)</span>
                <button onClick={() => speak('ich bin, du bist, er ist')} className="text-amber-600 hover:text-amber-700">
                  <Volume2 className="w-5 h-5" />
                </button>
              </div>
              <div className="grid grid-cols-2 gap-2 text-xs">
                <div className="p-1.5 bg-slate-50 rounded">ich <span className="font-bold text-amber-600">bin</span></div>
                <div className="p-1.5 bg-slate-50 rounded">wir <span className="font-bold text-amber-600">sind</span></div>
                <div className="p-1.5 bg-slate-50 rounded">du <span className="font-bold text-amber-600">bist</span></div>
                <div className="p-1.5 bg-slate-50 rounded">ihr <span className="font-bold text-amber-600">seid</span></div>
                <div className="p-1.5 bg-slate-50 rounded">er/sie/es <span className="font-bold text-amber-600">ist</span></div>
                <div className="p-1.5 bg-slate-50 rounded">sie/Sie <span className="font-bold text-amber-600">sind</span></div>
              </div>
            </div>

            {/* Haben */}
            <div className="border border-slate-200 rounded-2xl p-4 bg-white shadow-sm">
              <div className="flex justify-between items-center mb-3">
                <span className="font-bold text-slate-800">فعل يملك (haben)</span>
                <button onClick={() => speak('ich habe, du hast, er hat')} className="text-amber-600 hover:text-amber-700">
                  <Volume2 className="w-5 h-5" />
                </button>
              </div>
              <div className="grid grid-cols-2 gap-2 text-xs">
                <div className="p-1.5 bg-slate-50 rounded">ich <span className="font-bold text-emerald-600">habe</span></div>
                <div className="p-1.5 bg-slate-50 rounded">wir <span className="font-bold text-emerald-600">haben</span></div>
                <div className="p-1.5 bg-slate-50 rounded">du <span className="font-bold text-emerald-600">hast</span></div>
                <div className="p-1.5 bg-slate-50 rounded">ihr <span className="font-bold text-emerald-600">habt</span></div>
                <div className="p-1.5 bg-slate-50 rounded">er/sie/es <span className="font-bold text-emerald-600">hat</span></div>
                <div className="p-1.5 bg-slate-50 rounded">sie/Sie <span className="font-bold text-emerald-600">haben</span></div>
              </div>
            </div>
          </div>
        </div>
      )
    },
    {
      id: 'sentence',
      title: '4. ترتيب الجملة الألمانية (Satzbau)',
      desc: 'القاعدة الذهبية: الفعل يأتي دائماً في المركز الثاني في الجملة الخبرية!',
      content: (
        <div className="space-y-6">
          <div className="p-4 bg-red-50 border border-red-200 rounded-2xl text-red-900">
            <h4 className="font-bold mb-1 text-sm">⚠️ القاعدة الأهم في الألمانية:</h4>
            <p className="text-xs">
              في الجملة الخبرية العادية، <span className="font-bold underline">الفعل المصرف يأتي دائماً في الموقع رقم 2 (Position 2)</span> مهما تغير باقي عناصر الجملة!
            </p>
          </div>

          <div className="space-y-3">
            <h4 className="font-bold text-slate-800 text-sm">أمثلة لتوضيح الترتيب:</h4>
            <div className="overflow-x-auto">
              <table className="w-full text-xs text-right border-collapse">
                <thead>
                  <tr className="bg-slate-100 text-slate-700 font-bold">
                    <th className="p-2 border">المركز 1 (Position 1)</th>
                    <th className="p-2 border bg-amber-100 text-amber-900">المركز 2 (Verb) 🔴</th>
                    <th className="p-2 border">باقي الجملة</th>
                    <th className="p-2 border">المعنى بالعربية</th>
                  </tr>
                </thead>
                <tbody className="divide-y">
                  <tr className="bg-white">
                    <td className="p-2 border font-semibold">Ich</td>
                    <td className="p-2 border bg-amber-50 font-bold text-amber-600">lerne</td>
                    <td className="p-2 border">heute Deutsch.</td>
                    <td className="p-2 border text-slate-500">أنا أتعلم الألمانية اليوم.</td>
                  </tr>
                  <tr className="bg-white">
                    <td className="p-2 border font-semibold">Heute</td>
                    <td className="p-2 border bg-amber-50 font-bold text-amber-600">lerne</td>
                    <td className="p-2 border">ich Deutsch.</td>
                    <td className="p-2 border text-slate-500">اليوم أتعلم أنا الألمانية. (الفعل ظل ثابتاً في المركز 2)</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <div className="p-4 bg-slate-50 rounded-2xl border border-slate-200">
            <h4 className="font-bold text-slate-800 text-sm mb-2">جملة السؤال (Fragesatz):</h4>
            <p className="text-xs text-slate-600 mb-2">
              1. **سؤال يبدأ بأداة استفهام (W-Frage):** أداة الاستفهام في Pos 1 ، والفعل في Pos 2.<br/>
              <span className="font-mono text-slate-800">Wo <span className="text-amber-600 font-bold">wohnst</span> du?</span> (أين تسكن؟)
            </p>
            <p className="text-xs text-slate-600">
              2. **سؤال إجابته نعم/لا (Ja/Nein-Frage):** يتقدم الفعل ليصبح في **المركز 1**!<br/>
              <span className="font-mono text-slate-800"><span className="text-amber-600 font-bold">Lernst</span> du Deutsch?</span> (هل تتعلم الألمانية؟)
            </p>
          </div>
        </div>
      )
    },
    {
      id: 'negation',
      title: '5. أدوات النفي (nicht / kein)',
      desc: 'متى نستخدم kein ومتى نستخدم nicht بنجاح؟',
      content: (
        <div className="space-y-6">
          <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div className="bg-white p-4 border border-slate-200 rounded-2xl shadow-sm">
              <span className="bg-amber-100 text-amber-800 font-bold px-2 py-0.5 rounded text-xs">استخدام kein</span>
              <h4 className="font-bold text-slate-800 my-2 text-sm">نفي الأسماء التي لها أداة تنكير (أو بدون أداة)</h4>
              <p className="text-xs text-slate-600 mb-3">تستخدم فقط مع الأسماء وتتصرف حسب الجنس.</p>
              <div className="space-y-2 text-xs">
                <div className="p-2 bg-slate-50 rounded flex justify-between">
                  <span>Ich habe <span className="text-red-600 font-bold">kein</span> Auto.</span>
                  <span className="text-slate-400">ليس لدي سيارة</span>
                </div>
                <div className="p-2 bg-slate-50 rounded flex justify-between">
                  <span>Das ist <span className="text-red-600 font-bold">keine</span> Zeit.</span>
                  <span className="text-slate-400">هذا ليس وقتاً</span>
                </div>
              </div>
            </div>

            <div className="bg-white p-4 border border-slate-200 rounded-2xl shadow-sm">
              <span className="bg-blue-100 text-blue-800 font-bold px-2 py-0.5 rounded text-xs">استخدام nicht</span>
              <h4 className="font-bold text-slate-800 my-2 text-sm">نفي الأفعال، الصفات، الأسماء المعرفة، والأسماء العلم</h4>
              <p className="text-xs text-slate-600 mb-3">تستخدم مع باقي الحالات في الجملة.</p>
              <div className="space-y-2 text-xs">
                <div className="p-2 bg-slate-50 rounded flex justify-between">
                  <span>Ich verstehe <span className="text-blue-600 font-bold">nicht</span>.</span>
                  <span className="text-slate-400">أنا لا أفهم (نفي فعل)</span>
                </div>
                <div className="p-2 bg-slate-50 rounded flex justify-between">
                  <span>Das Haus ist <span className="text-blue-600 font-bold">nicht</span> groß.</span>
                  <span className="text-slate-400">البيت ليس كبيراً (نفي صفة)</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      )
    },
    {
      id: 'possessive',
      title: '6. الضمائر الملكية (Possessivpronomen)',
      desc: 'كيف تقول "كتابي"، "سيارتك"، "بيته" بالألمانية؟',
      content: (
        <div className="space-y-6">
          <p className="text-sm text-slate-600">
            تعتمد ملكيتك على الضمير وشكل الاسم المملوك (إذا كان مؤنثاً أو جمعاً نضيف حرف <span className="font-bold text-red-600">-e</span> لنهاية الضمير).
          </p>

          <div className="overflow-x-auto">
            <table className="w-full text-xs text-right border-collapse bg-white border border-slate-200 rounded-xl">
              <thead>
                <tr className="bg-slate-100 font-bold text-slate-700">
                  <th className="p-2.5 border">الضمير الشخصي</th>
                  <th className="p-2.5 border">الضمير الملكي (مذكر / محايد)</th>
                  <th className="p-2.5 border">الضمير الملكي (مؤنث / جمع)</th>
                  <th className="p-2.5 border">مثال</th>
                </tr>
              </thead>
              <tbody className="divide-y text-slate-700">
                <tr>
                  <td className="p-2.5 border font-bold">ich (أنا)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">mein</td>
                  <td className="p-2.5 border text-amber-600 font-bold">meine</td>
                  <td className="p-2.5 border">mein Buch / meine Mutter</td>
                </tr>
                <tr>
                  <td className="p-2.5 border font-bold">du (أنت)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">dein</td>
                  <td className="p-2.5 border text-amber-600 font-bold">deine</td>
                  <td className="p-2.5 border">dein Name / deine Tasche</td>
                </tr>
                <tr>
                  <td className="p-2.5 border font-bold">er / es (هو / محايد)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">sein</td>
                  <td className="p-2.5 border text-amber-600 font-bold">seine</td>
                  <td className="p-2.5 border">sein Vater / seine Schwester</td>
                </tr>
                <tr>
                  <td className="p-2.5 border font-bold">sie (هي)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">ihr</td>
                  <td className="p-2.5 border text-amber-600 font-bold">ihre</td>
                  <td className="p-2.5 border">ihr Kind / ihre Katze</td>
                </tr>
                <tr>
                  <td className="p-2.5 border font-bold">wir (نحن)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">unser</td>
                  <td className="p-2.5 border text-amber-600 font-bold">unsere</td>
                  <td className="p-2.5 border">unser Haus / unsere Familie</td>
                </tr>
                <tr>
                  <td className="p-2.5 border font-bold">Sie (حضرتك)</td>
                  <td className="p-2.5 border text-amber-600 font-bold">Ihr</td>
                  <td className="p-2.5 border text-amber-600 font-bold">Ihre</td>
                  <td className="p-2.5 border">Ihr Pass / Ihre Adresse</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      )
    }
  ];

  const current = grammarTopics[selectedTopic];

  const isCompleted = progress.completedGrammar.includes(current.id);

  const toggleComplete = (id) => {
    let updated = [...progress.completedGrammar];
    if (updated.includes(id)) {
      updated = updated.filter(item => item !== id);
    } else {
      updated.push(id);
    }
    saveProgress({ ...progress, completedGrammar: updated });
  };

  return (
    <div className="grid grid-cols-1 lg:grid-cols-12 gap-6">
      {/* Sidebar Topics */}
      <div className="lg:col-span-4 space-y-2">
        <h3 className="font-bold text-slate-800 text-sm mb-3 flex items-center gap-2">
          <BookOpen className="w-4 h-4 text-amber-600" />
          قائمة دروس قواعد A1:
        </h3>
        {grammarTopics.map((topic, index) => {
          const completed = progress.completedGrammar.includes(topic.id);
          const isSelected = selectedTopic === index;
          return (
            <button
              key={topic.id}
              onClick={() => setSelectedTopic(index)}
              className={`w-full text-right p-3.5 rounded-2xl transition border flex items-center justify-between ${
                isSelected
                  ? 'bg-amber-500 text-slate-950 border-amber-600 font-bold shadow-md'
                  : 'bg-white hover:bg-slate-50 text-slate-700 border-slate-200'
              }`}
            >
              <div className="flex items-center gap-3 overflow-hidden">
                <span className={`w-7 h-7 rounded-full flex items-center justify-center text-xs font-bold shrink-0 ${
                  isSelected ? 'bg-slate-950 text-amber-400' : 'bg-slate-100 text-slate-600'
                }`}>
                  {index + 1}
                </span>
                <span className="text-xs sm:text-sm truncate">{topic.title.split('. ')[1]}</span>
              </div>
              {completed && (
                <CheckCircle2 className={`w-5 h-5 shrink-0 ${isSelected ? 'text-slate-950' : 'text-emerald-500'}`} />
              )}
            </button>
          );
        })}
      </div>

      {/* Main Topic Display */}
      <div className="lg:col-span-8">
        <div className="bg-white border border-slate-200 rounded-3xl p-5 sm:p-7 shadow-sm space-y-6">
          <div className="flex flex-col sm:flex-row justify-between sm:items-center gap-4 pb-4 border-b border-slate-100">
            <div>
              <h2 className="text-lg sm:text-xl font-black text-slate-900">{current.title}</h2>
              <p className="text-xs text-slate-500 mt-1">{current.desc}</p>
            </div>
            <button
              onClick={() => toggleComplete(current.id)}
              className={`flex items-center gap-2 px-4 py-2 rounded-xl text-xs font-bold transition shrink-0 ${
                isCompleted
                  ? 'bg-emerald-100 text-emerald-800 hover:bg-emerald-200'
                  : 'bg-slate-100 text-slate-700 hover:bg-slate-200'
              }`}
            >
              <CheckCircle2 className={`w-4 h-4 ${isCompleted ? 'text-emerald-600' : 'text-slate-400'}`} />
              <span>{isCompleted ? 'تمت المذاكرة' : 'تعليم كـ مكتمل'}</span>
            </button>
          </div>

          {/* Lesson Content Render */}
          {current.content}

          {/* Bottom Navigation between lessons */}
          <div className="flex justify-between items-center pt-6 border-t border-slate-100 text-xs font-bold">
            <button
              disabled={selectedTopic === 0}
              onClick={() => setSelectedTopic(prev => prev - 1)}
              className="px-4 py-2 bg-slate-100 hover:bg-slate-200 disabled:opacity-40 rounded-xl text-slate-700 transition"
            >
              الدرس السابق
            </button>
            <span className="text-slate-400">{selectedTopic + 1} من {grammarTopics.length}</span>
            <button
              disabled={selectedTopic === grammarTopics.length - 1}
              onClick={() => setSelectedTopic(prev => prev + 1)}
              className="px-4 py-2 bg-amber-500 hover:bg-amber-600 disabled:opacity-40 text-slate-950 rounded-xl transition"
            >
              الدرس التالي
            </button>
          </div>
        </div>
      </div>
    </div>
  );
}

// ==========================================
// 2. PHRASES SECTION (الجمل والعبارات اليومية)
// ==========================================
function PhrasesSection({ speak }) {
  const [activeCategory, setActiveCategory] = useState('greetings');

  const categories = [
    { id: 'greetings', name: 'التحيات والتعارف' },
    { id: 'daily', name: 'المحادثات اليومية' },
    { id: 'shopping', name: 'التسوق والمطعم' },
    { id: 'emergency', name: 'الطوارئ والمساعدة' }
  ];

  const phrasesData = {
    greetings: [
      { de: 'Hallo!', ar: 'مرحباً!', context: 'تحية عامة غير رسمية' },
      { de: 'Guten Tag!', ar: 'نهارك سعيد / يوم سعيد', context: 'تحية رسمية خلال النهار' },
      { de: 'Wie heißen Sie?', ar: 'ما اسم حضرتك؟', context: 'سؤال رسمي عن الاسم' },
      { de: 'Ich heiße Ahmed.', ar: 'اسمي أحمد.', context: 'الإجابة عن الاسم' },
      { de: 'Woher kommen Sie?', ar: 'من أين حضرتك؟', context: 'سؤال رسمي عن الموطن' },
      { de: 'Ich komme aus Ägypten.', ar: 'أنا من مصر.', context: 'الإجابة عن البلد' },
      { de: 'Freut mich!', ar: 'سررت بلقائك!', context: 'تقال عند التعرف لأول مرة' }
    ],
    daily: [
      { de: 'Wie geht es Ihnen?', ar: 'كيف حال حضرتك؟', context: 'سؤال رسمي عن الحال' },
      { de: 'Danke, gut!', ar: 'شكراً، بخير!', context: 'إجابة سريعة ومبسطة' },
      { de: 'Ich verstehe nicht.', ar: 'أنا لا أفهم.', context: 'عند عدم فهم الكلام' },
      { de: 'Können Sie das wiederholen?', ar: 'هل يمكنك إعادة ذلك؟', context: 'طلب إعادة الشرح' },
      { de: 'Sprechen Sie Englisch?', ar: 'هل تتحدث الإنجليزية؟', context: 'سؤال عن الإنجليزية' },
      { de: 'Sprechen Sie bitte langsam.', ar: 'تحدث ببطء من فضلك.', context: 'طلب التحدث ببطء' }
    ],
    shopping: [
      { de: 'Was kostet das?', ar: 'كم سعر هذا؟', context: 'السؤال عن السعر' },
      { de: 'Ich möchte das bitte kaufen.', ar: 'أود شراء هذا من فضلك.', context: 'عند الشراء' },
      { de: 'Kann ich mit Karte zahlen?', ar: 'هل يمكنني الدفع بالبطاقة؟', context: 'طريقة الدفع' },
      { de: 'Die Rechnung, bitte!', ar: 'الحساب من فضلك!', context: 'طلب الفاتورة بالمطعم' },
      { de: 'Wo ist der Supermarkt?', ar: 'أين هو السوبرماركت؟', context: 'السؤال عن الاتجاهات' }
    ],
    emergency: [
      { de: 'Hilfe!', ar: 'النجدة / المساعدة!', context: 'طوارئ عامة' },
      { de: 'Rufen Sie einen Arzt!', ar: 'اتصلوا بالطبيب!', context: 'طلب طبيب' },
      { de: 'Ich brauche Hilfe.', ar: 'أحتاج إلى المساعدة.', context: 'طلب عون' },
      { de: 'Wo ist die Toilette?', ar: 'أين الحمام؟', context: 'سؤال هام ومباشر' }
    ]
  };

  return (
    <div className="space-y-6">
      <div className="bg-gradient-to-r from-slate-900 to-amber-950 text-white p-6 rounded-3xl shadow-md">
        <h2 className="text-xl sm:text-2xl font-black mb-2 flex items-center gap-2">
          💬 أهم جمل وعبارات مستوى A1
        </h2>
        <p className="text-xs sm:text-sm text-slate-300">
          اضغط على زر الصوت في أي بطاقة للاستماع إلى النطق الألماني الصحيح بصوت نقي وبسرعة مناسبة للمبتدئين!
        </p>
      </div>

      {/* Category Buttons */}
      <div className="flex flex-wrap gap-2 border-b border-slate-200 pb-3">
        {categories.map(cat => (
          <button
            key={cat.id}
            onClick={() => setActiveCategory(cat.id)}
            className={`px-4 py-2 rounded-xl text-xs sm:text-sm font-bold transition ${
              activeCategory === cat.id
                ? 'bg-amber-500 text-slate-950 shadow-sm'
                : 'bg-white text-slate-600 hover:bg-slate-100 border border-slate-200'
            }`}
          >
            {cat.name}
          </button>
        ))}
      </div>

      {/* Phrases Cards Grid */}
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
        {phrasesData[activeCategory].map((item, idx) => (
          <div key={idx} className="bg-white border border-slate-200 rounded-2xl p-4 hover:shadow-md transition flex flex-col justify-between space-y-3">
            <div>
              <div className="flex justify-between items-start mb-2">
                <span className="text-[10px] font-bold uppercase tracking-wider text-amber-700 bg-amber-50 px-2 py-0.5 rounded-md border border-amber-100">
                  {item.context}
                </span>
                <button
                  onClick={() => speak(item.de)}
                  className="p-2 bg-amber-50 hover:bg-amber-500 hover:text-white text-amber-600 rounded-xl transition shadow-sm"
                  title="استمع للنطق"
                >
                  <Volume2 className="w-5 h-5" />
                </button>
              </div>
              <h3 className="text-lg font-black text-slate-900 dir-ltr text-right font-mono">{item.de}</h3>
            </div>
            <div className="pt-2 border-t border-slate-100">
              <p className="text-xs sm:text-sm font-bold text-slate-600">{item.ar}</p>
            </div>
          </div>
        ))}
      </div>
    </div>
  );
}

// ==========================================
// 3. AI TUTOR SECTION (المعلم الذكي Gemini)
// ==========================================
function AITutorSection({ speak }) {
  const [messages, setMessages] = useState([
    {
      sender: 'bot',
      text: 'Hallo! 👋 أنا "Herr Max" معلمك الذكي للغة الألمانية! يمكنك أن تسألني عن أي قاعدة، أو نتدرب معاً على المحادثة البسيطة لمستوى A1. كيف يمكنني مساعدتك اليوم؟'
    }
  ]);
  const [input, setInput] = useState('');
  const [loading, setLoading] = useState(false);
  const chatEndRef = useRef(null);

  const scrollToBottom = () => {
    chatEndRef.current?.scrollIntoView({ behavior: 'smooth' });
  };

  useEffect(() => {
    scrollToBottom();
  }, [messages, loading]);

  const handleSend = async () => {
    if (!input.trim() || loading) return;

    const userText = input;
    setInput('');
    setMessages(prev => [...prev, { sender: 'user', text: userText }]);
    setLoading(true);

    try {
      const apiKey = ""; // API Key placeholder for runtime injection
      const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-3-flash-preview:generateContent?key=${apiKey}`;

      const systemPrompt = `
        أنت معلم لغة ألمانية ممتاز وصبور اسمه "Herr Max" مخصص لتعليم المبتدئين في المستوى الأول (A1).
        - أسلوبك مشجع ولطيف جداً ومناسب للطلاب المصريين والعرب.
        - تحدث بالألمانية المبسطة جداً مع ترجمة توضيحية بالعربية المصرية.
        - إذا كتب لك المستطرد بالألمانية، قم بتصحيح الأخطاء النحوية أو الإملائية بلطف وشرحها بشكل مبسط جداً.
        - اجعل إجاباتك قصيرة ومباشرة ومشجعة (لا تطل الإجابة).
      `;

      // Build chat context
      const contentsPayload = [
        ...messages.map(m => ({
          role: m.sender === 'user' ? 'user' : 'model',
          parts: [{ text: m.text }]
        })),
        { role: 'user', parts: [{ text: userText }] }
      ];

      const response = await fetch(apiUrl, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          contents: contentsPayload,
          systemInstruction: { parts: [{ text: systemPrompt }] }
        })
      });

      const data = await response.json();
      const botResponse = data.candidates?.[0]?.content?.parts?.[0]?.text || 'عذراً لم أستطع فهم ذلك، هل يمكنك المحاولة مرة أخرى؟';

      setMessages(prev => [...prev, { sender: 'bot', text: botResponse }]);
    } catch (error) {
      console.error('AI Error:', error);
      setMessages(prev => [...prev, { 
        sender: 'bot', 
        text: 'حدث خطأ في الاتصال بالسيرفر الذكي. يرجى التأكد من الإنترنت والمحاولة لاحقاً.' 
      }]);
    } finally {
      setLoading(false);
    }
  };

  return (
    <div className="max-w-4xl mx-auto h-[75vh] flex flex-col bg-white rounded-3xl border border-slate-200 shadow-lg overflow-hidden">
      {/* Chat Header */}
      <div className="bg-slate-900 text-white p-4 flex items-center justify-between border-b border-slate-800">
        <div className="flex items-center gap-3">
          <div className="relative">
            <div className="w-10 h-10 rounded-full bg-amber-500 text-slate-950 flex items-center justify-center font-black text-lg shadow-inner">
              👨‍🏫
            </div>
            <span className="w-3 h-3 bg-emerald-500 border-2 border-slate-900 rounded-full absolute bottom-0 right-0"></span>
          </div>
          <div>
            <h3 className="font-bold text-sm sm:text-base flex items-center gap-2">
              Herr Max <span className="text-[10px] bg-amber-400 text-slate-950 px-1.5 py-0.5 rounded font-extrabold">Gemini AI</span>
            </h3>
            <p className="text-xs text-slate-400">معلم الألمانية التفاعلي لمستوى A1</p>
          </div>
        </div>

        <button 
          onClick={() => setMessages([{
            sender: 'bot',
            text: 'مرحباً من جديد! كيف يمكنني مساعدتك الآن؟'
          }])}
          className="text-slate-400 hover:text-white text-xs flex items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition"
        >
          <RotateCcw className="w-4 h-4" />
          <span className="hidden sm:inline">محادثة جديدة</span>
        </button>
      </div>

      {/* Messages Scroll Area */}
      <div className="flex-1 overflow-y-auto p-4 space-y-4 bg-slate-50/50">
        {messages.map((msg, index) => (
          <div
            key={index}
            className={`flex items-start gap-2 ${msg.sender === 'user' ? 'flex-row-reverse' : 'flex-row'}`}
          >
            <div className={`w-8 h-8 rounded-full flex items-center justify-center text-xs shrink-0 font-bold ${
              msg.sender === 'user' ? 'bg-amber-500 text-slate-950' : 'bg-slate-800 text-amber-400'
            }`}>
              {msg.sender === 'user' ? <User className="w-4 h-4" /> : <Bot className="w-4 h-4" />}
            </div>

            <div className={`max-w-[85%] sm:max-w-[75%] rounded-2xl p-3.5 text-xs sm:text-sm leading-relaxed shadow-sm relative group ${
              msg.sender === 'user'
                ? 'bg-amber-500 text-slate-950 font-medium rounded-tr-none'
                : 'bg-white text-slate-800 border border-slate-200 rounded-tl-none'
            }`}>
              <p className="whitespace-pre-wrap">{msg.text}</p>
              
              {/* Optional Read Aloud button for Bot response */}
              {msg.sender === 'bot' && (
                <button
                  onClick={() => speak(msg.text)}
                  className="mt-2 text-[10px] text-slate-400 hover:text-amber-600 flex items-center gap-1 font-semibold"
                >
                  <Volume2 className="w-3.5 h-3.5" /> استمع للنص الألماني
                </button>
              )}
            </div>
          </div>
        ))}

        {loading && (
          <div className="flex items-center gap-2 text-slate-400 text-xs font-semibold p-2">
            <Bot className="w-4 h-4 animate-spin text-amber-500" />
            <span>Herr Max يفكر ويعد لك الإجابة...</span>
          </div>
        )}
        <div ref={chatEndRef} />
      </div>

      {/* Chat Input */}
      <div className="p-3 sm:p-4 bg-white border-t border-slate-200">
        <form
          onSubmit={(e) => {
            e.preventDefault();
            handleSend();
          }}
          className="flex items-center gap-2"
        >
          <input
            type="text"
            value={input}
            onChange={(e) => setInput(e.target.value)}
            placeholder="اسأل معلمك الألمانية عن قاعدة أو أكتب جملة ليتأكد منها..."
            className="flex-1 bg-slate-100 text-slate-800 px-4 py-2.5 rounded-2xl text-xs sm:text-sm focus:outline-none focus:ring-2 focus:ring-amber-500 border border-transparent"
          />
          <button
            type="submit"
            disabled={!input.trim() || loading}
            className="bg-amber-500 hover:bg-amber-600 text-slate-950 p-2.5 rounded-2xl transition disabled:opacity-50 shrink-0"
          >
            <Send className="w-5 h-5 rotate-180" />
          </button>
        </form>
      </div>
    </div>
  );
}

// ==========================================
// 4. EXERCISES SECTION (التدريبات والتمارين)
// ==========================================
function ExercisesSection({ speak }) {
  const [activeGame, setActiveGame] = useState('articles'); // 'articles' | 'fill'
  const [score, setScore] = useState(0);

  // Article Game State
  const [articleIndex, setArticleIndex] = useState(0);
  const [articleFeedback, setArticleFeedback] = useState(null);

  const articleWords = [
    { word: 'Tisch', correct: 'der', tr: 'طاولة' },
    { word: 'Frau', correct: 'die', tr: 'مرأة' },
    { word: 'Kind', correct: 'das', tr: 'طفل' },
    { word: 'Auto', correct: 'das', tr: 'سيارة' },
    { word: 'Stuhl', correct: 'der', tr: 'كرسي' },
    { word: 'Tasche', correct: 'die', tr: 'حقيبة' },
    { word: 'Buch', correct: 'das', tr: 'كتاب' },
    { word: 'Mann', correct: 'der', tr: 'رجل' }
  ];

  const handleArticleGuess = (chosen) => {
    const current = articleWords[articleIndex];
    if (chosen === current.correct) {
      setScore(prev => prev + 10);
      setArticleFeedback({ type: 'correct', msg: `إجابة صحيحة! 🎉 (${current.correct} ${current.word})` });
      speak(`${current.correct} ${current.word}`);
    } else {
      setArticleFeedback({ type: 'wrong', msg: `إجابة خاطئة ❌ الأداة الصحيحة هي: ${current.correct}` });
    }

    setTimeout(() => {
      setArticleFeedback(null);
      setArticleIndex(prev => (prev + 1) % articleWords.length);
    }, 1500);
  };

  // Fill in the Blanks Game State
  const [fillIndex, setFillIndex] = useState(0);
  const [selectedOption, setSelectedOption] = useState(null);
  const [fillFeedback, setFillFeedback] = useState(null);

  const fillQuestions = [
    {
      q: 'Ich ___ aus Ägypten.',
      options: ['komme', 'kommt', 'kommen'],
      ans: 'komme',
      explain: 'الضمير ich يأخذ النهاية -e دائماً.'
    },
    {
      q: 'Wo ___ du?',
      options: ['wohnen', 'wohnst', 'wohnt'],
      ans: 'wohnst',
      explain: 'الضمير du يأخذ النهاية -st.'
    },
    {
      q: 'Das ist ___ Auto. (نفي سيارة)',
      options: ['nicht', 'kein', 'keine'],
      ans: 'kein',
      explain: 'نستخدم kein لنفي الأسماء المحايدة (das Auto).'
    }
  ];

  const handleFillSubmit = (opt) => {
    const current = fillQuestions[fillIndex];
    setSelectedOption(opt);
    if (opt === current.ans) {
      setScore(prev => prev + 15);
      setFillFeedback({ type: 'correct', msg: `ممتاز! 👏 ${current.explain}` });
    } else {
      setFillFeedback({ type: 'wrong', msg: `حاول مجدداً ❌ الإجابة الصحيحة هي "${current.ans}". ${current.explain}` });
    }

    setTimeout(() => {
      setSelectedOption(null);
      setFillFeedback(null);
      setFillIndex(prev => (prev + 1) % fillQuestions.length);
    }, 2500);
  };

  return (
    <div className="space-y-6">
      {/* Exercise Tabs & Score Header */}
      <div className="flex flex-col sm:flex-row justify-between items-start sm:items-center bg-white p-4 rounded-3xl border border-slate-200 gap-4 shadow-sm">
        <div className="flex gap-2">
          <button
            onClick={() => setActiveGame('articles')}
            className={`px-4 py-2 rounded-2xl text-xs sm:text-sm font-bold transition ${
              activeGame === 'articles'
                ? 'bg-amber-500 text-slate-950'
                : 'bg-slate-100 text-slate-600 hover:bg-slate-200'
            }`}
          >
            🎮 لعبة الأداة (der / die / das)
          </button>
          <button
            onClick={() => setActiveGame('fill')}
            className={`px-4 py-2 rounded-2xl text-xs sm:text-sm font-bold transition ${
              activeGame === 'fill'
                ? 'bg-amber-500 text-slate-950'
                : 'bg-slate-100 text-slate-600 hover:bg-slate-200'
            }`}
          >
            ✏️ أكمل الفراغ بالنهاية الصحيحة
          </button>
        </div>

        <div className="flex items-center gap-2 bg-amber-50 border border-amber-200 px-3 py-1.5 rounded-2xl text-xs font-bold text-amber-900">
          <Award className="w-4 h-4 text-amber-600" />
          <span>نقاطك التفاعلية: <span className="text-sm font-black text-amber-600">{score}</span></span>
        </div>
      </div>

      {/* GAME 1: ARTICLES */}
      {activeGame === 'articles' && (
        <div className="max-w-xl mx-auto bg-white border border-slate-200 rounded-3xl p-6 sm:p-8 text-center space-y-6 shadow-sm">
          <span className="text-xs font-bold text-slate-400">سؤال {articleIndex + 1} من {articleWords.length}</span>
          
          <div>
            <span className="text-3xl sm:text-4xl font-black text-slate-900 font-mono tracking-wide">
              ___ {articleWords[articleIndex].word}
            </span>
            <p className="text-xs text-slate-500 mt-2">المعنى: ({articleWords[articleIndex].tr})</p>
          </div>

          <div className="grid grid-cols-3 gap-3">
            {[
              { art: 'der', color: 'bg-blue-600 hover:bg-blue-700' },
              { art: 'die', color: 'bg-pink-600 hover:bg-pink-700' },
              { art: 'das', color: 'bg-emerald-600 hover:bg-emerald-700' }
            ].map(item => (
              <button
                key={item.art}
                onClick={() => handleArticleGuess(item.art)}
                disabled={articleFeedback !== null}
                className={`${item.color} text-white font-black py-3 rounded-2xl text-lg shadow-md transition transform active:scale-95 disabled:opacity-50`}
              >
                {item.art}
              </button>
            ))}
          </div>

          {articleFeedback && (
            <div className={`p-3 rounded-2xl text-xs font-bold animate-fade-in ${
              articleFeedback.type === 'correct' ? 'bg-emerald-100 text-emerald-800' : 'bg-red-100 text-red-800'
            }`}>
              {articleFeedback.msg}
            </div>
          )}
        </div>
      )}

      {/* GAME 2: FILL IN BLANKS */}
      {activeGame === 'fill' && (
        <div className="max-w-xl mx-auto bg-white border border-slate-200 rounded-3xl p-6 sm:p-8 space-y-6 shadow-sm">
          <span className="text-xs font-bold text-slate-400">تمرين {fillIndex + 1} من {fillQuestions.length}</span>

          <h3 className="text-lg sm:text-xl font-black text-slate-900 text-center font-mono">
            {fillQuestions[fillIndex].q}
          </h3>

          <div className="space-y-2">
            {fillQuestions[fillIndex].options.map((opt) => (
              <button
                key={opt}
                onClick={() => handleFillSubmit(opt)}
                disabled={fillFeedback !== null}
                className={`w-full p-3.5 rounded-2xl text-xs sm:text-sm font-bold text-right border transition flex justify-between items-center ${
                  selectedOption === opt
                    ? 'bg-amber-500 text-slate-950 border-amber-600'
                    : 'bg-slate-50 hover:bg-slate-100 text-slate-800 border-slate-200'
                }`}
              >
                <span>{opt}</span>
                {selectedOption === opt && <Check className="w-4 h-4" />}
              </button>
            ))}
          </div>

          {fillFeedback && (
            <div className={`p-3.5 rounded-2xl text-xs font-bold leading-relaxed ${
              fillFeedback.type === 'correct' ? 'bg-emerald-100 text-emerald-900' : 'bg-red-100 text-red-900'
            }`}>
              {fillFeedback.msg}
            </div>
          )}
        </div>
      )}
    </div>
  );
}

// ==========================================
// 5. EXAM SECTION (الامتحان النهائي A1)
// ==========================================
function ExamSection({ progress, saveProgress, speak }) {
  const [examStarted, setExamStarted] = useState(false);
  const [currentQ, setCurrentQ] = useState(0);
  const [userAnswers, setUserAnswers] = useState({});
  const [showResult, setShowResult] = useState(false);

  const examQuestions = [
    {
      id: 1,
      q: 'Welche Aussage ist richtig? (أي جملة هي الصحيحة نحوياً؟)',
      options: [
        'Ich lerne heute Deutsch.',
        'Heute ich lerne Deutsch.',
        'Ich Deutsch lerne heute.'
      ],
      correct: 0,
      explain: 'في الجملة الخبرية، الفعل المصرف (lerne) يجب أن يأتي دائماً في المركز الثاني (Position 2).'
    },
    {
      id: 2,
      q: 'Wie heißen Sie? - Ich ___ Sarah.',
      options: ['heiße', 'heißt', 'heißen'],
      correct: 0,
      explain: 'تصريف الفعل heißen مع الضمير ich هو heiße.'
    },
    {
      id: 3,
      q: 'Was ist das? - Das ist ___ Buch. (كتاب/محايد)',
      options: ['ein', 'eine', 'einen'],
      correct: 0,
      explain: 'كلمة Buch أداتها das، وأداة التنكير للمحايد هي ein.'
    },
    {
      id: 4,
      q: 'Haben Sie Kinder? - Nein, ich habe ___ Kinder.',
      options: ['kein', 'nicht', 'keine'],
      correct: 2,
      explain: 'كلمة Kinder اسم جمع، ونفي الجمع يكون بـ keine.'
    },
    {
      id: 5,
      q: 'Wo ___ du? - In Kairo.',
      options: ['wohnst', 'wohne', 'wohnt'],
      correct: 0,
      explain: 'مع الضمير du نضيف النهاية -st للفعل.'
    }
  ];

  const handleOptionSelect = (qIdx, optionIdx) => {
    setUserAnswers({ ...userAnswers, [qIdx]: optionIdx });
  };

  const calculateScore = () => {
    let correctCount = 0;
    examQuestions.forEach((q, idx) => {
      if (userAnswers[idx] === q.correct) {
        correctCount++;
      }
    });
    return Math.round((correctCount / examQuestions.length) * 100);
  };

  const finishExam = () => {
    const finalScore = calculateScore();
    setShowResult(true);
    if (finalScore >= 60) {
      saveProgress({ ...progress, passedExam: true });
    }
  };

  return (
    <div className="max-w-3xl mx-auto space-y-6">
      {!examStarted ? (
        <div className="bg-white border border-slate-200 rounded-3xl p-6 sm:p-8 text-center space-y-6 shadow-sm">
          <div className="w-16 h-16 bg-amber-100 text-amber-600 rounded-full flex items-center justify-center mx-auto text-2xl font-black">
            🎓
          </div>
          <div>
            <h2 className="text-xl sm:text-2xl font-black text-slate-900">محاكي الامتحان النهائي لمستوى A1</h2>
            <p className="text-xs sm:text-sm text-slate-500 mt-2 max-w-md mx-auto leading-relaxed">
              هذا الامتحان يحاكي أسئلة قواعد Goethe/ÖSD لمستوى A1. يتكون من 5 أسئلة رئيسية ومصمم لاختبار جاهزيتك.
            </p>
          </div>

          <div className="bg-slate-50 p-4 rounded-2xl text-xs space-y-2 text-right border border-slate-200">
            <h4 className="font-bold text-slate-800">شروط النجاح:</h4>
            <p className="text-slate-600">✓ الحصول على 60% على الأقل لاجتياز المستوى.</p>
            <p className="text-slate-600">✓ سيتم عرض إجاباتك مع الشرح التفصيلي بعد الانتهاء.</p>
          </div>

          <button
            onClick={() => setExamStarted(true)}
            className="bg-amber-500 hover:bg-amber-600 text-slate-950 font-black px-8 py-3.5 rounded-2xl text-sm shadow-md transition transform active:scale-95"
          >
            ابدأ الامتحان الآن 🚀
          </button>
        </div>
      ) : showResult ? (
        <div className="bg-white border border-slate-200 rounded-3xl p-6 sm:p-8 text-center space-y-6 shadow-sm">
          <div className="space-y-2">
            <h2 className="text-2xl font-black text-slate-900">نتيجة الامتحان النهائي</h2>
            <p className="text-xs text-slate-500">تقييم الجاهزية لمستوى A1</p>
          </div>

          {/* Score Badge */}
          <div className="py-6">
            <div className={`inline-block p-6 rounded-full border-4 ${
              calculateScore() >= 60 ? 'bg-emerald-50 border-emerald-500 text-emerald-700' : 'bg-red-50 border-red-500 text-red-700'
            }`}>
              <span className="text-4xl font-black">{calculateScore()}%</span>
            </div>
            <p className="text-sm font-bold mt-3">
              {calculateScore() >= 60 
                ? '🎉 مبروك! أنت جاهز لاجتياز مستوى A1 بنجاح!' 
                : '⚠️ تحتاج إلى مراجعة بعض الدروس قبل دخول الامتحان الرسمي.'}
            </p>
          </div>

          {/* Answer Breakdown */}
          <div className="space-y-3 text-right">
            <h4 className="font-bold text-slate-800 text-sm">مراجعة الإجابات وشرح القواعد:</h4>
            {examQuestions.map((q, idx) => {
              const isCorrect = userAnswers[idx] === q.correct;
              return (
                <div key={q.id} className={`p-4 rounded-2xl border text-xs space-y-1.5 ${
                  isCorrect ? 'bg-emerald-50/50 border-emerald-200' : 'bg-red-50/50 border-red-200'
                }`}>
                  <div className="flex justify-between font-bold text-slate-900">
                    <span>{idx + 1}. {q.q}</span>
                    <span>{isCorrect ? '✅ صح' : '❌ خطأ'}</span>
                  </div>
                  <p className="text-slate-600">
                    إجابتك: <span className="font-semibold">{q.options[userAnswers[idx]] || 'لم تجب'}</span>
                  </p>
                  {!isCorrect && (
                    <p className="text-emerald-700 font-semibold">
                      الإجابة الصحيحة: {q.options[q.correct]}
                    </p>
                  )}
                  <p className="text-slate-500 text-[11px] bg-white p-2 rounded-xl mt-1 border border-slate-100">
                    💡 **الشرح:** {q.explain}
                  </p>
                </div>
              );
            })}
          </div>

          <button
            onClick={() => {
              setExamStarted(false);
              setShowResult(false);
              setUserAnswers({});
              setCurrentQ(0);
            }}
            className="bg-slate-900 text-white font-bold px-6 py-3 rounded-2xl text-xs transition hover:bg-slate-800"
          >
            إعادة الامتحان 🔄
          </button>
        </div>
      ) : (
        /* Exam In Progress */
        <div className="bg-white border border-slate-200 rounded-3xl p-6 sm:p-8 space-y-6 shadow-sm">
          <div className="flex justify-between items-center text-xs text-slate-400 border-b border-slate-100 pb-3">
            <span>السؤال {currentQ + 1} من {examQuestions.length}</span>
            <span className="font-bold text-amber-600">A1 Prüfung Simulator</span>
          </div>

          <h3 className="text-base sm:text-lg font-black text-slate-900 leading-snug">
            {examQuestions[currentQ].q}
          </h3>

          <div className="space-y-2.5">
            {examQuestions[currentQ].options.map((opt, optIdx) => (
              <button
                key={optIdx}
                onClick={() => handleOptionSelect(currentQ, optIdx)}
                className={`w-full p-3.5 rounded-2xl text-xs sm:text-sm font-bold text-right border transition flex justify-between items-center ${
                  userAnswers[currentQ] === optIdx
                    ? 'bg-amber-500 text-slate-950 border-amber-600'
                    : 'bg-slate-50 hover:bg-slate-100 text-slate-800 border-slate-200'
                }`}
              >
                <span>{opt}</span>
                {userAnswers[currentQ] === optIdx && <Check className="w-4 h-4" />}
              </button>
            ))}
          </div>

          <div className="flex justify-between items-center pt-4 border-t border-slate-100">
            <button
              disabled={currentQ === 0}
              onClick={() => setCurrentQ(prev => prev - 1)}
              className="px-4 py-2 bg-slate-100 disabled:opacity-40 text-slate-700 rounded-xl text-xs font-bold"
            >
              السابق
            </button>

            {currentQ < examQuestions.length - 1 ? (
              <button
                disabled={userAnswers[currentQ] === undefined}
                onClick={() => setCurrentQ(prev => prev + 1)}
                className="px-6 py-2 bg-amber-500 disabled:opacity-40 text-slate-950 rounded-xl text-xs font-bold"
              >
                التالي
              </button>
            ) : (
              <button
                disabled={userAnswers[currentQ] === undefined}
                onClick={finishExam}
                className="px-6 py-2 bg-emerald-600 disabled:opacity-40 text-white rounded-xl text-xs font-bold shadow-md"
              >
                إنهاء الاختبار
              </button>
            )}
          </div>
        </div>
      )}
    </div>
  );
}