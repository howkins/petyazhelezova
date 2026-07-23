# Уебсайт — Логопед Петя Железова

Статичен сайт (HTML/CSS/vanilla JS), готов за качване на **Vercel** без build стъпка.

## Структура
```
site/
├── index.html        # цялата страница
├── assets/           # лого, снимки
├── robots.txt        # индексиране за търсачки
├── sitemap.xml       # карта на сайта
└── vercel.json       # cache + сигурност хедъри
```

## Качване на Vercel
1. Създай проект в [vercel.com](https://vercel.com) и качи папката `site/` (или я свържи с GitHub repo).
2. Framework preset: **Other** · Output/Root directory: `site` · без build команда.
3. Deploy — готово.

## ⚠️ Преди пускане: смени домейна
Навсякъде в проекта е поставен временен адрес **`https://petya-zhelezova.vercel.app/`**.
След като имаш реален домейн, замени го в:
- `index.html` — таговете `canonical`, `og:*`, `twitter:*` и JSON-LD блока
- `robots.txt` — реда `Sitemap:`
- `sitemap.xml` — `<loc>`

## Добавяне на домейн (petyazhelezova.bg)
1. В Vercel dashboard → проекта → **Settings → Domains** → въведи `petyazhelezova.bg` → Add.
2. Vercel ще покаже DNS записи, които трябва да добавиш при регистратора на домейна:
   - **Apex домейн (petyazhelezova.bg)**: A record → `76.76.21.21`
   - Или Nameservers: смяна към Vercel-ните NS сървъри (по-лесно, ако регистраторът позволява)
   - **www поддомейн (www.petyazhelezova.bg)**: CNAME → `cname.vercel-dns.com`
3. При регистратора на .bg домейна (напр. Register.BG, SuperHosting) → DNS управление → добави записите точно както ги покаже Vercel (те са специфични за проекта, затова гледай реалния екран, не преписвай стойностите сляпо).
4. Изчакай пропагация (минути до няколко часа) — Vercel автоматично издава SSL сертификат щом провери домейна.
5. Не забравяй да смениш временния адрес `https://petya-zhelezova.vercel.app/` с `https://petyazhelezova.bg/` навсякъде, описано в секцията по-долу.

## SEO включено
- Title, meta description, keywords, canonical, robots
- Open Graph + Twitter Card (споделяне във Facebook, Viber, LinkedIn, X)
- JSON-LD структурирани данни (LocalBusiness + MedicalBusiness / SpeechPathology) → богати резултати в Google, карти, локално търсене
- Гео-тагове за София, sitemap.xml, robots.txt

## След пускане
- Регистрирай сайта в [Google Search Console](https://search.google.com/search-console) и подай `sitemap.xml`.
- За OG изображение при споделяне се ползва `assets/hero.jpg` (препоръка: подготви версия 1200×630 px).
