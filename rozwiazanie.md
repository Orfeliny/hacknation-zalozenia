# Propozycja rozwiązania

Kod: [Orfeliny/Hacknation-2026](https://github.com/Orfeliny/Hacknation-2026). Zadania i kolejność
prac są w issues tego repo (#9 kontrakt, #10-#32 moduły). Założenia, na których stoi ten opis:
[zalozenia.md](zalozenia.md).

## Propozycja wartości

**Dla kogo:** przełożeni oceniający pracowników służby cywilnej; dodatkowo oceniani, komórki
kadrowe i kierownictwo urzędu.

**Jaki problem rozwiązujemy:** ocena okresowa jest papierowa, formalna i robiona w pośpiechu
przed terminem. Przełożony nie ma obserwacji z całego okresu, nie wie, jak przełożyć zachowania
na poziom kompetencji, i sam musi napisać uzasadnienia oraz plan rozwoju. Kadry ręcznie pilnują
terminów i poprawiają błędy po fakcie.

**Jak to robimy inaczej:**

- Prowadzimy przez cały proces krok po kroku, a przepisy trzymamy jako wersjonowane dane.
  Nowelizacja ustawy to zmiana danych, nie przebudowa aplikacji.
- Zbieramy obserwacje przez cały okres oceny, a potem AI układa z nich projekt uzasadnień.
  Każde zdanie wskazuje obserwację, na której się opiera.
- AI nigdy nie wybiera oceny. Sugerowany poziom kompetencji liczymy jawnym algorytmem
  z zachowań zaznaczonych przez przełożonego, a decyzja i tak należy do niego.
- Asystent wiedzy odpowiada tylko na podstawie przepisów i poradników, pokazuje źródło
  i mówi „nie wiem”, gdy w bazie nie ma odpowiedzi.
- Całość uruchamia się w sieci urzędu (Docker, opcjonalnie lokalny polski model Bielik / PLLuM),
  bez płatnych licencji i bez wysyłania danych pracowników na zewnątrz.

**Jakiej wartości dostarcza rozwiązanie:**

- przełożony: mniej czasu nad arkuszem, lepiej przygotowana rozmowa, ocena oparta na faktach
  z całego okresu;
- oceniany: zna oczekiwania od początku okresu i widzi swój plan rozwoju;
- kadry: terminy i braki formalne widoczne od razu, bez arkusza kalkulacyjnego;
- kierownictwo: zagregowany obraz ocen i potrzeb rozwojowych urzędu;
- KPRM i MC: narzędzie, które każdy urząd może postawić u siebie i aktualizować wraz z przepisami.

## Kluczowy flow

### Ścieżka główna: ocena okresowa (Asystent, KPRM)

1. Przełożony otwiera „Mój zespół” i rozpoczyna ocenę pracownika. Aplikacja podpowiada arkusz
   A/B/C i pokazuje kryteria obowiązkowe.
2. Przełożony wybiera do 3 kryteriów dodatkowych. Przy każdym widzi opis i przykład oczekiwań.
3. Przygotowanie do rozmowy rozpoczynającej: AI proponuje cel, plan i pytania do każdego
   kryterium. Przełożony je poprawia, a po rozmowie zapisuje ustalenia (widzi je też oceniany).
4. Przez okres oceny (zwykle 24 miesiące) przełożony dopisuje krótkie obserwacje przypięte do
   kryteriów. Aplikacja pokazuje kryteria bez żadnej obserwacji.
5. HR partner w tle podnosi sygnały: przeciążenie, długi brak docenienia, zmiana zadań. Do
   każdego proponuje działania i scenariusz rozmowy wspierającej.
6. Kadry widzą status wszystkich ocen i terminy, aplikacja sama wysyła przypomnienia.
7. Przed rozmową oceniającą przełożony przechodzi w tryb rozmowy: skrypt i pytania na pierwszym
   planie, wykresy schowane.
8. Przełożony wybiera ocenę każdego kryterium. AI układa projekt uzasadnień, mocnych stron,
   obszarów do rozwoju i działań rozwojowych (wnioski do IPRZ) z odnośnikami do obserwacji
   i ostrzega o niespójnościach.
9. Walidacja formalna sprawdza braki, potem obie strony podpisują ocenę. Wydruk lub PDF wygląda
   jak urzędowy arkusz.

### Ścieżka rozszerzenia: Kompas kompetencji (MC)

1. Przełożony wybiera ścieżkę: pierwsza ocena albo ocena okresowa.
2. Przy każdej kompetencji zaznacza przy wskaźnikach behawioralnych zachowania najbliższe temu,
   co obserwował.
3. Aplikacja pokazuje sugerowany poziom i sposób jego wyliczenia. Przełożony wybiera poziom
   końcowy; jeśli różni się od sugestii, dopisuje krótkie uzasadnienie.
4. W dowolnym momencie przełożony pyta asystenta o zasady („ile mam czasu na rozmowę
   oceniającą?”) i dostaje odpowiedź z klikalnym źródłem albo „nie znalazłem tego w bazie”.

## Zakres MVP

### W MVP

- [ ] Kontrakt danych i demo-role: przełożony, oceniany, kadry, dyrektor (#9)
- [ ] Reguły prawne jako dane: arkusze, kryteria, skala, terminy, sytuacje kadrowe (#10)
- [ ] Zespół i fikcyjne dane demo (#11)
- [ ] Kreator oceny okresowej od startu do podpisu (#12)
- [ ] Dziennik obserwacji (#13)
- [ ] AI: przygotowanie do rozmów + tryb rozmowy (#14)
- [ ] AI: projekt uzasadnień i wniosków rozwojowych ze źródłami (#15)
- [ ] Wirtualny HR partner: sygnały i rekomendacje (#16)
- [ ] Panel kadr: statusy, terminy, przypomnienia, statystyki (#17)
- [ ] Wydruk / PDF arkusza (#18)
- [ ] Kompas: wskaźniki behawioralne i sugerowany poziom (#19)
- [ ] Kompas: asystent wiedzy z cytatami (#20)
- [ ] Guardrails AI i pseudonimizacja (#28)
- [ ] Przełącznik profilu wyzwania Asystent / Kompas (#29)
- [ ] Uruchomienie on-prem w Docker Compose + instrukcja (#23, #24, #25)
- [ ] Materiały zgłoszeniowe i dwa wideo-demo (#22, #32)

### Poza MVP (opisane jako kierunek rozwoju)

- Prawdziwe logowanie (SSO / Active Directory) – w MVP demo-role; wraca do zakresu, jeśli MC
  tego wymaga (H19).
- Podpis kwalifikowany / profil zaufany i obieg w EZD – w MVP potwierdzenie w aplikacji (H9).
- Działające integracje z EZD i QNT – w MVP eksport JSON i opis interfejsu (H20).
- Wysyłka e-mail – w MVP przypomnienia w aplikacji i atrapa kanału.
- Wersja mobilna – świadomie pominięta (wymóg MC, H23).
- Ścieżka pierwszej oceny (#21), widok pracownika (#30), odznaka modelu AI (#27), lokalny Bielik
  (#26) – „mile widziane”, jeśli starczy czasu.
- Układ ekranu sterowany przez AI (Maelstrom, spike #31) – tylko po decyzji GO.

## Kryteria sukcesu MVP

- Na demo przechodzimy jedną ocenę okresową od startu do podpisanego wydruku w mniej niż 5 minut,
  na danych fikcyjnych i bez internetu (tryb `mock`).
- Każdy krok ze schematu procesu KPRM ma odpowiednik w aplikacji (H5).
- Jury MC przechodzi ścieżkę: kompetencja → wskaźniki → sugerowany poziom → decyzja
  przełożonego, a odchylenie od sugestii wymaga uzasadnienia.
- Asystent wiedzy odpowiada poprawnie na co najmniej 80% pytań testowych z poprawnym źródłem
  i mówi „nie wiem” przy pytaniach spoza bazy (H14).
- Żadna funkcja AI nie proponuje poziomu oceny (H11), a dane identyfikujące pracownika nie trafiają
  do promptu (H16).
- Osoba spoza zespołu stawia aplikację według instrukcji on-prem na czystej maszynie.
- Spełniamy wszystkie wymagania formalne obu zgłoszeń: prezentacje 15 i 10 slajdów, opis,
  opis użycia AI, architektura, linki dostępne bez logowania.
