<!-- زر النصيحة العائم - أضف هذا الكود قبل </body> في كل صفحة -->

<style>
.tip-fab {
  position: fixed;
  bottom: 90px;
  left: 20px;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

.tip-btn {
  display: flex;
  align-items: center;
  gap: 10px;
  background: linear-gradient(135deg, #f5c842, #e5a800);
  color: #0a0e1a;
  border: none;
  border-radius: 50px;
  padding: 14px 20px;
  font-family: 'Cairo', sans-serif;
  font-size: 14px;
  font-weight: 800;
  cursor: pointer;
  box-shadow: 0 4px 20px rgba(245,200,66,0.5);
  transition: all 0.3s;
  animation: pulse-fab 2s infinite;
  white-space: nowrap;
}

.tip-btn:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 28px rgba(245,200,66,0.7);
}

@keyframes pulse-fab {
  0%, 100% { box-shadow: 0 4px 20px rgba(245,200,66,0.5); }
  50% { box-shadow: 0 4px 32px rgba(245,200,66,0.9); }
}

.tip-modal {
  display: none;
  position: fixed;
  bottom: 160px;
  left: 20px;
  z-index: 9999;
  background: #1a2340;
  border: 1px solid rgba(245,200,66,0.3);
  border-radius: 20px;
  padding: 20px;
  max-width: 320px;
  width: calc(100vw - 40px);
  box-shadow: 0 12px 40px rgba(0,0,0,0.5);
  animation: slideUp 0.3s ease;
  direction: rtl;
}

@keyframes slideUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.tip-modal.open { display: block; }

.tip-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 14px;
}

.tip-title {
  font-family: 'Cairo', sans-serif;
  font-size: 15px;
  font-weight: 800;
  color: #f5c842;
  display: flex;
  align-items: center;
  gap: 8px;
}

.tip-close {
  background: none;
  border: none;
  color: #64748b;
  cursor: pointer;
  font-size: 20px;
  line-height: 1;
  padding: 0;
}

.tip-content {
  font-family: 'Cairo', sans-serif;
  font-size: 14px;
  color: #e8edf8;
  line-height: 1.8;
  min-height: 60px;
}

.tip-loading {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #a0aec0;
  font-family: 'Cairo', sans-serif;
  font-size: 13px;
}

.tip-spinner {
  width: 16px;
  height: 16px;
  border: 2px solid rgba(245,200,66,0.3);
  border-top-color: #f5c842;
  border-radius: 50%;
  animation: spin 0.8s linear infinite;
}

@keyframes spin { to { transform: rotate(360deg); } }

.tip-footer {
  margin-top: 14px;
  padding-top: 12px;
  border-top: 1px solid rgba(99,130,255,0.15);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.tip-new-btn {
  background: rgba(245,200,66,0.1);
  border: 1px solid rgba(245,200,66,0.3);
  color: #f5c842;
  border-radius: 8px;
  padding: 7px 14px;
  font-family: 'Cairo', sans-serif;
  font-size: 12px;
  font-weight: 700;
  cursor: pointer;
  transition: all 0.2s;
}

.tip-new-btn:hover {
  background: rgba(245,200,66,0.2);
}

.tip-badge {
  font-family: 'Cairo', sans-serif;
  font-size: 11px;
  color: #64748b;
}
</style>

<!-- زر النصيحة العائم -->
<div class="tip-fab">
  <div class="tip-modal" id="tipModal">
    <div class="tip-header">
      <div class="tip-title">💡 نصيحة اليوم</div>
      <button class="tip-close" onclick="closeTip()">×</button>
    </div>
    <div class="tip-content" id="tipContent">
      <div class="tip-loading">
        <div class="tip-spinner"></div>
        جاري توليد نصيحة مخصصة لك...
      </div>
    </div>
    <div class="tip-footer">
      <button class="tip-new-btn" onclick="loadTip()">🔄 نصيحة أخرى</button>
      <div class="tip-badge">⚡ بواسطة Gemini AI</div>
    </div>
  </div>

  <button class="tip-btn" onclick="toggleTip()">
    💡 نصيحة اليوم للطالب
  </button>
</div>

<script>
const GEMINI_KEY = 'AIzaSyCaiZV0wew1zW6oyx5kO0kITTXaxJ9ZycA';
let tipOpen = false;
let tipLoaded = false;

const topics = [
  'نصيحة للطالب العربي في مرحلة البكالوريا حول إدارة الوقت والمذاكرة',
  'نصيحة للطالب العربي حول اختيار التخصص الجامعي المناسب',
  'نصيحة للطالب العربي حول التغلب على ضغط الامتحانات',
  'نصيحة للطالب العربي حول الاستعداد لامتحانات البكالوريا',
  'نصيحة للطالب العربي حول التفوق الدراسي وبناء المستقبل',
  'نصيحة للطالب العربي حول أهمية القراءة والتعلم الذاتي',
  'نصيحة للطالب العربي حول الصحة النفسية خلال فترة الامتحانات',
];

async function loadTip() {
  const content = document.getElementById('tipContent');
  content.innerHTML = `<div class="tip-loading"><div class="tip-spinner"></div>جاري توليد نصيحة مخصصة لك...</div>`;

  const topic = topics[Math.floor(Math.random() * topics.length)];

  try {
    const res = await fetch(
      `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${GEMINI_KEY}`,
      {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          contents: [{
            parts: [{
              text: `اكتب ${topic} في جملتين أو ثلاث جمل قصيرة ومفيدة ومحفزة باللغة العربية الفصحى البسيطة. لا تستخدم عناوين أو نقاط، فقط نص مباشر.`
            }]
          }]
        })
      }
    );
    const data = await res.json();
    const tip = data.candidates?.[0]?.content?.parts?.[0]?.text || 'تعلّم كل يوم شيئاً جديداً، فالعلم نور يضيء طريقك نحو المستقبل.';
    content.innerHTML = tip;
    tipLoaded = true;
  } catch (e) {
    content.innerHTML = 'النجاح لا يأتي بالصدفة، بل بالإصرار والعمل المستمر. استثمر وقتك في المذاكرة والتعلم اليوم لتحصد ثماره غداً.';
  }
}

function toggleTip() {
  const modal = document.getElementById('tipModal');
  tipOpen = !tipOpen;
  if (tipOpen) {
    modal.classList.add('open');
    if (!tipLoaded) loadTip();
  } else {
    modal.classList.remove('open');
  }
}

function closeTip() {
  document.getElementById('tipModal').classList.remove('open');
  tipOpen = false;
}
</script>
