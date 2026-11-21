# Pytania do mentorów

Lista do rozmów przy stoiskach i na Discordzie. W nawiasie numer hipotezy z
[zalozenia.md](zalozenia.md), którą pytanie sprawdza. Ta sama lista wyświetla się jako checklista
na [stronie walidacji](https://orfeliny.github.io/hacknation-zalozenia/) (odhaczenia zapisują się
w przeglądarce). Po rozmowie odhacz pytanie tutaj, dopisz odpowiedź pod nim
(albo w `wywiady/<data>-<mentor>.md`) i zmień status hipotezy.

Jak pytać:

- Najpierw pytania otwarte o praktykę („jak to wygląda u was?”), dopiero potem o nasze rozwiązanie.
  Inaczej usłyszymy uprzejme „tak, fajne”.
- Prosić o przykład z życia: „kiedy ostatnio…?”, „co poszło nie tak?”.
- Nie bronić pomysłu. Zapisywać dosłownie, zwłaszcza zaskoczenia.
- Jedna osoba pyta, druga notuje (albo nasłuch w `index.html`).

## 1. KPRM – Departament Służby Cywilnej (merytoryczni)

### Praktyka i problem

- [ ] Jak dziś wygląda ocena okresowa w typowym urzędzie, od pierwszego do ostatniego kroku? (H5)
- [ ] Który etap przełożeni najczęściej odkładają na ostatnią chwilę? (H1)
- [ ] Co przełożonym sprawia największą trudność: wybór kryteriów, opis oczekiwań, rozmowa,
   uzasadnienia czy plan rozwoju? Proszę o przykład. (H1)
- [ ] Czy przełożeni zapisują obserwacje w trakcie okresu oceny? Jeśli tak, gdzie? (H2)
- [ ] Jakie błędy formalne najczęściej wracają z kadr do poprawki? (H3)
- [ ] Ile ocen w urzędzie wymaga poprawek albo kończy się odwołaniem? Czy ktoś to liczy? (H3)
- [ ] Czy zdarzają się spory „nie wiedziałem, że tego się ode mnie oczekuje”? Jak się kończą? (H4)
- [ ] Co powinien zobaczyć oceniany, a czego nie powinien widzieć? (H4)

### Przepisy

- [ ] Czy arkusz A/B/C wynika jednoznacznie z rodzaju stanowiska? Są wyjątki? (H6)
- [ ] Jakie sytuacje kadrowe najczęściej komplikują ocenę i co z nich wynika (zmiana oceniającego,
  zmiana zadań, długotrwała nieobecność, przeniesienie)? (H7)
- [ ] Kto sporządza ocenę, gdy przełożony zmienił się w trakcie okresu? (H7)
- [ ] Jak liczyć terminy przy długiej nieobecności pracownika? (H7)
- [ ] W którą stronę idzie procedowana zmiana ustawy w części o ocenach: częstotliwość, terminy,
  elementy, skala? (H8)
- [ ] Które elementy oceny są obowiązkowe z mocy przepisów, a które to dobra praktyka? (H5)
- [ ] Jak wygląda ścieżka od wniosków z oceny do IPRZ i do wniosku o stopień służbowy? (H5)
- [ ] Czy bieżące rozmowy feedbackowe ze standardów ZZL warto pokazać jako osobny etap? (H5)
- [ ] Czy oczekujecie od nas ścieżki pierwszej oceny, czy tylko oceny okresowej? (H22)

### Rozwiązanie

- [ ] Czy projekt uzasadnienia przygotowany przez AI z odnośnikami do obserwacji przełożonego jest
  dla was do przyjęcia? Gdzie widzicie granicę? (H10, H11)
- [ ] Czy sugerowanie poziomu oceny przez AI byłoby problemem, nawet z zastrzeżeniem? (H11)
- [ ] Które sygnały HR partnera uznalibyście za przydatne, a które za przesadę? (H12)
- [ ] Czy łączenie nieobecności z sygnałem przeciążenia jest w porządku z punktu widzenia
  ochrony danych? (H13)
- [ ] Jakie działania rozwojowe i szkolenia są realnie dostępne w urzędach? Jest jakiś katalog? (H12)
- [ ] Czy aplikacja musi działać na telefonie dla ocenianych? (H23)
- [ ] Co musielibyśmy pokazać na demo, żebyście uznali proces za odwzorowany w całości? (H5)
- [ ] Co was najbardziej przekonuje w „potencjale wdrożeniowym” – instalacja, koszt, aktualizacje? (H17)

## 2. KPRM – Biuro Informatyki (techniczni)

- [ ] Jak wygląda środowisko IT małego urzędu: serwery, system operacyjny, Docker, dostęp do
  internetu? (H17)
- [ ] Czy `docker compose up` + instrukcja to dla was „łatwa instalacja”? Jeśli nie, co jest? (H17)
- [ ] Czy stos open source z backendem Convex we własnym kontenerze spełnia wymóg „bez płatnych
  licencji”? Na co patrzycie przy licencjach? (H18)
- [ ] Czy w prototypie wystarczy przełącznik ról zamiast logowania? Jakie logowanie jest docelowe
  (AD, SSO, login.gov.pl)? (H19)
- [ ] Jak wygląda dziś podpis i obieg arkusza w EZD? Czy prototyp musi coś z tym robić? (H9, H20)
- [ ] Czy działająca integracja z EZD lub systemem kadrowym jest oczekiwana, czy wystarczy opisany
  interfejs (eksport JSON / API)? (H20)
- [ ] Czy zamiana imion i nazwisk na znacznik przed wysłaniem do modelu wystarcza jako
  anonimizacja? Czego jeszcze byście oczekiwali? (H16)
- [ ] Czy urzędy mogą uruchomić lokalny model językowy (Bielik / PLLuM)? Na jakim sprzęcie? (H15)
- [ ] Jak urząd wdraża aktualizacje aplikacji: sam, przez dostawcę, przez centralny serwis? (H8)
- [ ] Jakie wymagania bezpieczeństwa i dostępności (WCAG) zwykle odrzucają rozwiązania? (H17)
- [ ] Czy dane ocen mogą leżeć w chmurze krajowej, czy tylko w urzędzie? (H16, H18)

## 3. Ministerstwo Cyfryzacji – Kompas (merytoryczni)

- [ ] Czy model kompetencyjny ma wskaźniki behawioralne z opisem zachowań na każdym poziomie? Jeśli
  nie, jak mamy je uzupełnić? (H24)
- [ ] Jak liczyć sugerowany poziom z wybranych zachowań: średnia, mediana, reguła progowa? Macie
  preferencję? (H11)
- [ ] Czy jawny algorytm z pokazanym wyliczeniem jest akceptowalny, a sugestia modelu AI nie? (H11)
- [ ] Co dokładnie różni ścieżkę pierwszej oceny od oceny okresowej w praktyce przełożonego? (H22)
- [ ] Które części formularza wypełnia się w pierwszej ocenie, a które w okresowej?
- [ ] Czy możecie dać 5-10 pytań, które jury zada asystentowi? Albo przykład pytania, na którym
  poległy inne narzędzia? (H14)
- [ ] Co uznacie za poprawną odpowiedź: treść, wskazanie przepisu, cytat? (H14)
- [ ] Jak asystent ma się zachować, gdy pytanie wykracza poza bazę wiedzy? Wystarczy „nie wiem”
  z sugestią, gdzie szukać? (H14)
- [ ] Co ma zobaczyć HR / administrator: statusy, terminy, przypomnienia? Coś jeszcze? (H3)
- [ ] Do czego służą 3 szablony opisów stanowiska? Mamy z nich dobierać kryteria? (H6)
- [ ] Czego brakuje dziś w poradnikach KPRM, o co przełożeni pytają najczęściej? (H1)

## 4. Ministerstwo Cyfryzacji – Kompas (techniczni)

- [ ] Czy w prototypie wymagacie działającego logowania i ról, czy wystarczy model uprawnień
  w danych i opis? (H19)
- [ ] Czy lokalny Bielik / PLLuM spełnia wymóg „wyłącznie darmowe narzędzia AI”? A darmowy limit
  API komercyjnego modelu? (H15)
- [ ] Jaki format API i dokumentacji oczekujecie pod przyszłą integrację z EZD i QNT? (H20)
- [ ] Czy PDF z „Drukuj → Zapisz jako PDF” wystarczy, czy PDF ma generować serwer? (H20)
- [ ] Jak sprawdzicie bezpieczeństwo AI: prompt injection, wycieki danych, halucynacje? (H14, H16)
- [ ] Na jakich przeglądarkach i rozdzielczościach ma działać aplikacja? (H23)

## 5. Organizatorzy hackathonu

- [ ] Czy jeden zespół może zgłosić jeden kod do dwóch wyzwań (KPRM i MC)? (H21)
- [ ] Czy obie kapituły muszą dostać osobne repozytorium, czy wystarczy jedno z dwoma profilami? (H21)
- [ ] Jak wygląda demo: na żywo, nagranie, ile minut, czy jury klika samo? (H21)
- [ ] Do kiedy można aktualizować repozytorium i linki po zgłoszeniu?
- [ ] Czy wolno korzystać z płatnych narzędzi AI do pisania kodu, jeśli aplikacja używa tylko
  darmowego modelu? (H15)

## Szybka ściąga na 5 minut przy stoisku

Gdy czasu jest mało, pytaj w tej kolejności:

- [ ] Co przełożonym sprawia największą trudność? Przykład z ostatniej oceny. (H1)
- [ ] Czy AI może proponować poziom oceny? Gdzie jest granica? (H11)
- [ ] Co musimy pokazać na demo, żeby proces uznać za kompletny? (H5)
- [ ] Czy prototyp potrzebuje logowania i podpisu, czy wystarczy opis? (H9, H19)
- [ ] Czy możecie dać przykładowe pytania dla asystenta? (H14)
