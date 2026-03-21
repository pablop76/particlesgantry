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

---

## Wymagania ogólne

- Joomla 5.x lub 6.x
- Gantry 5 Framework
- Szablon oparty na Gantry 5

---

## Licencja

MIT — używaj dowolnie w projektach komercyjnych i niekomercyjnych.
