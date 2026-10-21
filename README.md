# مهارة كتابة السيناريو
### (Arabic Screenwriting Skill)

<p align="center">
  <a href="https://github.com/specailm5/arabic-screenwriting-skill/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/specailm5/arabic-screenwriting-skill?style=flat-square"></a>
  <a href="https://github.com/specailm5/arabic-screenwriting-skill/commits/master"><img alt="Last commit" src="https://img.shields.io/github/last-commit/specailm5/arabic-screenwriting-skill?style=flat-square"></a>
  <a href="https://specailm5.github.io/arabic-screenwriting-skill/"><img alt="Docs" src="https://img.shields.io/badge/docs-live-brightgreen?style=flat-square"></a>
  <img alt="Agent Skills" src="https://img.shields.io/badge/Agent%20Skills-compatible-5B21B6?style=flat-square">
</p>

**Arabic screenwriting skill for AI agents** — turns an idea into a logline, synopsis, treatment and scene-by-scene script; builds three-act structure, character desire and obstacle, scene objectives, visual storytelling and dialogue: `«يشعر بالحزن»` ← `«يضع يده على كتفها، ثم يسحبها»`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (البنية والشخصية والمشهد والنماذج): [specailm5.github.io/arabic-screenwriting-skill](https://specailm5.github.io/arabic-screenwriting-skill/)**

> مهارة برمجية ولغوية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لكتابة السيناريو العربي وتحريره وتشخيصه، استناداً إلى **«السيناريو»** لسيد فيلد، و**«فن كتابة السيناريو»** لفرانك هارو، و**«كيف تكتب السيناريو»** لصلاح أبو سيف.

---

## 📖 ما هي المهارة؟

أكثر ما يُكتب تحت اسم «سيناريو» هو حوار يشرح ما لم يُصوَّر. والنتيجة نصّ يُقرأ ولا يُرى، وشخصيات تتكلم بلسان واحد، ونهاية تأتي من خارج القصة.

تُمكِّنُ هذه المهارةُ الوكيلَ الذكيَّ من:

1. **تحويل الفكرة إلى لوجلاين** فيه شخص ورغبة وعائق ورهان.
2. **بناء الملخص والمعالجة** قبل القفز إلى الحوار.
3. **رسم البنية:** الفصول الثلاثة، والحبكتان، والتصعيد، والنهاية.
4. **بناء الشخصية:** الرغبة، والحاجة، والعائق، والقوس.
5. **كتابة المشهد:** هدف، ودخول متأخر، وخروج مبكر، وصورة.
6. **ضبط الحوار:** يدفع ولا يشرح، ويُسمع ولا يُقرأ.
7. **تنسيق الصفحة** وترويسة المشهد والانتقالات.
8. **تقييم المسودة** مشهداً مشهداً، مع سلم خطورة.

**القواعد الأربع:**
> **قصة تُرى. مشهد له هدف. حوار يُسمع. ونهاية نتيجة اختيار.**

---

## 📂 بنية المهارة ومكوناتها

<pre dir="rtl"><code>
arabic-screenwriting-skill/
│
├── skills/arabic-screenwriting-skill/          # المهارة (تركيب Agent Skills القياسي)
│   ├── SKILL.md                                # الدليل الأساسي: من الفكرة إلى التنسيق
│   ├── references/                             # المراجع التفصيلية
│   │   ├── structure.md                        # اللوجلاين، الملخص، المعالجة، الفصول
│   │   ├── character.md                        # الرغبة، الحاجة، العائق، القوس
│   │   ├── scene_dialogue.md                   # المشهد، الحوار، الصورة
│   │   └── format_adaptation.md                # التنسيق، التكييف، الحقوق
│   └── examples/                               # النماذج والتمارين
│       ├── before_after_scene.md                # مشهد كامل قبل/بعد
│       └── short_film_workshop.md               # ورشة فيلم قصير
│
├── docs/                                       # الموقع المرجعي (GitHub Pages)
│
├── .agents/skills/arabic-screenwriting-skill/  # مسار Codex و Antigravity
│
└── .claude/skills/arabic-screenwriting-skill/  # مسار Claude Code
</code></pre>

---

## 🚀 طرق التثبيت والاستخدام (Installation Guide)

تُثبَّتُ المهارةُ إما في مشروعٍ بعينه (**محلياً**)، وإما **عامةً (Global)** لتعمل في كافة المشاريع.

---

### أولاً: التثبيت بأمر واحد عبر `npx` (الطريقة الأسرع — موصى به)

```bash
npx skills add specailm5/arabic-screenwriting-skill -g -y
```

ولاختيار بيئات بعينها أو التثبيت داخل مشروع محدد:

```bash
npx skills add specailm5/arabic-screenwriting-skill -a claude-code -a codex
npx skills add specailm5/arabic-screenwriting-skill --skill arabic-screenwriting-skill -g -y
```

---

### ثانياً: التثبيت العام لبيئة Claude Code و Codex و Antigravity (يدوياً)

#### لنظام Windows (PowerShell):

```powershell
# مصدر المهارة داخل المستودع
$src = "skills\arabic-screenwriting-skill"

# 1. تثبيت لبيئة Claude Code
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-screenwriting-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-screenwriting-skill\"

# 2. تثبيت لبيئة Codex و Agent Skills العامة
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-screenwriting-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-screenwriting-skill\"

# 3. تثبيت لبيئة Google Antigravity / Gemini
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-screenwriting-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-screenwriting-skill\"
```

#### لنظام macOS / Linux (Bash):

```bash
src=skills/arabic-screenwriting-skill

# 1. لبيئة Claude Code
mkdir -p ~/.claude/skills/arabic-screenwriting-skill
cp -r "$src/." ~/.claude/skills/arabic-screenwriting-skill/

# 2. لبيئة Codex و Agent Harness
mkdir -p ~/.agents/skills/arabic-screenwriting-skill
cp -r "$src/." ~/.agents/skills/arabic-screenwriting-skill/

# 3. لبيئة Antigravity / Gemini
mkdir -p ~/.gemini/config/skills/arabic-screenwriting-skill
cp -r "$src/." ~/.gemini/config/skills/arabic-screenwriting-skill/
```

---

### ثالثاً: التثبيت المحلي داخل مشروع محدد (VS Code Workspace Harness)

```powershell
New-Item -ItemType Directory -Force -Path ".agents\skills\arabic-screenwriting-skill"
Copy-Item -Recurse -Force "path\to\skills\arabic-screenwriting-skill\*" ".agents\skills\arabic-screenwriting-skill\"
```

---

### رابعاً: الاستخدام اليدوي (Direct System Prompt / Custom Instructions)

* افتح ملف [`skills/arabic-screenwriting-skill/SKILL.md`](skills/arabic-screenwriting-skill/SKILL.md) وانسخ محتواه وضعه في خانة **التعليمات المخصصة (Custom Instructions)** أو **System Prompt**.

---

## ⚡ كيف تعمل المهارة؟

### سبعة أسئلة قبل الكتابة

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">السؤال</th>
<th align="right">لماذا؟</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ما النوع؟</strong></td>
<td>فيلم / قصير / مسلسل / مسرحية / إعلان</td>
</tr>
<tr>
<td><strong>ما الطول؟</strong></td>
<td>يحدد عدد المشاهد</td>
</tr>
<tr>
<td><strong>من الجمهور؟</strong></td>
<td>يحدد اللغة والإيقاع</td>
</tr>
<tr>
<td><strong>ما المصدر؟</strong></td>
<td>فكرة / رواية / قصة حقيقية</td>
</tr>
<tr>
<td><strong>ما الميزانية؟</strong></td>
<td>يحدد المشاهد القابلة للتنفيذ</td>
</tr>
<tr>
<td><strong>ما اللغة؟</strong></td>
<td>فصحى / عامية / مختلط</td>
</tr>
<tr>
<td><strong>ما المرحلة؟</strong></td>
<td>فكرة / ملخص / معالجة / سيناريو</td>
</tr>
</tbody>
</table>
<br clear="all">

### المراحل في سطر

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">المرحلة</th>
<th align="right">الوظيفة</th>
<th align="right">الطول</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>اللوجلاين</strong></td>
<td>جملة واحدة</td>
<td>سطر</td>
</tr>
<tr>
<td><strong>الملخص</strong></td>
<td>المفاصل الدرامية</td>
<td>٤ أسطر–١٫٥ صفحة</td>
</tr>
<tr>
<td><strong>المعالجة</strong></td>
<td>القصة كاملة بلا حوار</td>
<td>١٠–٢٠ صفحة</td>
</tr>
<tr>
<td><strong>السيناريو</strong></td>
<td>مشاهد وحوار</td>
<td>٩٠–١٢٠ صفحة</td>
</tr>
</tbody>
</table>
<br clear="all">

### مسار العمل

<pre dir="rtl"><code>
① النوع والجمهور
        ↓
② اللوجلاين
        ↓
③ الملخص
        ↓
④ المعالجة
        ↓
⑤ خريطة المشاهد
        ↓
⑥ السيناريو
        ↓
⑦ المراجعة
        ↓
⑧ التنسيق
</code></pre>

### قبل/بعد

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">قبل</th>
<th align="right">بعد</th>
<th align="right">السبب</th>
</tr>
</thead>
<tbody>
<tr>
<td>«أنا مقصر لأنني أعمل كثيراً»</td>
<td>طبق ثالث لم يُلمس</td>
<td>أرِ ولا تروِ</td>
</tr>
<tr>
<td>«يشعر بالحزن»</td>
<td>«يضع يده على كتفها، ثم يسحبها»</td>
<td>فعل بدل تفسير</td>
</tr>
<tr>
<td>ينتظر ثم يأتي الأخ</td>
<td>يدخل على الطبق الثالث</td>
<td>دخول متأخر</td>
</tr>
<tr>
<td>«شكراً / لا شكر»</td>
<td>يأكل من طبق أخيه</td>
<td>خروج بالفعل</td>
</tr>
</tbody>
</table>
<br clear="all">

---

## 📚 المراجع والاعتماد

* **«السيناريو»** — سيد فيلد — ترجمة دار المأمون، بغداد، ١٩٨٩:
  <https://archive.org/details/moharram1965_gmail_20170615_0228>
* **«فن كتابة السيناريو»** — فرانك هارو — ترجمة رانيا قرداحي:
  <https://archive.org/details/ELshandawily0124>
* **«كيف تكتب السيناريو»** — صلاح أبو سيف — الموسوعة الصغيرة:
  <https://archive.org/details/ELshandawily0079>

> **إقرار بالفضل:** هذه المهارة صياغة تعليمية مستقلة لمبادئ الكتب الثلاثة، مع نقل اقتباسات محدودة بإسنادها إلى صفحاتها. ولا يتضمّن المستودع نسخاً كاملة من الكتب، ولا يُغني عن الرجوع إلى الأصل.

---

## ⚠️ حدود المسؤولية

- المهارة **لبناء السيناريو وتحريره**، لا لنسخ سيناريوهات قائمة.
- لا تختلق وقائع تاريخية في الأعمال المبنية على أحداث حقيقية.
- لا تُشهّر بشخص حقيقي ولا تنسب إليه جريمة بلا بينة.
- لا تُقدّم استشارة قانونية في الحقوق؛ راجع مختصاً قبل الإنتاج.
- المستخدم مسؤول عن مراجعة النص النهائي وحقوق الاقتباس.

---

## 🤝 المساهمة

نرحب بالمساهمات التي تحسّن المادة أو التحرير أو التوثيق. اقرأ [CONTRIBUTING.md](CONTRIBUTING.md) قبل فتح طلب سحب، والتزم بـ[قواعد السلوك](CODE_OF_CONDUCT.md).

## 🛡️ الأمان

إن وجدت مشكلة أمنية، فلا تفتح قضية عامة؛ راجع [SECURITY.md](SECURITY.md).

## 📄 سجل التغييرات

راجع [CHANGELOG.md](CHANGELOG.md) لمعرفة ما أُضيف في كل إصدار.

## 📬 الدعم

للأسئلة والاقتراحات: [افتح قضية](https://github.com/specailm5/arabic-screenwriting-skill/issues).

---

## 📜 الترخيص (License)

هذه المهارة مفتوحة المصدر تحت رخصة [MIT](LICENSE)، ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم اللغة العربية.
