# AI Workflow — jak pracowałem z LLM

Ten plik pokazuje **sposób pracy**, a nie historię rozmów z AI.

Nie chodziło mi o kopiowanie gotowych odpowiedzi. Największą wartością było nauczenie się, jak przekazać modelowi odpowiedni kontekst, postawić jasny cel, przetestować rezultat i wrócić z kolejną iteracją.

---

## 1. Mój schemat pracy

Najczęściej pracowałem w takim cyklu:

**1. Definiuję problem**  
Co konkretnie nie działa albo co chcę usprawnić?

**2. Dodaję kontekst**  
Jak działa obecny system? Jakie są ograniczenia? Jakich elementów nie chcę zmieniać?

**3. Określam efekt**  
Jak poznam, że zadanie jest wykonane dobrze?

**4. Korzystam z AI**  
Proszę o rozwiązanie, analizę lub kilka możliwych wariantów.

**5. Testuję**  
Sprawdzam wynik na realnych danych i działającym systemie.

**6. Wracam z wynikiem**  
Jeśli coś nie działa, przekazuję AI logi, screen, błąd lub nowe dane i zawężam problem.

To pozwalało mi szybko iterować bez zgadywania.

---

## 2. Przykład — ograniczenie fałszywych alarmów

### Problem

System generował alerty o bardzo wysokim priorytecie dla aktywności, która wyglądała na normalną pracę Windows.

### Jak pracowałem z AI?

Zamiast pytać ogólnie:

> „Dlaczego SIEM robi fałszywe alerty?”

przekazałem modelowi:

- typ alertu,
- konkretne zdarzenia źródłowe,
- surowe logi,
- identyfikatory zdarzeń,
- informację, jak działa obecna reguła,
- wymaganie, aby ograniczyć false positive bez wyłączania prawdziwej detekcji.

### Przykładowa forma promptu

> „Przeanalizuj poniższe zdarzenia i ustal, czy obecna reguła błędnie traktuje normalną aktywność systemową jako eskalację uprawnień. Zależy mi na ograniczeniu false positive, ale nie chcę wyłączać całej klasy detekcji. Najpierw wyjaśnij wzorzec w danych, a dopiero potem zaproponuj zmianę.”

### Rezultat

Po analizie rzeczywistych danych udało się rozróżnić normalne logowania usług systemowych od bardziej wartościowych przypadków.

**Wniosek:** AI przyspieszyło analizę, ale decyzja została oparta na danych i testach.

---

## 3. Przykład — zbyt agresywna detekcja aktywności sieciowej

### Problem

Pierwsza wersja mechanizmu wykrywania skanowania portów traktowała część zwykłego ruchu sieciowego jako podejrzaną.

### Podejście

Przekazałem AI:

- przykładowe rekordy sieciowe,
- zachowanie obecnej reguły,
- przykłady false positive,
- oczekiwany rezultat,
- warunek: nie stosować prostego „wyciszenia” całego hosta.

### Przykładowa forma promptu

> „Nie chcę whitelistować całego komputera, bo wtedy prawdziwe zagrożenie z tego hosta też zostałoby ukryte. Zaproponuj sposób odróżnienia zwykłych połączeń wychodzących od zachowania rzeczywiście przypominającego skanowanie.”

### Rezultat

Logika została zawężona do bardziej sensownych wzorców zamiast prostego alarmowania na podstawie pojedynczych połączeń.

**Wniosek:** dobry prompt zawiera nie tylko cel, ale też informację, czego rozwiązanie nie może zrobić.

---

## 4. Przykład — szybkie debugowanie błędu

### Problem

Po dodaniu nowej funkcji dashboard przestał poprawnie pobierać dane i zwracał błąd 500.

### Podejście

Zamiast opisywać problem z pamięci, dostarczyłem:

- dokładny komunikat błędu,
- nazwę funkcji,
- adres wywołania,
- kontekst ostatniej zmiany.

### Rezultat

Błąd został szybko zawężony do konfliktu nazwy parametru z wbudowaną funkcją języka.

**Wniosek:** przy debugowaniu jakość danych wejściowych dla LLM jest ważniejsza niż długość promptu.

---

## 5. Czego nauczyłem się o prompt engineeringu?

Dla mnie dobry prompting to nie „magiczne polecenia”.

Największą różnicę robi:

- **kontekst** — model musi wiedzieć, z czym pracuje,
- **cel** — rezultat musi być jasno określony,
- **ograniczenia** — czego rozwiązanie nie może zepsuć,
- **dane** — przykłady są lepsze niż ogólne opisy,
- **weryfikacja** — odpowiedź AI to hipoteza, dopóki jej nie sprawdzę,
- **iteracja** — kolejne prompty powinny wykorzystywać wynik poprzedniego testu.

---

## 6. Jak wykorzystałbym ten sposób pracy w danych biznesowych?

Ten sam workflow można zastosować do codziennych zadań analitycznych.

Przykład:

**Problem:** dane o lokalizacjach pochodzą z kilku źródeł i mają różne formaty.

**Proces:**

1. określenie wspólnego formatu,
2. wykorzystanie prostego skryptu do zebrania i połączenia danych,
3. użycie AI do klasyfikacji niejednoznacznych rekordów,
4. wskazanie braków i konfliktów,
5. ręczna weryfikacja wyjątków,
6. zapis powtarzalnego procesu na przyszłość.

Cel jest prosty: **mniej ręcznego przeklejania danych, więcej czasu na analizę i decyzje.**
