# Truwer — Mudlet

Pakiet do Mudleta: asystent scenek RP dla Arkadii MUD — śpiewanie, recytacja,
odgrywanie scen krok po kroku z prompterem. Biblioteka scen per postać,
edytor kroków i okno odgrywania z odliczaniem pauz.

Port pluginu truwer z klientów [Dargoth](https://github.com/Isithunzi000/arkadia-dargoth-plugins)
i WWW (rozszerzenie do przeglądarki).

---

## Jak zainstalować

1. Pobierz `.mpackage` albo `.xml` z [najnowszego wydania](https://github.com/Isithunzi000/arkadia-mudlet-truwer/releases/latest) (oba działają tak samo, wybierz który wolisz)
2. W Mudlecie: **Toolbox → Package Manager** (`Alt+O`) → **Install** i wskaż pobrany plik
3. Gotowe — wpisz `/truwer`

> Paczka powinna znajdować się powyżej skryptów ogólnodostępnych Arkadii — przesuń ją w górę listy w Package Manager.

Plik [`truwer.xml`](truwer.xml) w korzeniu repo to źródło pakietu — możesz podejrzeć cały kod bez pobierania.

---

## Komendy

| Komenda | Opis |
|---------|------|
| `/truwer` | otwiera/zamyka okno truwera |
| `/truwer pomoc` | pomoc w konsoli (pełna pomoc: przycisk „Pomoc" w oknie) |
| `/truwer aktualizuj` | sprawdza i instaluje aktualizację z GitHub Releases |

## Co potrafi

- **biblioteka scen per postać** — każda postać ma własną bibliotekę
  (plus biblioteka wspólna przed wykryciem postaci); sortowanie po dacie
  modyfikacji, powielanie, zaznaczanie i operacje zbiorcze, eksport/import
  JSON (format v1 zgodny z klientami przeglądarkowymi)
- **edytor scen** — kroki trzech typów: komenda, pauza (z liczbą sekund),
  nota; kolejność kroków strzałkami, duplikowanie, warianty komendy
  `a|b|c` (prompter wylosuje jedną); zapis jest natychmiastowy
- **prompter (odgrywanie)** — scena krok po kroku: bieżący krok w polu
  do edycji, wysyłka przyciskiem „Wyślij" albo Enterem, „Losuj ponownie"
  dla wariantów, pauza z widocznym odliczaniem; opcjonalnie po pauzie
  kursor sam przechodzi dalej (bez wysyłania)
- **ustawienia** — ręczne nadpisanie postaci dla biblioteki (puste pole
  = automatyczne wykrywanie z gry)

## Regulamin

Plugin **nigdy sam nie wysyła** komend do gry — każda wysyłka to świadoma
akcja gracza (kliknięcie „Wyślij" albo Enter w polu komendy). Odliczanie
pauzy i automatyczne przechodzenie dalej nie wysyłają niczego.

---

## Aktualizacje

Pakiet sam sprawdza aktualizacje: przy starcie klienta (nie częściej niż
co 8 godzin) pyta o najnowsze wydanie na GitHubie i — jeśli jest nowsza
wersja — wyświetla powiadomienie. Sam nic nie instaluje: aktualizację
uruchamiasz świadomie komendą `/truwer aktualizuj` albo przyciskiem
w ustawieniach — pakiet pobiera wydanie, podmienia je i prosi o restart
Mudleta.

Assety wydania mają stałe nazwy (`truwer.mpackage`, `truwer.xml`),
a aktualizator przed instalacją sprząta historyczne nazwy pakietów —
jedna paczka zostaje w profilu zawsze pod nazwą `truwer`.

---

## Dane

Sceny, ustawienia i pozycja okna zapisują się na dysku profilu Mudleta
(`<profil>/truwer/`) i przeżywają restart klienta. W mudlet-web (Mudlet
w przeglądarce) zapis działa przez IndexedDB — per origin i profil,
best-effort (np. czyszczenie danych przeglądarki kasuje bibliotekę).

## Licencja

GPL-3.0 — patrz [LICENSE](LICENSE).
