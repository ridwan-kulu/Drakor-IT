# Drakor IT

![Preview](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfmTkrilNem0UuFEXli8z84DbuW8pR60zGvQeVChbWZqrev_NRSe9MhyRnP8KOC0SEjwiszSUtpLdedOnfZ9S037mRNhqoyIYI43dJanRNBaOT4pFaSj9SyC3Ru34ddYw0iFM9szyq-Vy38kgDDY9QPt3z8FP4WxeoRpq1fGouxDYCa1R1m2RPUbjOG-0/s1600/355748.jpg)


Drakor IT adalah katalog streaming drama Korea, film Asia, series ongoing, dan movie populer dengan tampilan sinematik berbasis liquid glass. Situs ini dirancang untuk pengalaman discovery yang cepat, mobile-friendly, SEO-ready, dan nyaman digunakan untuk mencari tontonan subtitle Indonesia.

Live site: [https://drakor-it.vercel.app](https://drakor-it.vercel.app)

## Kenapa Drakor IT?

Drakor IT dibuat untuk memberi pengalaman browsing yang lebih premium dibanding katalog streaming biasa. Tampilan menggunakan glassmorphism, poster card responsif, homepage kurasi, halaman detail informatif, watch page dengan riwayat tontonan, rating pengguna, komentar, bookmark, dan metadata SEO yang siap diindeks mesin pencari.

Fokus utama proyek ini:

- Discovery cepat untuk drama Korea, movie, series ongoing, completed, dan top-rated.
- UI liquid glass yang modern, responsif, dan nyaman di desktop maupun ponsel.
- Halaman detail yang kaya informasi: poster, genre, rating, metadata, cast, episode, komentar, dan rekomendasi.
- Pengalaman pengguna login: watchlist, history, rating, dan komentar.
- SEO lengkap: metadata dinamis, Open Graph image, canonical URL, robots.txt, dan sitemap.xml dinamis.

## Fitur Utama

- Homepage sinematik dengan hero featured, live pulse, new releases, popular series, top rated, dan continue watching.
- Poster card berbasis data API: title, episode, status, type, year, resolution, poster, dan rating tampil rapi tanpa teks terpotong di mobile.
- Detail page liquid glass dengan poster showcase, CTA watch, metadata cards, episode rail, rating panel, komentar, cast, dan rekomendasi.
- Watch page dengan server player, episode navigation, playback info, media details, rating, komentar, dan rekomendasi.
- Header dan footer modern dengan hover glass, announcement panel, search, auth navigation, dan social/contact links.
- SEO dan indexing: `app/robots.ts` dan `app/sitemap.ts` menghasilkan `/robots.txt` dan `/sitemap.xml` secara dinamis.
- PWA/site assets: favicon, manifest, Apple touch icon, dan logo navbar.
- Supabase integration untuk auth, comments, ratings, watch history, watchlist, dan admin data.

## Tech Stack

- Next.js 16 App Router
- React 19
- TypeScript
- Tailwind CSS
- Supabase SSR dan Supabase JS
- Motion for React
- Lucide React icons
- Vercel deployment

## SEO

Proyek ini sudah disiapkan agar bisa diindeks mesin pencari:

- Dynamic metadata per halaman.
- Canonical URL.
- Open Graph dan Twitter card.
- Dynamic OG image route.
- `robots.txt` mengizinkan crawler mengakses halaman publik.
- `sitemap.xml` dinamis berisi halaman utama dan item katalog dari API.
- Private routes seperti `/admin`, `/profile`, `/api`, dan auth/reset routes tidak diprioritaskan untuk crawling.

Endpoint SEO:

- [https://drakor-it.vercel.app/robots.txt](https://drakor-it.vercel.app/robots.txt)
- [https://drakor-it.vercel.app/sitemap.xml](https://drakor-it.vercel.app/sitemap.xml)

## Menjalankan Lokal

Install dependencies:

```bash
npm install
```

Buat `.env` berdasarkan kebutuhan project:

```bash
NEXT_PUBLIC_SITE_URL=http://localhost:3000
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=your_supabase_publishable_key
```

Jalankan development server:

```bash
npm run dev
```

Buka `http://localhost:3000`.

## Scripts

```bash
npm run dev
npm run build
npm run start
npm run lint
```

## Deployment

Project ini sudah terhubung ke Vercel dan production deploy tersedia di:

[https://drakor-it.vercel.app](https://drakor-it.vercel.app)

Deploy manual:

```bash
npx vercel deploy --prod --yes
```

## Struktur Penting

```text
app/
  page.tsx          Homepage
  robots.ts         Dynamic robots.txt
  sitemap.ts        Dynamic sitemap.xml
  api/og/route.tsx  Dynamic Open Graph image
components/
  header.tsx        Header liquid glass
  footer.tsx        Footer liquid glass
  poster-card.tsx   Card katalog responsif
  detail-view.tsx   Detail dan watch page layout
lib/
  api.ts            API client dan tipe katalog
  seo.tsx           Metadata, canonical, OG, JSON-LD helpers
  supabase/         Auth dan data integration
```

## Tentang Situs

Drakor IT cocok untuk pengguna yang ingin menemukan drama Korea dan film Asia dengan cepat, tampilan bersih, dan informasi yang mudah dipahami. Desainnya dibuat mobile-first, dengan card poster yang mengikuti data asli dari API dan layout yang tetap rapi di layar kecil.

Kunjungi situsnya di [drakor-it.vercel.app](https://drakor-it.vercel.app) dan temukan drama, movie, ongoing series, completed titles, serta rekomendasi tontonan terbaru.
