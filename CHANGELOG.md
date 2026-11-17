# Änderungsprotokoll – hofmetzgerei-kronseder.de

Kunde: Hofmetzgerei Kronseder, Wambach / Vils
Live-Adresse: https://hofmetzgerei-kronseder.de/

Neueste Version oben. Jede Version hat in Git einen gleichnamigen Tag (z. B. `v59_01`).
Hochgeladen wird nur der Inhalt von `site/` (mit `.htaccess`).

## Unveröffentlicht
- –

## V59_01 – 13.11.2026 (Basis: V59_00)
- **Bilder:** alle Fotos und Logos als WebP, Seitenbilder gesamt ca. 3,4 MB → 0,7 MB; `width`/`height` bei allen Bildern; `hof.jpg` und alte JPG/PNG entfernt; neu `assets/og-image.jpg` (1200 × 630).
- **SEO:** Titel „Hofmetzgerei & Hofladen in Wambach / Vils | Kronseder“, Open Graph und Twitter-Card, JSON-LD `Butcher` (Adresse, Telefon, E-Mail, Fr 11–18, Sa 07:30–12:00), neu `robots.txt` und `sitemap.xml`.
- **Gestaltung:** `--rust` #bf4b2f → #b04327 (Kontrast 4,26:1 → 4,93:1), sichtbarer Fokusrahmen, `prefers-reduced-motion`.
- **Server:** `404.html` (noindex) und `ErrorDocument 404`, Komprimierung, Browser-Cache, MIME-Typen für `.webp`/`.webmanifest`.

## V59_00 – 13.11.2026
- Sechs Sicherheits-Header in der `.htaccess` (HSTS ohne `includeSubDomains`, CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy).
- Inline-Styles in `site-overrides.css` ausgelagert (CSP ohne `unsafe-inline`).
- Dauerhafte Weiterleitung auf https und `hofmetzgerei-kronseder.de`; Canonical auf allen drei Seiten.
- Hero und Preload auf `hof-web.jpg` umgestellt.
- (Ausgangsstand „Archiv.zip“ nur als Beschreibung, nicht in Git.)

## Offen
- Impressum: Kammer, Berufsbezeichnung, USt-IdNr., Streitbeilegung, Stand.
- Inhalte: Gaststuben-Zeiten, „EM-Produkte“, Datum bei „Aktuell“, Samstag (Markt Vilsbiburg 07:00–12:00 und Hofladen 07:30–12:00).
- Datenschutzerklärung: Mailanbieter ergänzen.
