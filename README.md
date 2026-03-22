# Gantry 5 Particles

Zbiór gotowych cząstek (particles) dla **Gantry 5** na **Joomla 5+ / 6+**.

Każda cząstka to dwa pliki — kopiujesz je do swojego szablonu i konfigurujesz przez panel admina Gantry bez dotykania kodu.

---

## Instalacja (każda cząstka)

1. Skopiuj pliki cząstki do katalogu swojego szablonu:
   ```
   templates/{nazwa_szablonu}/custom/particles/nazwa.yaml
   templates/{nazwa_szablonu}/custom/particles/nazwa.html.twig
   ```
2. Wyczyść cache Gantry: **Gantry 5 → Clear Cache**
3. W Layout Managerze przeciągnij cząstkę w wybrane miejsce layoutu

---

## Dostępne cząstki

### Menu Bootstrap

> `particles/menu_bootstrap.yaml` + `particles/menu_bootstrap.html.twig`

Pełnoprawna nawigacja Joomla oparta na **Bootstrap 5.3** z offcanvas na mobile. Zastępuje domyślną cząstkę Menu w Gantry 5.

**Funkcje:**
- Nawigacja desktopowa z wielopoziomowymi dropdownami
- Panel offcanvas na mobile (hamburger → panel boczny)
- Responsywne podwójne logo — osobne dla desktop i mobile
- Tryby sticky: brak / sticky / scroll-up / fixed
- Zmniejszanie logo przy scrollu
- Ikony social media w navbarze i offcanvas
- Własny hamburger (ikona Font Awesome lub obrazek)
- Typografia: Google Fonts, rozmiar, grubość, transformacja, letter-spacing, odstępy
- Kolory i szerokość offcanvas dziedziczone z Gantry Styles → Offcanvas Styles
- Kolory dropdownów niezależne od navbara
- Dostępność zgodna ze standardami WCAG (aria-label, aria-expanded, offcanvas-title i in.)

**Wymagania:** Joomla 5+ / 6+, Gantry 5, szablon z Bootstrap 5 (np. Helium)

> Bootstrap 5.3 jest wbudowany w Joomla 5+ — cząstka ładuje go z `/media/vendor/bootstrap/`, nie wymaga dodatkowej instalacji.

### Gallery Lightbox

> `particles/gallery_lightbox.yaml` + `particles/gallery_lightbox.html.twig` + `particles/js/bs5-lightbox.bundle.min.js`

Galeria zdjęć z filtrowaniem kategorii i lightboxem opartym na **[bs5-lightbox](https://trvswgnr.github.io/bs5-lightbox/)** (Bootstrap 5 Modal + Carousel).

**Funkcje:**
- Kolekcja zdjęć z tytułem, opisem, kategorią i osobnym pełnym rozmiarem do lightboxa
- Filtrowanie po kategoriach — przyciski generowane automatycznie z danych zdjęć
- Obsługa wielu kategorii na jedno zdjęcie (oddzielone przecinkiem)
- Siatka CSS Grid z niezależną liczbą kolumn na 5 breakpointach (xs/sm/md/lg/xl)
- Konfigurowalne proporcje miniatur: 1:1, 4:3, 16:9, 3:4, swobodne
- Dopasowanie obrazka: cover / contain
- Lightbox: nawigacja karuzelą, klawiatura, swipe, caption, opis, rozmiar (sm/lg/xl/fullscreen)
- Efekt lupy i powiększenia przy hover
- Pełna dostępność (aria-label, aria-pressed, keyboard)

**Instalacja (dodatkowy plik JS):**
```
templates/{nazwa_szablonu}/custom/particles/js/bs5-lightbox.bundle.min.js
```

**Wymagania:** Joomla 5+ / 6+, Gantry 5, szablon z Bootstrap 5 (np. Helium)

> Bootstrap 5.3 ładowany z `/media/vendor/bootstrap/` — bs5-lightbox używa go przez `window.bootstrap` (cząstka wystawia klasy globalnie automatycznie).

---

## Wymagania ogólne

- Joomla 5.x lub 6.x
- Gantry 5 Framework
- Szablon oparty na Gantry 5

---

## Licencja

MIT — używaj dowolnie w projektach komercyjnych i niekomercyjnych.
