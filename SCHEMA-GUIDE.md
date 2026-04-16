# دليل Schema Markup لـ gifts-flower.com

## ما هو Schema Markup؟
Schema Markup = بيانات منظمة تساعد Google يفهم موقعك أفضل ويعرض نتائج أغنى (Rich Snippets)

---

## 1. Organization Schema (للموقع كامل)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "متجر فلاور - محل ورد مكة",
  "alternateName": "Flower Gifts",
  "url": "https://gifts-flower.com",
  "logo": "https://cdn.salla.sa/vXwXwB/bVrO7sRo84BN7zzc7YzYSUXdMadna5qX1SFu1Tce.png",
  "description": "متجر ورد وهدايا في مكة المكرمة - توصيل مكة جدة الطائف",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "مكة المكرمة",
    "addressCountry": "SA"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "21.4225",
    "longitude": "39.8262"
  },
  "telephone": "+966551254922",
  "email": "flower.gifts2030@gmail.com",
  "sameAs": [
    "https://www.instagram.com/s7op_flower",
    "https://twitter.com/s7op_flower",
    "https://www.snapchat.com/add/s7op_flower",
    "https://www.tiktok.com/@s7op_flower"
  ]
}
</script>
```

---

## 2. LocalBusiness Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Florist",
  "name": "متجر فلاور - ورد مكة",
  "image": "https://cdn.salla.sa/vXwXwB/bVrO7sRo84BN7zzc7YzYSUXdMadna5qX1SFu1Tce.png",
  "url": "https://gifts-flower.com",
  "telephone": "+966551254922",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "",
    "addressLocality": "مكة المكرمة",
    "addressRegion": "مكة",
    "postalCode": "24231",
    "addressCountry": "SA"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "21.4225",
    "longitude": "39.8262"
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday", "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday"],
      "opens": "09:00",
      "closes": "23:00"
    }
  ],
  "priceRange": "$$",
  "acceptsReservations": "False"
}
</script>
```

---

## 3. FAQPage Schema (أسئلة شائعة)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "هل توفّرون توصيل هدايا في مكة؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "نعم، نوصل هدايا وورد في مكة المكرمة وجدة والطائف. التوصيل مجاني في مكة."
      }
    },
    {
      "@type": "Question",
      "name": "ما هي مناطق التوصيل؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "نوصل في مكة المكرمة وجدة والطائف وجميع المناطق المحيطة."
      }
    },
    {
      "@type": "Question",
      "name": "هل يوجد توصيل نفس اليوم؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "نعم، نوفر توصيل_same_day في مكة المكرمة للطلبات قبل الساعة 5 مساءً."
      }
    },
    {
      "@type": "Question",
      "name": "ما هي طرق الدفع المتاحة؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "نقبل: تابي، تمارا، بطاقة ائتمان، PayPal، STC Pay، تحويل بنكي"
      }
    }
  ]
}
</script>
```

---

## 4. Product Schema (لكل منتج)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "[اسم المنتج]",
  "image": "[رابط صورة المنتج]",
  "description": "[وصف المنتج]",
  "sku": "[SKU المنتج]",
  "brand": {
    "@type": "Brand",
    "name": "متجر فلاور"
  },
  "offers": {
    "@type": "Offer",
    "url": "[رابط المنتج]",
    "priceCurrency": "SAR",
    "price": "[السعر]",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "Organization",
      "name": "متجر فلاور"
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "156"
  }
}
</script>
```

---

## 📍 طريقة الإضافة:

### الطريقة 1: Google Tag Manager (الأسهل)
1. ادخل GTM
2. أنشئ Tag جديد → Custom HTML
3. لصق الكود
4. اضبط Trigger = All Pages
5. Publish

### الطريقة 2: Salla Theme
1. لوحة تحكم سلة → المظهر → Edit Code
2. افتح ملف `theme.liquid` أو `footer`
3. لصق الكود قبل `</head>`

---

## ✅ المهام المطلوبة:
- [ ] إضافة Organization Schema ✅ (موجود)
- [ ] إضافة LocalBusiness Schema ⬜
- [ ] إضافة FAQPage Schema ⬜
- [ ] التأكد من Product Schema ⬜

