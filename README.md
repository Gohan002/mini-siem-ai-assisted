# Mini SIEM — AI-Assisted Automation Project

> Projekt własny pokazujący, jak wykorzystuję AI do szybkiego uczenia się, pracy z danymi, automatyzacji i budowania działających rozwiązań od pomysłu do gotowego efektu.

Mini SIEM to system, który automatycznie zbiera dane z logów Windows, porządkuje je, analizuje i pokazuje najważniejsze informacje w czytelnym panelu.

Projekt stworzyłem od podstaw, intensywnie wykorzystując **ChatGPT i Claude** jako codziennych asystentów do nauki, rozwiązywania problemów, tworzenia kolejnych funkcji i automatyzowania powtarzalnej pracy.

![Dashboard Mini SIEM](assets/dashboard.png)

---

## Co zbudowałem?

Zbudowałem działający system od A do Z:

**dane → uporządkowanie → analiza → automatyzacja → czytelny wynik**

System potrafi m.in.:

- automatycznie zbierać dane z logów Windows,
- porządkować tysiące zdarzeń do jednej, spójnej formy,
- wykrywać wybrane nietypowe sytuacje,
- tworzyć alerty i nadawać im priorytet,
- filtrować i przeszukiwać dane,
- analizować użytkowników, komputery i adresy IP,
- pokazywać historię konkretnego zdarzenia,
- prezentować wyniki w czytelnym dashboardzie.

Najważniejsze było dla mnie nie samo napisanie aplikacji, ale zbudowanie całego procesu tak, aby jak najwięcej pracy wykonywało się automatycznie.

---

## Dlaczego zrobiłem ten projekt?

Chciałem sprawdzić, jak daleko można dojść, traktując AI nie tylko jako narzędzie do zadawania pojedynczych pytań, ale jako **codziennego partnera do pracy**.

Założyłem sobie ambitny cel: zbudować kompletny, działający system, mimo że część wykorzystywanych narzędzi poznawałem dopiero podczas tworzenia projektu.

Projekt był dla mnie praktycznym ćwiczeniem z:

- pracy z dużą liczbą danych,
- automatyzacji powtarzalnych czynności,
- analitycznego rozwiązywania problemów,
- szybkiego uczenia się nowych narzędzi,
- prompt engineeringu,
- sprawdzania i poprawiania rezultatów generowanych przy wsparciu AI.

---

## AI-Assisted Development & Prompt Engineering

ChatGPT i Claude były jednymi z głównych narzędzi wykorzystywanych podczas tworzenia projektu.

Nie traktowałem AI jako prostego generatora kodu. Wykorzystywałem je jako:

- **asystenta** — do szybkiego przygotowywania pierwszych wersji rozwiązań,
- **nauczyciela** — do poznawania nowych narzędzi dokładnie wtedy, gdy były mi potrzebne,
- **partnera analitycznego** — do szukania przyczyn błędów i porównywania możliwych rozwiązań,
- **narzędzie automatyzacji** — do skracania czasu potrzebnego na powtarzalne zadania.

Mój typowy sposób pracy wyglądał tak:

**problem → kontekst → precyzyjny prompt → rozwiązanie → test → analiza → poprawa**

Kluczowe było dla mnie przekazywanie AI pełnego kontekstu:

- jaki jest cel,
- jak obecnie działa system,
- jakie są ograniczenia,
- czego nie chcę zmieniać,
- jaki powinien być rezultat końcowy.

Nie przyjmowałem odpowiedzi AI bez weryfikacji. Każdą większą zmianę sprawdzałem na działającym systemie i rzeczywistych danych.

---

## Przykład pracy z AI

Podczas testowania system zaczął generować alarmy, które początkowo wyglądały jak poważne zdarzenia bezpieczeństwa.

Zamiast analizować wszystko ręcznie:

1. zebrałem rzeczywiste dane źródłowe,
2. przekazałem AI kontekst problemu,
3. wspólnie przeanalizowaliśmy powtarzające się wzorce,
4. zidentyfikowałem źródło błędnej klasyfikacji,
5. poprawiłem sposób przetwarzania danych,
6. ponownie przetestowałem rezultat.

Efektem było ograniczenie fałszywych alarmów bez wyłączania właściwej analizy.

Ten przykład dobrze pokazuje mój sposób pracy z AI:  
**nie pytam tylko „co zrobić?”, ale wykorzystuję AI do szybszego przechodzenia od problemu do zweryfikowanego rozwiązania.**

---

## Automatyzacja zamiast ręcznej pracy

Jednym z głównych założeń projektu było eliminowanie powtarzalnych czynności.

Zamiast ręcznie:

- przeglądać tysiące zdarzeń,
- porównywać dane,
- wyszukiwać ważne przypadki,
- łączyć informacje z różnych miejsc,

system wykonuje dużą część tych działań automatycznie.

To podejście chcę wykorzystywać również w pracy z danymi biznesowymi:

**jeżeli coś jest powtarzalne, warto sprawdzić, czy można to uprościć, zautomatyzować albo wesprzeć AI.**

---

## Jak przekładam to na pracę z danymi?

Projekt dotyczy cyberbezpieczeństwa, ale sposób pracy jest uniwersalny.

Ten sam model można zastosować np. przy danych o lokalizacjach sklepów:

**zbieranie danych → czyszczenie → porządkowanie → weryfikacja → analiza → wynik**

Przykładowe zastosowania:

- łączenie informacji z kilku źródeł,
- automatyczne porządkowanie danych,
- wykrywanie braków i niespójności,
- przygotowywanie prostych skryptów eliminujących ręczną pracę,
- wykorzystanie LLM do klasyfikacji informacji,
- szybkie przygotowanie danych do dalszej analizy,
- tworzenie powtarzalnych procesów zamiast wykonywania tych samych czynności ręcznie.

To właśnie obszar **AI + dane + automatyzacja** chcę rozwijać dalej.

---

## System w praktyce

### Dashboard

Czytelny podgląd najważniejszych danych, alertów i aktywności.

![Dashboard](assets/dashboard.png)

### Alerty

Widok pozwalający szybko przejść od ogólnego alarmu do szczegółów i dalszej analizy.

![Alerts](assets/alerts.png)

### Szczegóły zdarzenia

Możliwość sprawdzenia pełnego kontekstu konkretnego zdarzenia.

![Event detail](assets/event-detail.png)

### Panel systemowy

Podgląd stanu systemu i automatycznych procesów analitycznych.

![System](assets/system.png)

---

## Czego nauczył mnie ten projekt?

Największa wartość projektu nie wynika z jednej konkretnej technologii.

Projekt nauczył mnie przede wszystkim:

- jak precyzyjnie przekazywać AI kontekst i oczekiwany rezultat,
- jak dzielić duży problem na mniejsze, wykonalne zadania,
- jak szybko uczyć się nowych narzędzi z pomocą LLM,
- jak automatyzować powtarzalne czynności,
- jak weryfikować odpowiedzi AI na realnych danych,
- jak poprawiać proces na podstawie wyników testów,
- jak przejść od pomysłu do działającego rozwiązania.

---

## Wykorzystane narzędzia

**Technologie:**  
Python • PostgreSQL • FastAPI • Docker • PowerShell • HTML/CSS/JavaScript

**Wsparcie AI:**  
ChatGPT • Claude

Technologie były dla mnie środkiem do celu — najważniejsze było stworzenie działającego procesu, który automatycznie zbiera, porządkuje i analizuje dane.

---

## Struktura projektu

```text
mini-siem-ai-assisted/
│
├── agent/        # zbieranie danych
├── backend/      # analiza i logika systemu
├── frontend/     # panel użytkownika
├── assets/       # screenshoty do README
├── docker-compose.yml
├── .env.example
└── README.md
```

---

## Uruchomienie projektu

Projekt działa lokalnie i składa się z bazy danych, modułu analitycznego, agenta zbierającego dane oraz panelu użytkownika.

Skrócona kolejność uruchomienia:

1. uruchomienie bazy danych,
2. uruchomienie backendu,
3. uruchomienie agenta,
4. uruchomienie panelu webowego.

Szczegółowa konfiguracja może zostać opisana osobno w dokumentacji technicznej.

---

## Status

Projekt jest rozwijany i służy mi jako praktyczne środowisko do nauki:

- automatyzacji,
- pracy z danymi,
- analizy,
- prompt engineeringu,
- AI-assisted development.

Kolejne usprawnienia skupiają się przede wszystkim na jakości danych, ograniczaniu ręcznej pracy i jeszcze lepszym wykorzystaniu AI w analizie.
