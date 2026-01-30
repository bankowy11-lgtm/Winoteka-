# 🍷 Vino Scanner - Skaner Win Włoskich

Elegancka aplikacja webowa do skanowania kodów kreskowych na butelkach włoskich win z możliwością instalacji na telefonie Android jako PWA (Progressive Web App).

## ✨ Funkcje

- 📸 **Skanowanie kamerą** - używa QuaggaJS do skanowania kodów kreskowych
- ⌨️ **Ręczne wprowadzanie** - możliwość wpisania kodu ręcznie
- 📱 **Instalacja na telefonie** - działa jako aplikacja mobilna (PWA)
- 🎨 **Elegancki design** - inspirowany włoską kulturą winiarską
- 🍇 **Informacje o winie** - typ (słodkie/półsłodkie/wytrawne/półwytrawne), region, szczepy
- 🌐 **Działa offline** - po instalacji nie wymaga połączenia z internetem

## 🚀 Instalacja na GitHub Pages

1. **Stwórz repozytorium na GitHub:**
   - Zaloguj się na GitHub
   - Kliknij "New repository"
   - Nazwij repozytorium np. "vino-scanner"
   - Ustaw jako publiczne

2. **Wgraj pliki:**
   - Kliknij "uploading an existing file"
   - Przeciągnij wszystkie pliki: `index.html`, `manifest.json`, `sw.js`, `README.md`
   - Kliknij "Commit changes"

3. **Włącz GitHub Pages:**
   - Idź do Settings → Pages
   - W "Source" wybierz "Deploy from a branch"
   - Wybierz branch "main" i folder "/ (root)"
   - Kliknij Save

4. **Otwórz aplikację:**
   - Poczekaj 1-2 minuty
   - Twoja aplikacja będzie dostępna pod adresem: `https://TWOJA-NAZWA.github.io/vino-scanner/`

## 📱 Instalacja na Androidzie

### ⚠️ PRZED INSTALACJĄ - Test kamery!
Wgraj również plik `camera-test.html` i otwórz go aby sprawdzić czy kamera działa.
Adres będzie: `https://TWOJA-NAZWA.github.io/vino-scanner/camera-test.html`

### Metoda 1: Chrome (zalecana)
1. Otwórz aplikację w Chrome na telefonie
2. Kliknij menu (trzy kropki) → "Dodaj do ekranu głównego"
3. Potwierdź instalację
4. Ikona aplikacji pojawi się na ekranie głównym

### Metoda 2: Banner instalacyjny
1. Otwórz aplikację w przeglądarce
2. Po chwili pojawi się banner "Zainstaluj aplikację"
3. Kliknij "Instaluj"

## 🍇 Przykładowe kody kreskowe

Aplikacja zawiera bazę danych przykładowych włoskich win:

- `8001935001706` - Chianti Classico DOCG (Wytrawne)
- `8002915001234` - Moscato d'Asti DOCG (Słodkie)
- `8003120001111` - Lambrusco (Półsłodkie)
- `8004567001234` - Soave DOC (Półwytrawne)
- `8005678901234` - Amarone della Valpolicella (Wytrawne)
- `8006789012345` - Barbera d'Alba (Wytrawne)
- `8007890123456` - Recioto della Valpolicella (Słodkie)

## 🔧 Dostosowanie

### Dodawanie własnych win

Edytuj plik `index.html` i znajdź sekcję `wineDatabase`. Dodaj nowe wino według wzoru:

```javascript
const wineDatabase = {
    'TU_KOD_KRESKOWY': {
        name: 'Nazwa Wina',
        region: 'Region',
        type: 'Wytrawne', // lub Słodkie, Półsłodkie, Półwytrawne
        grapes: 'Szczepy winogron',
        color: '#HEX_KOLOR'
    },
    // ... reszta win
};
```

### Zmiana kolorów

Edytuj style CSS w sekcji `<style>` w pliku `index.html`. Główne kolory:
- Tło: `#1a0e0e`, `#3d1616`
- Akcenty: `#fbbf24` (złoty), `#7f1d1d` (bordowy)

## 🛠️ Technologie

- **HTML5** - struktura aplikacji
- **CSS3** - stylizacja z animacjami
- **JavaScript** - logika aplikacji
- **QuaggaJS** - biblioteka do skanowania kodów kreskowych
- **PWA** - Progressive Web App dla instalacji mobilnej

## 📄 Struktura plików

```
vino-scanner/
├── index.html         # Główny plik aplikacji
├── manifest.json      # Manifest PWA dla instalacji
├── sw.js             # Service Worker dla trybu offline
├── camera-test.html  # Test dostępu do kamery (opcjonalny)
└── README.md         # Ten plik
```

## 🌟 Funkcje PWA

- ✅ Działa offline
- ✅ Instalowalna na urządzenia mobilne
- ✅ Szybkie ładowanie
- ✅ Własna ikona na ekranie głównym
- ✅ Pełny ekran (bez paska przeglądarki)

## 🐛 Rozwiązywanie problemów

### ⚠️ BŁĄD: "Permission denied" (Brak dostępu do kamery)

To najczęstszy problem! Oto rozwiązania:

#### 1. Sprawdź uprawnienia w Chrome (Android):
- Kliknij ikonę kłódki/informacji obok adresu URL
- Znajdź "Uprawnienia" lub "Permissions"
- Upewnij się, że "Kamera" jest ustawiona na "Zezwalaj"
- Odśwież stronę (F5)

#### 2. Uprawnienia w ustawieniach systemu Android:
- Ustawienia → Aplikacje → Chrome
- Uprawnienia → Kamera
- Upewnij się, że jest włączona

#### 3. Sprawdź czy strona używa HTTPS:
- Kamera działa TYLKO przez HTTPS!
- Adres musi zaczynać się od `https://`
- GitHub Pages automatycznie używa HTTPS ✅
- Otwieranie lokalnie (`file://`) NIE DZIAŁA ❌

#### 4. Zamknij inne aplikacje używające kamery:
- Facebook, Instagram, Messenger
- Inne karty w przeglądarce z kamerą
- Aplikacje do wideokonferencji

#### 5. Restart:
- Zamknij całkowicie Chrome (z menu "Zamknij Chrome")
- Otwórz ponownie
- Spróbuj jeszcze raz

### Skaner nie reaguje na kod
1. **Sprawdź oświetlenie** - kody kreskowe wymagają dobrego światła
2. **Trzymaj stabilnie** - unikaj ruchów podczas skanowania
3. **Dystans** - spróbuj przybliżyć lub oddalić telefon (15-30 cm)
4. **Kąt** - trzymaj kod prostopadle do kamery
5. **Użyj przycisku "Test"** - sprawdź czy aplikacja działa
6. **Ręczne wprowadzanie** - zawsze możesz wpisać kod ręcznie

### Skaner nie uruchamia się
- Upewnij się, że przeglądarka ma dostęp do kamery
- Sprawdź czy strona jest otwarta przez HTTPS (GitHub Pages automatycznie używa HTTPS)
- Spróbuj ręcznego wprowadzania kodu

### Aplikacja nie instaluje się
- Upewnij się, że używasz Chrome lub innej przeglądarki obsługującej PWA
- Sprawdź czy strona jest otwarta przez HTTPS
- Wyczyść cache przeglądarki

### Najlepsze praktyki skanowania
- ✅ Dobre, równomierne światło (ale nie bezpośrednie odblaski)
- ✅ Stabilne trzymanie telefonu
- ✅ Kod kreskowy prostopadle do kamery
- ✅ Dystans 15-30 cm od kodu
- ✅ Czysty, wyraźny kod bez uszkodzeń

## 📝 Licencja

Projekt open-source - możesz swobodnie używać i modyfikować.

## 🤝 Kontakt

Masz pytania lub sugestie? Stwórz Issue na GitHubie!

---

**Buon appetito e salute! 🍷**
