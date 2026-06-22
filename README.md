# AlMaqam Design System
## دليل نظام التصميم — للفريق UI/UX

> **المشروع:** almqam-web  
> **التاريخ:** يونيو 2026  
> **المصدر:** مستخرج من الكود الحالي (`src/globals.css` + `src/app/(components)/ui/`)  
> **الاستخدام:** مرجع للتصميم في Figma + توحيد الواجهة مع التطوير

---

## 1. نظرة عامة

| البند | القيمة |
|-------|--------|
| المنصة | Web — Next.js 16 |
| مكتبة المكوّنات | shadcn/ui (style: `radix-mira`) |
| الأيقونات | Lucide React |
| CSS | Tailwind CSS 4 |
| الخط | Zain (Google Fonts) |
| اللغات | العربية (RTL) + الإنجليزية (LTR) |
| الوضع الافتراضي | Light Mode |

**ملفات مرجعية في المشروع:**
- `src/globals.css` — الألوان، الظلال، الأنماط العامة
- `src/app/(components)/ui/` — مكوّنات الواجهة
- `docs/design-tokens.json` — Tokens جاهزة للاستيراد في Figma

---

## 2. الألوان (Color Palette)

### 2.1 Brand — الألوان الأساسية

| الاسم | Hex | الاستخدام |
|-------|-----|-----------|
| **Primary** | `#DC340A` | أزرار CTA، روابط، تحديد، scrollbar |
| **Primary Hover** | `#C02E09` | hover على الأزرار الأساسية |
| **Primary Dark** | `#A32607` | حالات pressed / أغمق |

### 2.2 Backgrounds — الخلفيات

| الاسم | Hex | الاستخدام |
|-------|-----|-----------|
| **Page Background** | `#ECEEF2` | خلفية الصفحة الرئيسية |
| **Surface Light** | `#F8F8F8` | خلفيات ثانوية |
| **Surface White** | `#FFFFFF` | كروت، نماذج، modals |
| **Input Background** | `#ECEEF2` | حقول الإدخال |
| **Tab List** | `#ECEEF2` | خلفية شريط التبويبات |
| **Car Card Image** | `#F2F2F2` | خلفية صورة السيارة |

### 2.3 Neutrals — الرمادي والنص

| الاسم | Hex | الاستخدام |
|-------|-----|-----------|
| **Gray Light** | `#E8E8E8` | حدود خفيفة |
| **Gray Medium** | `#9E9E9E` | نص muted |
| **Gray Dark** | `#757575` | نص ثانوي |
| **Text Primary** | `#333333` | نص أساسي (token) |
| **Text Secondary** | `#666666` | نص ثانوي (token) |
| **Heading** | `#1A1A1A` | عناوين ونص قوي — الأكثر استخداماً |
| **Body Muted** | `#595959` | نص ثانوي في الحجز والبروفايل |
| **Body Alt** | `#393838` | نص في قوائم السيارات |
| **Footer** | `#1A1A1A` | خلفية الفوتر |
| **Border Subtle** | `#CDCDCD` | حدود dialog header |
| **Divider** | `#1A1A1A` | فواصل عمودية |

### 2.4 Semantic — ألوان دلالية

| الاسم | Hex | الاستخدام |
|-------|-----|-----------|
| **Success** | `#177E64` | دفع ناجح / تأكيد |
| **Warning** | `#B8860B` | تحذير |
| **Warning BG** | `#FFF8E6` | خلفية تحذير |
| **Error** | `#DC2626` | خطأ / فشل |
| **Error BG** | `#FEF2F2` | خلفية خطأ |
| **Destructive** | `oklch(0.58 0.22 27)` | حذف / إجراءات خطرة |
| **Overlay** | `#000000` @ 30% | خلفية الـ modal |
| **Selection** | `rgba(250, 100, 9, 0.3)` | تحديد النص |

### 2.5 Gradients — التدرجات

#### Soft Button / Navbar / Logo
```
Background: linear-gradient(180deg, #F4F4F4 0%, #FEFEFE 100%)
Border:     linear-gradient(180deg, #FFFFFF 0%, #ECECEC 100%)
```

#### Referral Card — Outer
```
linear-gradient(180deg, #FFFFFF 0%, #ECECEC 100%)
```

#### Referral Card — Inner
```
linear-gradient(180deg, #F4F4F4 0%, #FEFEFE 100%)
```

#### Avatar Border
```
linear-gradient(303.36deg, #FFFFFF -15.63%, #F5A600 123.85%)
```

---

## 3. Typography — الخطوط

### 3.1 Font Family

| البند | القيمة |
|-------|--------|
| **الخط** | Zain |
| **المصدر** | Google Fonts |
| **Subsets** | Arabic, Latin |
| **CSS Variable** | `--font-zain` |

### 3.2 Font Weights

| الوزن | القيمة | الاستخدام |
|-------|--------|-----------|
| Extra Light | 200 | نادر |
| Light | 300 | نادر |
| Regular | 400 | النص الأساسي، labels، dialogs |
| Bold | 700 | عناوين، tabs نشطة، أرقام |

### 3.3 Type Scale — مقياس النص

| الاسم | Size | Weight | Line Height | الاستخدام |
|-------|------|--------|-------------|-----------|
| Display XL | 60px | 700 | tight | Hero — desktop |
| Display LG | 48px | 700 | tight | Hero — tablet |
| Display MD | 36px | 700 | tight | Hero — mobile |
| H1 | 24–30px | 700 | normal | عناوين الأقسام |
| H2 | 18px | 400 | normal | عناوين Dialog |
| H3 | 16–18px | 700 | normal | عناوين الكروت |
| Body LG | 16px | 400–500 | relaxed | نص أساسي كبير |
| Body MD | 14px | 400 | relaxed | **الافتراضي** — inputs, tabs, body |
| Body SM | 12px | 400–500 | normal | نص صغير، labels فرعية |
| Caption | 10px | 500 | normal | Badges |
| Counter | 24px | 700 | normal | عداد الأيام في الفلتر |

---

## 4. Spacing — المسافات

### 4.1 Scale

| Token | Value | الاستخدام |
|-------|-------|-----------|
| `space-1` | 4px | gaps صغيرة |
| `space-2` | 8px | padding داخلي صغير |
| `space-3` | 12px | gaps متوسطة |
| `space-4` | 16px | padding كروت — mobile |
| `space-6` | 24px | padding كروت — desktop |
| `space-8` | 32px | — |
| `space-15` | 60px | `.space-custom` — بين الأقسام |
| `space-21` | 84px | margin جانبي desktop |

### 4.2 Layout

| العنصر | Mobile | Desktop |
|--------|--------|---------|
| Container margin | 16px (`mx-4`) | 84px (`mx-[84px]`) |
| Ultra-wide (2400px+) | — | 400px margin |
| Section vertical | 60px | 60px |
| Card padding | 16px | 24px |
| Dialog header | 16px horizontal, 12px vertical | نفس |

---

## 5. Border Radius — الانحناءات

| Token | Value | الاستخدام |
|-------|-------|-----------|
| `radius-sm` | 4px | عناصر صغيرة جداً |
| `radius-md` | 6px | — |
| `radius-lg` | 8px | Cards, inputs base |
| `radius-button` | **10px** | الأزرار |
| `radius-input` | **8px** | حقول الإدخال |
| `radius-tab` | 8–12px | التبويبات |
| `radius-calendar` | **12px** | أيام التقويم |
| `radius-card` | **18px** | بطاقات السيارات |
| `radius-surface` | **20px** | Dialogs, فلاتر, صور السيارات |
| `radius-pill` | 20px | Language switcher |
| `radius-full` | 9999px | Avatar, badges |

---

## 6. Shadows — الظلال

### Shadow / Elevation 1 — Card
```
0px 2px 8px 0px rgba(88, 88, 88, 0.10)   /* #5858581A */
```
**الاستخدام:** كروت الفلتر، Rental Duration Card, Navbar

### Shadow / Elevation 2 — Soft Button
```
0px 6px 12px rgba(0, 20, 37, 0.12)
0px 2px 4px rgba(0, 20, 37, 0.08)
```
**الاستخدام:** `.btn-soft`, navbar logo

### Shadow / Elevation 3 — MD
```
0px 0.9px 3.6px 0.9px rgba(0, 20, 37, 0.12)
0px 0px 0.22px 0.67px rgba(0, 0, 0, 0.05)
0px 0px 0.22px 0.22px rgba(0, 0, 0, 0.07)
0px 3px 6px 0px rgba(0, 20, 37, 0.15)
```
**الاستخدام:** `.shadow-md`

### Shadow / Referral Card
```
0px 3px 6px 0px rgba(0, 20, 37, 0.15)
```

### Tab Active
```
0px 1px 2px rgba(0, 0, 0, 0.05)  /* shadow-sm */
```

---

## 7. Components — المكوّنات

### 7.1 Button

#### Variants
| Variant | المظهر |
|---------|--------|
| **Default** | خلفية Primary `#DC340A` + نص أبيض |
| **Outline** | حدود + خلفية شفافة |
| **Secondary** | خلفية رمادية فاتحة |
| **Ghost** | بدون خلفية، hover رمادي |
| **Destructive** | أحمر شفاف |
| **Link** | نص Primary + underline |

#### Sizes
| Size | Height | Font |
|------|--------|------|
| XS | 24px | 10px |
| Default | 28px | 12px |
| SM | 32px | 12px |
| LG | 40px | 12px |
| Icon | 28×28px | — |
| Icon LG | 32×32px | — |

**Specs:** Border radius `10px` · Transition `all` · Disabled `opacity 50%`

---

### 7.2 Soft Button (`.btn-soft`)

مكوّن مخصص — ليس shadcn standard.

| الخاصية | القيمة |
|---------|--------|
| Background | gradient `#F4F4F4` → `#FEFEFE` |
| Border | 1.8px gradient `#FFFFFF` → `#ECECEC` |
| Text | `#1A1A1A` |
| Shadow | Elevation 2 |
| Hover | بدون shadow + border `#ECEEF2` |
| Transition | 400ms ease-in-out |
| Disabled | opacity 50% |

---

### 7.3 Input

| Size | Height |
|------|--------|
| SM | 28px |
| MD | 40px (default) |
| LG | 44px |

| الخاصية | القيمة |
|---------|--------|
| Background | `#ECEEF2` / `bg-input/20` |
| Border radius | 8px |
| Font size | 14px |
| Focus ring | 2px, color ring token |
| Label | 14px, weight 500 |

**يدعم:** start/end icon · start/end button · password toggle · RTL

---

### 7.4 Card

| الخاصية | القيمة |
|---------|--------|
| Background | `#FFFFFF` |
| Border | 1px ring `foreground/10%` |
| Radius | 8px |
| Padding | 16px vertical, 16px horizontal |
| Title | 14px, weight 500 |
| Description | 12px, muted color |

---

### 7.5 Dialog / Modal

| الخاصية | القيمة |
|---------|--------|
| Overlay | `#000000` @ 30% |
| Content radius | 20px |
| Title | 18px, weight 400, `#000` |
| Header border | 0.5px `#CDCDCD` |
| Max width | ~512px (`max-w-lg`) |
| Animation enter | 700ms, slide from bottom + scale |
| Animation exit | 500ms |
| Easing | `cubic-bezier(0.16, 1, 0.3, 1)` |

---

### 7.6 Tabs

| الحالة | المظهر |
|--------|--------|
| **List** | خلفية `#ECEEF2`, radius 8px, padding 4px |
| **Active** | خلفية بيضاء, bold, shadow-sm |
| **Inactive** | `#6B7280` (gray-600) |
| **Hover inactive** | `#1A1A1A` (gray-900) |
| Font | 14px |
| Padding | 8px vertical, 16px horizontal |

---

### 7.7 Badge

| الخاصية | القيمة |
|---------|--------|
| Height | 20px |
| Font | 10px, weight 500 |
| Shape | Pill (full radius) |
| Padding | 8px horizontal |

Variants: default · secondary · destructive · outline · ghost · link

---

### 7.8 Date Picker (Calendar)

| الحالة | المظهر |
|--------|--------|
| Default day | 14px, radius 12px |
| Hover | `#ECEEF2` |
| Selected | Primary bg + white text |
| Range start/end | Primary bg + white text |
| Range middle | `#F2F2F2` bg, `#1A1A1A` text |
| Disabled | line-through, `#1A1A1A` @ 40% |

---

### 7.9 Time Slot Selector

| الحالة | المظهر |
|--------|--------|
| Default | 36px height, 12px font |
| Selected | Primary border + `primary/3%` bg, bold `#1A1A1A` |

---

### 7.10 Car Card

| الخاصية | القيمة |
|---------|--------|
| Radius | 18px |
| Background | `#FFFFFF` |
| Image area | `#F2F2F2` |
| Border default | `#FFFFFF` |
| Border hover | `#ECEEF2` |
| Shadow | gray-200 |

---

### 7.11 Footer

| الخاصية | القيمة |
|---------|--------|
| Background | `#1A1A1A` |
| Text | `#FFFFFF` |
| Top margin | 32px mobile / 60px desktop |

---

## 8. Motion — الحركة والأنيميشن

### Easing الأساسي
```
cubic-bezier(0.16, 1, 0.3, 1)
```

### Durations
| العنصر | Enter | Exit |
|--------|-------|------|
| Dialog | 700ms | 500ms |
| Dialog overlay | 700ms | 500ms |
| Login tabs | 350ms | — |
| Soft button hover | 400ms | — |
| Calendar day | 300ms | — |

### Login Tab Interactions
- Hover inactive: `scale(1.03)`
- Active: subtle bounce `scale(0.98)` → `scale(1.02)` → `scale(1)`
- Icon active: pulse animation

### Hover Effects شائعة
- App store badges: `scale(1.05)`
- Buttons: background color transition

---

## 9. Icons — الأيقونات

| البند | القيمة |
|-------|--------|
| Library | Lucide React |
| Default in buttons | 14px |
| Default in inputs | 16px |
| Tab icons | inline, shrink-0 |

---

## 10. Scrollbars

### Global
| الجزء | اللون |
|-------|-------|
| Width | 7px |
| Track | `#ECEEF2` |
| Thumb | `#DC340A` (Primary) |
| Thumb hover | `#162A2B` |

### Time Slot
- Width: 6px · Thumb: `#B8BCC0` · Track: `#F5F5F5`

### Booking Details
- Width: 5px · Thumb: `#aab0bc` · Track: `#ffffff`

---

## 11. Breakpoints — نقاط التوقف

| Name | Min Width | ملاحظات |
|------|-----------|---------|
| Mobile | 0 | Bottom nav, padding أقل |
| `sm` | 640px | — |
| `md` | 768px | Container 84px margin |
| `lg` | 1024px | Layouts أوسع |
| `xl` | 1280px | Hero text أكبر |
| `2xl` | 1536px | — |
| Ultra-wide | 2400px | Container 400px margin |

---

## 12. RTL / Localization

| البند | القيمة |
|-------|--------|
| العربية | `dir="rtl"`, text-align right |
| الإنجليزية | `dir="ltr"`, text-align left |
| Icons/Inputs | padding معكوس تلقائياً |
| Scrollbar booking | forced LTR للـ scrollbar |

---

## 13. قائمة المكوّنات الكاملة

```
Button · Input · Textarea · Label · Field
Card · Badge · Tabs · Dialog · Drawer · Alert Dialog
Select · Combobox · Checkbox · Radio Group
Date Picker · Time Slot Selector · Input OTP
Breadcrumb · Carousel · Popover · Dropdown Menu
Separator · Image · Sonner (Toast) · Filter Section Trigger
```

---

## 14. استيراد في Figma

> **الملف الجاهز:** `docs/figma-tokens/` — صيغة Tokens Studio للاستيراد المباشر

1. ثبّت plugin **Tokens Studio for Figma**
2. Import → اختر مجلد `docs/figma-tokens/`
3. Export to Figma → Variables + Text Styles + Effect Styles
4. راجع `docs/figma-tokens/README.md` للخطوات التفصيلية

ملف بديل (W3C format): `docs/design-tokens.json`

### هيكل Figma المقترح
```
📁 AlMaqam Design System
├── 🎨 Colors / Brand
├── 🎨 Colors / Neutrals
├── 🎨 Colors / Semantic
├── 🔤 Typography / Zain
├── 📐 Spacing
├── 🔲 Radius
├── 🌫️ Shadows
├── 🎭 Gradients
├── 🧩 Components
│   ├── Button
│   ├── Soft Button
│   ├── Input
│   ├── Card
│   ├── Dialog
│   ├── Tabs
│   ├── Badge
│   ├── Date Picker
│   └── Car Card
└── 📱 Breakpoints
```

---

## 15. ملاحظات للمصمم

1. **Primary `#DC340A`** هو لون البراند الرسمي — موجود في Figma أصلاً
2. **خلفية الصفحة `#ECEEF2`** ليست بيضاء — مهم في التصميم
3. التطبيق **Light-first** — Dark mode معرّف لكن غير مستخدم بشكل أساسي
4. الخط **Zain** إلزامي للعربية والإنجليزية
5. الأزرار تستخدم **radius 10px** وليس 8px
6. الـ Dialogs تستخدم **radius 20px**
7. `.btn-soft` نمط مخصص مهم في Navbar والأزرار الثانوية

---

*آخر تحديث: يونيو 2026 — مُستخرج من فرع التطوير الحالي*
