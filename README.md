# Quotex Bot Website

SEO-optimized Astro website for Quotex Bot Chrome Extension.

## Pages
- `/` — Homepage
- `/features` — Full features breakdown
- `/how-it-works` — Step-by-step guide
- `/pricing` — Free demo vs $20/month live
- `/faq` — 30+ FAQ with schema markup
- `/blog` — Blog index
- `/blog/quotex-martingale-strategy-guide` — SEO article
- `/blog/how-to-use-quotex-bot` — Tutorial article
- `/privacy-policy` — Privacy policy

## Deployment to Vercel

1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → Import your repo
3. Framework: Astro (auto-detected)
4. Click Deploy

## Connect Domain
1. Vercel Dashboard → Your Project → Settings → Domains
2. Add your domain (e.g. quotexbot.com)
3. Update DNS at your domain registrar with Vercel's nameservers

## Google Search Console
1. Go to search.google.com/search-console
2. Add property → URL prefix → https://quotexbot.com
3. Verify with HTML tag method (add to Layout.astro head)
4. Submit sitemap: https://quotexbot.com/sitemap-index.xml

## Google Analytics
1. Go to analytics.google.com → Create property
2. Get measurement ID (G-XXXXXXXXXX)
3. Add to Layout.astro before </head>:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## Update Before Launch
- Replace `quotexbot.com` with your actual domain in astro.config.mjs and Layout.astro
- Add real OG image at /public/og-image.jpg (1200x630px)
- Add logo at /public/logo.png
- Update WhatsApp group link in Footer.astro
- Add Google Analytics measurement ID
- Add Google Search Console verification tag
