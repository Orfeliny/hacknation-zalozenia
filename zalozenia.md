# Założenia hackathonowe

Temat główny: **Cyfrowy Asystent Ocen Okresowych** (KPRM). Rozszerzenie: **Kompas kompetencji**
(Ministerstwo Cyfryzacji). Opisy wyzwań:
[Hacknation-2026/docs/wyzwanie](https://github.com/Orfeliny/Hacknation-2026/tree/main/docs/wyzwanie).

Każda hipoteza poniżej to coś, w co dziś wierzymy, ale czego nie sprawdziliśmy. Przy każdej jest
metoda walidacji i próg, po którym uznajemy ją za potwierdzoną. Pytania do mentorów, które je
sprawdzają, są w [pytania-do-mentorow.md](pytania-do-mentorow.md) (numery H w nawiasach).

Status: ⬜ niesprawdzona · ✅ potwierdzona · ❌ obalona · 🔄 zmieniona po rozmowie.

## Problem

**Opis problemu:** Ocena okresowa w służbie cywilnej żyje głównie na papierze, czasem pisana
odręcznie. Przełożeni traktują ją jak obowiązek administracyjny: pilnują terminów i pól
formularza, a nie jakości informacji zwrotnej ani rozwoju pracownika. Najtrudniej idzie im wybór
kryteriów dodatkowych, opisanie oczekiwań, rozmowa oceniająca, obiektywna ocena i plan rozwoju.
Dobrostan i sygnały wypalenia praktycznie nie wchodzą do procesu. Kompetencje („komunikacja”,
„współpraca”) różni przełożeni rozumieją różnie, więc ten sam pracownik u dwóch szefów mógłby
dostać inną ocenę.

**Kogo dotyczy:** ok. 123 tys. członków korpusu służby cywilnej w ok. 1743 urzędach: przełożonych
(oceniających), ocenianych, komórek kadrowych i kierownictwa urzędów.

**Obserwacje / dowody:**

- Opis KPRM: ocena „najczęściej sporządzana jest w formie papierowej”, a problemem jest obieg
  dokumentacji cyfrowej i poświadczeń.
- Opis KPRM: pięć konkretnych trudności oceniających (kryteria, wymagania, informacja zwrotna,
  obiektywność, plan rozwoju).
- Opis MC: brak jednego narzędzia, które łączy przepisy, model kompetencyjny, formularze
  i przygotowanie do rozmowy.
- Brakuje nam danych z pierwszej ręki: ilu przełożonych pisze ocenę w ostatnim tygodniu przed
  terminem, ile ocen ma błędy formalne, jak wygląda obieg w średnim urzędzie. To mają
  zweryfikować rozmowy z mentorami.

## Użytkownik docelowy

### Przełożony (oceniający) – główny użytkownik

- **Segment:** kierownik komórki, naczelnik, dyrektor departamentu; od 2 do kilkunastu osób
  w zespole; często bez przygotowania HR.
- **Kontekst użycia:** kilka razy w roku na krótko (notatka, rozmowa), raz na okres oceny
  intensywnie (sporządzenie oceny); przy biurku, na komputerze służbowym.
- **Najważniejsza potrzeba:** sporządzić ocenę poprawnie formalnie i bez stresu, a przy okazji
  mieć z czym iść na rozmowę.
- **Obecna alternatywa:** wzór arkusza w Wordzie lub na papierze, zeszłoroczna ocena jako
  ściąga, telefon do kadr, poradniki KPRM w PDF.

### Oceniany

- **Segment:** urzędnik i pracownik służby cywilnej.
- **Kontekst użycia:** rozmowa rozpoczynająca, rozmowa oceniająca, podpis, wgląd w plan rozwoju.
- **Najważniejsza potrzeba:** wiedzieć z góry, czego się od niego oczekuje, i dostać uzasadnioną
  ocenę.
- **Obecna alternatywa:** kopia papierowego arkusza.

### Komórka kadrowa

- **Segment:** specjaliści ds. kadr i HR w urzędzie.
- **Kontekst użycia:** pilnowanie terminów wszystkich ocen, przypomnienia, archiwizacja,
  wnioski o stopnie służbowe, statystyki dla kierownictwa.
- **Najważniejsza potrzeba:** wiedzieć bez ręcznego liczenia, które oceny są zagrożone, i nie
  poprawiać błędów formalnych po fakcie.
- **Obecna alternatywa:** arkusz kalkulacyjny z terminami, system kadrowy (np. QNT), e-maile.

### Kierownictwo urzędu (dyrektor generalny)

- **Kontekst użycia:** kilka razy w roku przegląd statystyk.
- **Najważniejsza potrzeba:** obraz rozkładu ocen i potrzeb rozwojowych w urzędzie bez
  zaglądania w oceny pojedynczych osób.

## Hipotezy

### A. Problem i użytkownicy

#### H1 – Najbardziej boli pisanie uzasadnień, nie wypełnianie pól ⬜

- **Założenie:** Przełożeni najwięcej czasu i nerwów tracą na opisaniu ocen i wniosków
  rozwojowych, a nie na formalnościach (wybór arkusza, daty, podpisy).
- **Dowód potrzebny do potwierdzenia:** mentorzy z DSC wskazują uzasadnienia albo plan rozwoju
  jako najczęstszy problem w praktyce.
- **Metoda walidacji:** pytanie otwarte do mentorów merytorycznych, bez podsuwania odpowiedzi.
- **Kryterium sukcesu:** co najmniej 2 z 3 zapytanych mentorów wymienia to wśród dwóch głównych
  problemów.

#### H2 – Przełożeni nie notują obserwacji w trakcie okresu oceny ⬜

- **Założenie:** Ocena powstaje z pamięci ostatnich tygodni, bo przez 24 miesiące nikt nie
  zapisuje obserwacji.
- **Dowód potrzebny do potwierdzenia:** mentorzy potwierdzają, że notatki z okresu oceny to
  rzadkość.
- **Metoda walidacji:** pytanie do mentorów i, jeśli się uda, do przełożonego z sali.
- **Kryterium sukcesu:** nikt nie zna urzędu, w którym notowanie jest standardem.

#### H3 – Kadry tracą najwięcej czasu na terminy i poprawki formalne ⬜

- **Założenie:** Kadry ręcznie pilnują terminów i odsyłają arkusze z błędami.
- **Dowód potrzebny do potwierdzenia:** przykłady typowych błędów formalnych i opis, jak kadry
  dziś pilnują terminów.
- **Metoda walidacji:** pytanie do mentorów o najczęstsze błędy w arkuszach.
- **Kryterium sukcesu:** mentorzy podają co najmniej 3 powtarzalne błędy, które da się wykryć
  automatycznie.

#### H4 – Oceniany chce widzieć oczekiwania i plan rozwoju, nie tylko wynik ⬜

- **Założenie:** Widok pracownika ma sens, bo oceniany dostaje dziś tylko kopię arkusza.
- **Dowód potrzebny do potwierdzenia:** mentorzy potwierdzają, że ustalenia z rozmowy
  rozpoczynającej giną po drodze.
- **Metoda walidacji:** pytanie do mentorów.
- **Kryterium sukcesu:** brak sprzeciwu i co najmniej jeden przykład sporu typu „nie wiedziałem,
  że tego się ode mnie oczekuje”.

### B. Przepisy i proces

#### H5 – Proces da się odwzorować jako stałą sekwencję etapów ⬜

- **Założenie:** Każda ocena przechodzi te same etapy: arkusz → kryteria → rozmowa
  rozpoczynająca → obserwacja → rozmowa oceniająca → ocena na piśmie → podpisy.
- **Dowód potrzebny do potwierdzenia:** schemat procesu od KPRM zgadza się z naszym kreatorem.
- **Metoda walidacji:** porównanie z udostępnionym schematem procesu i przypadkami użycia.
- **Kryterium sukcesu:** każdy krok ze schematu ma odpowiednik w aplikacji albo świadomą decyzję,
  że go pomijamy.

#### H6 – Arkusz A/B/C wynika wprost z rodzaju stanowiska ⬜

- **Założenie:** Arkusz da się wybrać automatycznie z danych stanowiska, bez decyzji przełożonego.
- **Dowód potrzebny do potwierdzenia:** reguła z rozporządzenia bez wyjątków albo lista wyjątków.
- **Metoda walidacji:** lektura rozporządzenia + pytanie do mentora DSC.
- **Kryterium sukcesu:** reguła mieści się w tabeli bez pola „inne”.

#### H7 – Sytuacje kadrowe da się opisać skończoną listą reguł ⬜

- **Założenie:** Zmiana oceniającego, zmiana zadań i długotrwała nieobecność mają w przepisach
  jasno określone skutki.
- **Dowód potrzebny do potwierdzenia:** lista sytuacji i skutków od mentorów.
- **Metoda walidacji:** pytanie do mentorów + przepisy.
- **Kryterium sukcesu:** każda sytuacja ma regułę, którą da się zapisać jako dane.

#### H8 – Nowelizacja zmieni terminy i elementy oceny, a nie całą logikę ⬜

- **Założenie:** Reguły trzymane jako wersjonowane dane wystarczą, żeby przeżyć procedowaną
  zmianę ustawy.
- **Dowód potrzebny do potwierdzenia:** mentorzy zdradzają kierunek zmian (częstotliwość ocen,
  terminy, elementy).
- **Metoda walidacji:** pytanie do mentorów DSC.
- **Kryterium sukcesu:** zapowiadane zmiany da się wyrazić jako zmianę danych reguł.

#### H9 – Prototyp nie potrzebuje podpisu elektronicznego ⬜

- **Założenie:** Jury przyjmie podpis jako potwierdzenie w aplikacji z datą i rolą, a docelowy
  podpis (kwalifikowany, profil zaufany, EZD) opiszemy jako integrację.
- **Dowód potrzebny do potwierdzenia:** odpowiedź mentora technicznego.
- **Metoda walidacji:** pytanie wprost.
- **Kryterium sukcesu:** mentor nie traktuje podpisu jako warunku kompletności.

### C. AI i HR partner

#### H10 – Przełożeni zaufają AI, jeśli każda podpowiedź pokazuje źródło ⬜

- **Założenie:** Projekt uzasadnienia z odnośnikami do obserwacji przełożonego zostanie przyjęty,
  a tekst „z niczego” odrzucony.
- **Dowód potrzebny do potwierdzenia:** reakcja mentora na dwie wersje w demo.
- **Metoda walidacji:** pokazanie obu wariantów na stoisku.
- **Kryterium sukcesu:** mentor sam wybiera wariant ze źródłami albo uznaje go za akceptowalny.

#### H11 – AI nie może proponować poziomu oceny ⬜

- **Założenie:** Każdą sugestię poziomu oceny od AI kapituły uznają za przejęcie decyzji
  przełożonego. Sugerowany poziom kompetencji (Kompas) liczymy więc deterministycznie
  z zaznaczonych zachowań, bez modelu.
- **Dowód potrzebny do potwierdzenia:** obie kapituły potwierdzają, że algorytm z jawnym
  wyliczeniem jest dopuszczalny, a sugestia modelu nie.
- **Metoda walidacji:** pytanie do mentorów MC i KPRM.
- **Kryterium sukcesu:** zgoda na podejście „algorytm tak, model nie”.

#### H12 – Sygnały przeciążenia wyliczymy z danych, które i tak zbieramy ⬜

- **Założenie:** Obserwacje z tagiem obciążenia, zmiany zakresu zadań, nieobecności i brak
  docenienia wystarczą do sensownych sygnałów HR partnera, bez ankiet dobrostanu.
- **Dowód potrzebny do potwierdzenia:** mentorzy uznają te sygnały za trafne i nie widzą w nich
  problemu prawnego.
- **Metoda walidacji:** pokazanie listy sygnałów z uzasadnieniem.
- **Kryterium sukcesu:** co najmniej 3 z 4 sygnałów uznane za przydatne.

#### H13 – Sygnały dobrostanu nie naruszają ochrony danych ⬜

- **Założenie:** Sygnał „ryzyko przeciążenia” widoczny tylko dla przełożonego, bez diagnozy
  i bez danych o zdrowiu, mieści się w przepisach.
- **Dowód potrzebny do potwierdzenia:** opinia mentora albo wskazanie, czego unikać.
- **Metoda walidacji:** pytanie o granice (np. czy wolno łączyć nieobecności z sygnałem).
- **Kryterium sukcesu:** jasna lista „wolno / nie wolno”.

#### H14 – Asystent wiedzy z cytatami przejdzie pytania jury ⬜

- **Założenie:** Wyszukiwanie pełnotekstowe po pociętych przepisach i poradnikach + model, który
  odpowiada tylko z cytowanych fragmentów, wystarczy do poprawnych odpowiedzi o pierwszą
  i okresową ocenę.
- **Dowód potrzebny do potwierdzenia:** wynik na zestawie pytań testowych, najlepiej od mentorów.
- **Metoda walidacji:** poprosić mentorów MC o 5-10 przykładowych pytań i zmierzyć trafność.
- **Kryterium sukcesu:** co najmniej 80% poprawnych odpowiedzi z poprawnym źródłem i „nie wiem”
  przy każdym pytaniu spoza bazy.

#### H15 – Otwarty polski model (Bielik / PLLuM) wystarczy jakościowo ⬜

- **Założenie:** Lokalny Bielik odpowiada po polsku wystarczająco dobrze na demo, a to załatwia
  wymóg darmowego AI (MC) i danych w sieci urzędu (KPRM).
- **Dowód potrzebny do potwierdzenia:** porównanie odpowiedzi Bielika i modelu chmurowego na tych
  samych pytaniach.
- **Metoda walidacji:** test na 10 pytaniach z H14 i 3 projektach uzasadnień.
- **Kryterium sukcesu:** różnica jakości akceptowalna dla zespołu i mentora; odpowiedź w mniej niż
  15 s na sprzęcie, który mamy.

#### H16 – Pseudonimizacja przed wysłaniem do modelu wystarczy KPRM ⬜

- **Założenie:** Zamiana imion i nazwisk na `[PRACOWNIK]` spełnia wymóg anonimizacji przy
  przetwarzaniu poza infrastrukturą urzędu.
- **Dowód potrzebny do potwierdzenia:** opinia mentora technicznego KPRM.
- **Metoda walidacji:** pytanie wprost, z przykładem promptu.
- **Kryterium sukcesu:** brak dodatkowych wymagań albo lista wymagań, które zmieścimy w czasie.

### D. Wdrożenie

#### H17 – Docker Compose to akceptowalna „łatwa instalacja” ⬜

- **Założenie:** Informatyk z urzędu uruchomi aplikację poleceniem `docker compose up`
  i instrukcją.
- **Dowód potrzebny do potwierdzenia:** mentor techniczny potwierdza, że urzędy mają Dockera, albo
  wskazuje alternatywę (maszyna wirtualna, Windows Server bez kontenerów).
- **Metoda walidacji:** pytanie o typowe środowisko IT małego urzędu.
- **Kryterium sukcesu:** Docker dostępny albo możliwy do zainstalowania w większości urzędów.

#### H18 – Self-hosted Convex nie przekreśla nas w oczach KPRM ⬜

- **Założenie:** Backend Convex uruchamiany we własnym kontenerze spełnia wymóg „bez płatnych
  licencji”. Do sprawdzenia: dokładna licencja `convex-backend` i jej warunki.
- **Dowód potrzebny do potwierdzenia:** brak zastrzeżeń mentora technicznego do licencji i stosu.
- **Metoda walidacji:** pytanie z krótkim opisem stosu.
- **Kryterium sukcesu:** brak zastrzeżeń albo jasna lista warunków.

#### H19 – W prototypie logowanie zastąpi przełącznik ról ⬜

- **Założenie:** Jury przyjmie demo-rolę (przełożony / oceniany / kadry / dyrektor) i opis
  docelowego logowania (SSO, Active Directory).
- **Dowód potrzebny do potwierdzenia:** mentorzy nie wymagają działającego logowania. Uwaga: MC
  wymienia uwierzytelnianie i role wprost w wymaganiach technicznych.
- **Metoda walidacji:** pytanie do mentorów obu kapituł.
- **Kryterium sukcesu:** MC akceptuje model ról i uprawnień w danych + opis; jeśli nie,
  logowanie wraca do zakresu MVP.

#### H20 – Integracja z EZD i QNT może zostać na poziomie interfejsu ⬜

- **Założenie:** Wystarczy udokumentowany eksport JSON i opis punktów integracji, bez działającego
  połączenia.
- **Dowód potrzebny do potwierdzenia:** MC pisze to wprost; KPRM trzeba dopytać.
- **Metoda walidacji:** pytanie do mentora technicznego KPRM.
- **Kryterium sukcesu:** brak wymogu działającej integracji.

### E. Strategia dwóch zgłoszeń

#### H21 – Jeden kod może wygrać w obu kapitułach ⬜

- **Założenie:** Wspólny rdzeń + przełącznik profilu (Asystent / Kompas) nie zostanie uznany za
  „kombajn” ani za brak skupienia.
- **Dowód potrzebny do potwierdzenia:** regulamin hackathonu dopuszcza zgłoszenie do dwóch
  wyzwań; mentorzy nie widzą problemu.
- **Metoda walidacji:** pytanie do organizatorów i mentorów obu stron.
- **Kryterium sukcesu:** wyraźne „tak” od organizatora.

#### H22 – Pierwszej oceny wymaga tylko Kompas ⬜

- **Założenie:** Pierwsza ocena to zakres wyłącznie dla MC; KPRM ocenia tylko ocenę okresową.
- **Dowód potrzebny do potwierdzenia:** potwierdzenie mentorów KPRM.
- **Metoda walidacji:** pytanie wprost.
- **Kryterium sukcesu:** KPRM nie oczekuje pierwszej oceny.

#### H23 – Wystarczy desktop ⬜

- **Założenie:** Obie kapituły przyjmą aplikację bez wersji mobilnej (MC wprost jej zabrania).
- **Dowód potrzebny do potwierdzenia:** KPRM nie oczekuje telefonu dla ocenianych.
- **Metoda walidacji:** pytanie do mentorów KPRM.
- **Kryterium sukcesu:** brak wymogu mobile.

#### H24 – Model kompetencyjny ma gotowe wskaźniki i opisy poziomów ⬜

- **Założenie:** Materiały MC zawierają wskaźniki behawioralne z opisami zachowań na każdym
  poziomie, więc nie musimy ich tworzyć sami.
- **Dowód potrzebny do potwierdzenia:** pliki z Discorda.
- **Metoda walidacji:** przegląd materiałów zaraz po udostępnieniu.
- **Kryterium sukcesu:** każda kompetencja ma wskaźniki i opisy poziomów; jeśli nie, pytamy
  mentora, jak je uzupełnić.
