# particlesgantry

Zbiór cząstek (particles) dla szablonów **Gantry 5** na **Joomla 5+ / 6+**.
Każda cząstka to gotowy do użycia komponent — kopiujesz dwa pliki do swojego szablonu i konfigurujesz przez panel admina Gantry bez dotykania kodu.

---

## Zawartość

| Plik | Opis |
|------|------|
| `particles/menu_bootstrap.yaml` | Definicja pól konfiguracyjnych (panel admina Gantry) |
| `particles/menu_bootstrap.html.twig` | Szablon HTML cząstki |

---

## Cząstka: Menu Bootstrap

Pełnoprawna nawigacja Joomla oparta na **Bootstrap 5.3** z offcanvas na urządzeniach mobilnych.
Zastępuje domyślną cząstkę Menu w Gantry 5 — działa na Joomla 5 i 6, nie wymaga instalacji dodatkowych rozszerzeń.

### Funkcje

- Nawigacja desktopowa z dropdownami wielopoziomowymi
- Offcanvas na mobile (hamburger → panel boczny)
- Responsywne podwójne logo (inne na desktop, inne na mobile)
- Tryby sticky: brak / sticky / scroll-up (chowa się przy scrollu w dół) / fixed
- Zmniejszanie logo przy scrollu
- Ikony social media w navbarze i offcanvas
- Własny hamburger (ikona FA lub własny obrazek)
- Pełna kontrola typografii: font (Google Fonts), rozmiar, grubość, transformacja tekstu, letter-spacing, odstępy
- Kolory dziedziczone z Gantry Styles (nawigacja, offcanvas) — nadpisywalne per instancja
- Zgodność z WCAG / standardami dostępności 2026

### Wymagania

- Joomla 5.x lub 6.x
- Gantry 5 Framework
- Szablon oparty na Gantry 5 (np. Helium, Hydrogen)

> Bootstrap 5.3 CSS i JS są wbudowane w Joomla 5+ — cząstka ładuje je z `/media/vendor/bootstrap/`.
> Nie trzeba instalować Bootstrap osobno.

---

## Instalacja

1. Skopiuj oba pliki do katalogu cząstek swojego szablonu:

```
templates/{nazwa_szablonu}/custom/particles/menu_bootstrap.yaml
templates/{nazwa_szablonu}/custom/particles/menu_bootstrap.html.twig
```

2. Wyczyść cache Gantry: **Gantry 5 → Clear Cache**

3. W Layout Managerze przeciągnij cząstkę **Menu Bootstrap** w wybrane miejsce layoutu

4. Skonfiguruj przez panel admina cząstki

---

## Konfiguracja

### Zakładka Logo

| Pole | Opis |
|------|------|
| URL Logo | Link logo (domyślnie strona główna) |
| Tekst Logo | Tekst gdy brak obrazka |
| Obrazek Logo | Logo dla desktopa |
| Maksymalna wysokość | Np. `50px`, `3rem` |
| Zmniejsz logo przy skrolu | Animuje logo do mniejszego rozmiaru po przewinięciu |
| Wysokość po zmniejszeniu | Docelowa wysokość po scrollu |
| Obrazek Logo (mobile) | Alternatywne logo widoczne w navbarze na mobile i w offcanvas |
| Maksymalna wysokość (mobile) | Wysokość logo mobilnego |

### Zakładka Menu

| Pole | Opis |
|------|------|
| Menu | Wybór menu Joomla |
| Element bazowy | Od którego elementu renderować |
| Poziom startowy / Maks. poziomów | Głębokość menu |
| Rozwiń menu od | Breakpoint Bootstrap: `sm` / `md` / `lg` / `xl` / `xxl` |
| Tekst przycisku | Tekst obok hamburgera |
| Ikona hamburgera | Ikona Font Awesome zamiast domyślnej |
| Obrazek hamburgera | Własny obrazek zamiast ikony |

### Zakładka Offcanvas

| Pole | Opis |
|------|------|
| Strona offcanvas | Lewa (start) lub prawa (end) |
| Pokaż logo w offcanvas | Logo w nagłówku panelu |
| Ikona zamknięcia | Niestandardowa ikona przycisku zamknięcia |
| Kolor tła offcanvas | Nadpisuje domyślne z Gantry Styles → Offcanvas Styles |
| Schemat kolorów | Jasny / ciemny (Bootstrap `data-bs-theme`) |

### Zakładka Social Media

Dodaj linki social media jako lista. Każda pozycja: ikona FA, URL, etykieta (aria-label), otwórz w nowej karcie.
Ikony można pokazać w navbarze (desktop) i/lub offcanvas (mobile).

### Zakładka Styl

**Przyklejanie:**

| Tryb | Zachowanie |
|------|-----------|
| Brak | Nawigacja w normalnym przepływie |
| Sticky | Przyklejona gdy dotrze do górnej krawędzi ekranu |
| Ukryj przy skrolu w dół | Zawsze na górze, chowa się przy scrollu w dół, pokazuje przy scrollu w górę |
| Fixed | Zawsze na górze (wymaga ręcznego `padding-top` na `body`) |

**Nawigacja desktop:** szerokość kontenera, wyrównanie linków, cień przy sticky, tło przy scrollu, kolory linków, tło dropdown.

**Typografia:** czcionka (Google Fonts picker), rozmiar, grubość, transformacja tekstu, letter-spacing, odstęp między pozycjami, padding linków, rozmiar i padding pozycji dropdown, tło hover dropdown.

---

## Jak działa sticky na Gantry 5 / Helium

CSS `position: sticky` nie działa w Helium ponieważ `#g-page-surround` ma `overflow: hidden`.
Cząstka używa JavaScriptu (scroll listener) jako obejścia — bez żadnych zależności zewnętrznych.

---

## Licencja

MIT — używaj dowolnie w projektach komercyjnych i niekomercyjnych.

---

*Autor: [pablop76](https://web-service.com.pl/)*
