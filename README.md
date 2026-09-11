# Truwer — Mudlet

Truwer to asystent odgrywania sekwencyjnego: śpiewanie piosenek, deklamowanie wierszy, odgrywanie scen lub rytuałów.

## Jak zainstalować

1. Pobierz `.mpackage` albo `.xml` z [najnowszego wydania](https://github.com/Isithunzi000/arkadia-mudlet-truwer/releases/latest) (oba działają tak samo, wybierz który wolisz)
2. W Mudlecie: **Toolbox → Package Manager** (`Alt+O`) → **Install** i wskaż pobrany plik
3. Gotowe — wpisz `/truwer`

## Użycie

- `/truwer` — otwiera okno asystenta
- Budujesz scenę z kroków: komendy, pauzy, notatki — plugin podaje kolejne linie do wysłania
- Każdą linię wysyłasz samodzielnie: kliknięciem **Wyślij** lub Enterem
- Opcjonalny tryb auto-przejścia po odliczeniu pauzy podpowiada kolejną linię, ale nigdy nie wysyła jej automatycznie

Plugin w pełni zgodny z regulaminem gry — wszystkie komendy wysyłane świadomie przez gracza, bez automatyki.

## Komendy

| Komenda | Opis |
|---------|------|
| `/truwer` | otwiera/zamyka okno truwera |
| `/truwer pomoc` | pomoc w konsoli (pełna pomoc: przycisk „Pomoc" w oknie) |
| `/truwer aktualizuj` | sprawdza i instaluje aktualizację z GitHub Releases |

## Aktualizacje

Pakiet przy starcie klienta (nie częściej niż co 8 godzin) sprawdza najnowsze wydanie na GitHubie i wyświetla powiadomienie o nowszej wersji — sam nic nie instaluje; aktualizację uruchamiasz świadomie komendą `/truwer aktualizuj`.

Sceny i ustawienia zapisują się w katalogu profilu Mudleta (`<profil>/truwer-dane/`).

Licencja [AGPL-3.0](LICENSE).
