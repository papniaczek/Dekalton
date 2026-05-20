# Sprawozdanie z projektu — Sklep Sportowy "Dekalton"

**Temat projektu:** Internetowy sklep sportowy Dekalton

---

## 0. Metryczka

| Pole | Wartość |
|------|---------|
| Uczelnia | Politechnika Białostocka |
| Wydział | Informatyki |
| Kierunek studiów | Informatyka |
| Przedmiot | Inżynieria oprogramowania |
| Rok studiów | II rok |
| Semestr studiów | semestr letni 2025/2026 |
| Prowadzący zajęcia | mgr Bruno Mirčevski |
| Data przekazania sprawozdania | _xx-xx-xxxx_ |

### 0.1 Skład zespołu i podział pracy

**Liczba członków zespołu:** 3

| # | Imię i nazwisko | Rola w zespole | Zakres odpowiedzialności / wkład w projekt |
|---|----------------|----------------|--------------------------------------------|
| 1 | Kacper S. | członek zespołu | wspólne opracowanie wszystkich sekcji sprawozdania |
| 2 | Kacper H. | członek zespołu | wspólne opracowanie wszystkich sekcji sprawozdania |
| 3 | Szymon N. | członek zespołu | wspólne opracowanie wszystkich sekcji sprawozdania |

> _Na obecnym etapie projektu (analiza wymagań — punkty 1–3) prace prowadzone są wspólnie przez wszystkich członków zespołu. Szczegółowy podział obowiązków zostanie doprecyzowany w kolejnych fazach projektu (projekt techniczny, implementacja, testy)._

### 0.2 Proponowana punktacja

| Podpunkt sprawozdania | Proponowana liczba punktów |
|-----------------------|----------------------------|
| 1. Treść zadania projektowego | _x pkt_ |
| 2. Cel, zakres, kontekst, korzyści mierzalne i niemierzalne | _x pkt_ |
| 3. Słownik | _x pkt_ |
| **Razem** | **_<suma>_ pkt** |

### 0.3 Repozytorium projektu

| Pole | Wartość |
|------|---------|
| Adres publiczny repozytorium | _https://github.com/papniaczek/Dekalton_ |
| System kontroli wersji | _GitHub_ |
| Widoczność | _publiczne_ |
| Sposób uzyskania dostępu | _dostęp publiczny — wystarczy otworzyć link_ |
| Główna gałąź (branch) | _main_ |
| Lokalizacja sprawozdania w repo | _/sprawozdanie/sprawozdanie.md_ |

---

## 1. Treść zadania projektowego

Przedmiotem projektu jest zaprojektowanie i wytworzenie internetowego sklepu sportowego o nazwie **Dekalton**, na wzór sklepu Decathlon. System ma postać aplikacji webowej dostępnej dla trzech grup użytkowników:

- **gości** (niezarejestrowanych klientów),
- **zarejestrowanych klientów** (osób prywatnych oraz klubów sportowych),
- **administratorów** (pracowników sklepu).

System Dekalton obejmuje następujące moduły funkcjonalne:

- prezentację katalogu produktów sportowych pogrupowanych według dyscyplin sportowych (np. piłka nożna, bieganie, kolarstwo, fitness, sporty wodne, sporty zimowe) wraz z wariantami produktów (rozmiar, kolor, płeć, wiek docelowy);
- mechanizm wyszukiwania i filtrowania produktów po cechach takich jak dyscyplina, kategoria, marka, cena, rozmiar, kolor, ocena;
- koszyk zakupowy oraz proces składania zamówień (checkout) z wyborem metody dostawy i płatności;
- obsługę płatności online za pośrednictwem zewnętrznego operatora płatniczego (BLIK, karta, szybki przelew, płatność przy odbiorze);
- zarządzanie kontem klienta (rejestracja, logowanie, dane adresowe, historia zamówień, lista życzeń);
- panel administracyjny służący do zarządzania produktami, kategoriami, cenami, stanami magazynowymi, promocjami i kuponami rabatowymi;
- moduł opinii i recenzji produktów wystawianych przez klientów po zakupie i dostawie towaru;
- obsługę zwrotów towaru w ustawowym terminie 14 dni od daty dostawy.



---

## 2. Cel, zakres, kontekst oraz korzyści z wdrożenia systemu

### 2.1 Cel systemu

Celem Systemu Dekalton jest udostępnienie klientom indywidualnym oraz klubom sportowym kanału sprzedaży internetowej sprzętu sportowego, który umożliwia samodzielne wyszukanie, porównanie i zakup produktów sportowych z dostawą do domu lub do paczkomatu, a właścicielowi sklepu — prowadzenie sprzedaży 24/7 bez konieczności obsługi klienta w sklepie stacjonarnym.

### 2.2 Zakres systemu

Zakres funkcjonalny Systemu Dekalton obejmuje:

- **Front-end klienta:** katalog, wyszukiwarka, karta produktu, koszyk, checkout, konto klienta, opinie, formularz zwrotu.
- **Back-end administracyjny:** zarządzanie produktami, wariantami, kategoriami, stanami magazynowymi, cenami, promocjami, zamówieniami, zwrotami, recenzjami.
- **Integracje zewnętrzne:** bramka płatnicza, operator dostawy, system pocztowy do powiadomień transakcyjnych.
- **Magazyn danych:** baza produktów, klientów, zamówień, opinii, zwrotów.

### 2.3 Kontekst biznesowy

Polski rynek e-commerce sprzętu sportowego rośnie corocznie i jest zdominowany przez kilku dużych graczy. Dekalton wchodzi na ten rynek jako nowy gracz oferujący szeroki wybór dyscyplin sportowych w jednym miejscu.

**Klienci docelowi:**

- amatorzy uprawiający sport rekreacyjnie (osoby 18–55 lat);
- rodzice kupujący sprzęt dla dzieci;
- kluby sportowe i szkółki sportowe zamawiające sprzęt hurtowo;
- początkujący sportowcy poszukujący kompletnego wyposażenia.

**Skala eksploatacji (założenie projektowe):** rolę administracyjną pełni 2–5 pracowników; w pierwszym roku działalności przewiduje się ok. 10 000 zarejestrowanych klientów.

### 2.4 Korzyści mierzalne z wdrożenia systemu

Każda korzyść jest opisana wartością docelową oraz sposobem wyliczenia. Wskaźniki są mierzone w okresie 12 miesięcy od wdrożenia, jeżeli nie podano inaczej.

| # | Korzyść | Wartość docelowa | Sposób wyliczenia |
|---|---------|-----------------|-------------------|
| K1 | Wzrost przychodu ze sprzedaży online | +30% rok do roku | (Przychód_rok_2 − Przychód_rok_1) / Przychód_rok_1 × 100%, gdzie przychód = suma wartości brutto zamówień ze statusem "zrealizowane" w danym okresie |
| K2 | Współczynnik konwersji w sklepie | ≥ 2,5% | liczba zamówień złożonych / liczba unikalnych sesji × 100%, mierzony miesięcznie w narzędziu analitycznym |
| K3 | Średnia wartość koszyka (AOV) | ≥ 220 PLN | suma wartości brutto zamówień / liczba zamówień, mierzona miesięcznie |
| K4 | Współczynnik porzucenia koszyka | ≤ 65% | (liczba koszyków utworzonych − liczba koszyków zakończonych zamówieniem) / liczba koszyków utworzonych × 100% |
| K5 | Czas wczytania strony katalogu (LCP) | ≤ 2,5 s dla 75. percentyla | pomiar Largest Contentful Paint w narzędziu Web Vitals na próbie min. 1000 sesji tygodniowo |
| K6 | Średni czas obsługi zwrotu | ≤ 5 dni roboczych | średnia różnica (data_akceptacji_zwrotu − data_zgłoszenia_zwrotu) liczona w dniach roboczych |
| K7 | Wskaźnik powracających klientów | ≥ 25% | liczba klientów z ≥ 2 zamówieniami w okresie / liczba wszystkich klientów z ≥ 1 zamówieniem × 100% |
| K8 | Średnia ocena produktów | ≥ 4,2 / 5,0 | średnia arytmetyczna ocen wystawionych przez klientów w okresie |
| K9 | Dostępność systemu (uptime) | ≥ 99,5% | (czas_całkowity − czas_niedostępności) / czas_całkowity × 100%, mierzony przez monitoring zewnętrzny |

### 2.5 Korzyści niemierzalne z wdrożenia systemu

- Wzmocnienie wizerunku marki Dekalton jako nowoczesnego sprzedawcy sprzętu sportowego.
- Zwiększenie zadowolenia klientów dzięki dostępności sklepu 24/7 oraz przejrzystej prezentacji produktów.
- Łatwiejszy dostęp do sprzętu sportowego dla mieszkańców miejscowości bez sklepów stacjonarnych.
- Lepsze decyzje zakupowe klientów dzięki recenzjom innych użytkowników.
- Uproszczenie pracy administratorów dzięki zintegrowanemu panelowi zarządzania.
- Budowa relacji z klubami sportowymi jako lojalnymi klientami hurtowymi.
- Większa elastyczność w prowadzeniu akcji marketingowych (kupony, promocje sezonowe) bez angażowania pracowników sklepu stacjonarnego.

---

## 3. Słownik pojęć

Słownik definiuje terminy specyficzne dla dziedziny projektu, używane w pozostałych częściach dokumentacji. Pisownia z podkreśleniem (np. *Wariant_Produktu*) oznacza, że termin jest używany jako pojęcie modelu dziedziny.

| Termin | Definicja |
|--------|-----------|
| **System / System Dekalton** | aplikacja webowa będąca przedmiotem niniejszego projektu, składająca się z front-endu klienta i panelu administracyjnego. |
| **Gość** | użytkownik korzystający z Systemu bez założonego konta (nie jest zalogowany). |
| **Klient** | zarejestrowany użytkownik Systemu posiadający konto, mogący składać zamówienia we własnym imieniu. |
| **Klub_Sportowy** | rodzaj konta Klienta przeznaczony dla organizacji (klubów, szkółek), uprawniający do zamówień hurtowych z rabatem oraz odroczonego terminu płatności. |
| **Administrator** | pracownik sklepu posiadający uprawnienia do zarządzania zawartością Systemu (produkty, zamówienia, recenzje, zwroty). |
| **Produkt** | artykuł sportowy dostępny w sprzedaży, opisany nazwą, marką, kategorią, opisem, zdjęciami i ceną bazową. |
| **Wariant_Produktu** | konkretna odmiana Produktu różniąca się rozmiarem, kolorem, płcią lub wiekiem docelowym; każdy Wariant_Produktu posiada osobny SKU oraz własny stan magazynowy. |
| **SKU (Stock Keeping Unit)** | unikalny alfanumeryczny identyfikator Wariantu_Produktu używany do śledzenia stanu magazynowego. |
| **Kategoria_Sportu** | grupa produktów związanych z konkretną dyscypliną sportową (np. "Piłka nożna", "Bieganie", "Kolarstwo"). |
| **Kategoria_Produktu** | hierarchiczna grupa Produktów (np. "Obuwie", "Odzież", "Akcesoria"), niezależna od Kategorii_Sportu. |
| **Marka** | producent Produktu (własna marka Dekalton lub marka zewnętrzna). |
| **Katalog** | zbiór wszystkich aktywnych Produktów wystawionych na sprzedaż w Systemie. |
| **Karta_Produktu** | ekran prezentujący szczegóły jednego Produktu wraz z dostępnymi Wariantami_Produktu, zdjęciami, ceną i sekcją Recenzji. |
| **Koszyk** | tymczasowa lista wybranych Wariantów_Produktu wraz z ilościami, przypisana do sesji Gościa lub konta Klienta. |
| **Zamówienie** | utrwalona transakcja zakupu zawierająca pozycje, dane dostawy, metodę płatności, status oraz wartość; identyfikowana unikalnym numerem zamówienia. |
| **Status_Zamówienia** | stan Zamówienia w cyklu jego życia, przyjmujący jedną z wartości: NOWE, OPŁACONE, W_REALIZACJI, WYSŁANE, DOSTARCZONE, ANULOWANE, ZWRÓCONE. |
| **Checkout** | proces finalizacji zakupu obejmujący wybór adresu dostawy, sposobu dostawy, metody płatności i potwierdzenie zamówienia. |
| **Bramka_Płatnicza** | zewnętrzny operator płatności online (np. Przelewy24, Stripe), z którym System komunikuje się w celu obsługi transakcji. |
| **Stan_Magazynowy** | liczba sztuk danego Wariantu_Produktu fizycznie dostępnych do sprzedaży. |
| **Recenzja** | pisemna opinia Klienta o Produkcie zawierająca ocenę liczbową w skali 1–5 oraz opcjonalny komentarz. |
| **Zwrot** | proces oddania zakupionego Produktu w terminie ustawowym (14 dni), prowadzący do zwrotu środków na rzecz Klienta. |
| **Lista_Życzeń** | lista Produktów zapisanych przez Klienta do późniejszego rozważenia (bez rezerwacji magazynowej), o maksymalnym rozmiarze 200 pozycji. |
| **Promocja** | czasowe obniżenie ceny Produktu lub grupy Produktów, opisane datą rozpoczęcia, datą zakończenia oraz wartością rabatu (procentową lub kwotową). |
| **Kupon_Rabatowy** | kod alfanumeryczny umożliwiający zastosowanie rabatu na Zamówienie podczas Checkoutu. |
| **Adres_Dostawy** | dane adresowe wskazane przez Klienta jako miejsce dostarczenia Zamówienia. |
| **Kurier** | zewnętrzny operator logistyczny realizujący dostawę Zamówienia (np. InPost, DPD). |

---

## 4. Perspektywa przypadków użycia

### 4.1 Diagramy przypadków użycia

#### 4.1.1 Aktorzy

W Systemie Dekalton wyróżniamy następujących aktorów:

**Aktorzy ludzcy:**

- **Gość** — niezarejestrowany użytkownik Systemu. Ma dostęp do publicznej części sklepu: przeglądania Katalogu, wyszukiwania Produktów, dodawania Produktów do Koszyka oraz złożenia Zamówienia bez rejestracji konta. Nie może wystawiać Recenzji ani prowadzić Listy_Życzeń.
- **Klient** — zarejestrowany użytkownik Systemu posiadający konto. Dziedziczy wszystkie uprawnienia Gościa, a dodatkowo: zarządza danymi konta, prowadzi Listę_Życzeń, przegląda historię Zamówień, wystawia Recenzje (po dostawie zakupionego Produktu) oraz zgłasza Zwroty w terminie 14 dni od dostawy.
- **Klub_Sportowy** — wyspecjalizowany typ Klienta (organizacja). Po weryfikacji przez Administratora otrzymuje dostęp do cennika hurtowego oraz do zamówień z odroczonym terminem płatności.
- **Administrator** — pracownik sklepu zarządzający zawartością Systemu. Tworzy i edytuje Produkty, Warianty_Produktu, Kategorie, Promocje i Kupony_Rabatowe, moderuje Recenzje, obsługuje Zamówienia (zmiana Statusu_Zamówienia, dodanie numeru przesyłki) oraz akceptuje lub odrzuca zgłoszone Zwroty.

**Aktorzy systemowi (zewnętrzni):**

- **Bramka_Płatnicza** — zewnętrzny system obsługujący płatności online (BLIK, karta, szybki przelew). Komunikuje się z Systemem podczas Checkoutu (autoryzacja transakcji) oraz przy realizacji zwrotu środków po akceptacji Zwrotu.
- **System_Pocztowy** — zewnętrzny system wysyłki wiadomości e-mail (potwierdzenia rejestracji, potwierdzenia Zamówień, powiadomienia o statusie wysyłki, powiadomienia o moderacji Recenzji, formularze Zwrotu).
- **System_Kuriera** — zewnętrzny system operatora logistycznego (np. InPost, DPD), z którym System wymienia numery przesyłek i linki do śledzenia.

#### 4.1.2 Lista przypadków użycia

Zidentyfikowano 15 przypadków użycia pogrupowanych w pięć obszarów funkcjonalnych:

| ID | Przypadek użycia | Aktor główny | Aktorzy wspierający |
|----|------------------|--------------|---------------------|
| UC-01 | Przeglądanie Katalogu | Gość, Klient | — |
| UC-02 | Wyszukiwanie i filtrowanie Produktów | Gość, Klient | — |
| UC-03 | Zarządzanie Koszykiem | Gość, Klient | — |
| UC-04 | Złożenie Zamówienia (Checkout) | Klient (lub Gość) | Bramka_Płatnicza, System_Pocztowy |
| UC-05 | Opłacenie Zamówienia | Klient (lub Gość) | Bramka_Płatnicza, System_Pocztowy |
| UC-06 | Rejestracja konta Klienta | Gość | System_Pocztowy |
| UC-07 | Logowanie do Systemu | Klient, Administrator | — |
| UC-08 | Zarządzanie kontem (dane, adresy, Lista_Życzeń) | Klient | — |
| UC-09 | Wystawienie Recenzji | Klient | — |
| UC-10 | Zgłoszenie Zwrotu | Klient | System_Pocztowy, Bramka_Płatnicza |
| UC-11 | Zarządzanie Produktami i Wariantami_Produktu | Administrator | — |
| UC-12 | Zarządzanie Promocjami i Kuponami_Rabatowymi | Administrator | — |
| UC-13 | Obsługa Zamówień (zmiana statusu, wysyłka) | Administrator | System_Pocztowy, System_Kuriera |
| UC-14 | Moderacja Recenzji | Administrator | System_Pocztowy |
| UC-15 | Akceptacja / odrzucenie Zwrotu | Administrator | Bramka_Płatnicza, System_Pocztowy |

#### 4.1.3 Diagram przypadków użycia

![Diagram przypadków użycia Systemu Dekalton](diagram-przyp-uzycia/4-1-diagram.png)

> _Diagram przedstawia wszystkie 15 przypadków użycia z tabeli w punkcie 4.1.2 wraz z powiązaniami z aktorami (Gość, Klient, Klub_Sportowy, Administrator, Bramka_Płatnicza, System_Pocztowy, System_Kuriera). Uwzględnione są relacje dziedziczenia ról (Gość → Klient → Klub_Sportowy), relacja «include» (UC-04 Złożenie Zamówienia → UC-05 Opłacenie Zamówienia, UC-04 → UC-03 Zarządzanie Koszykiem) oraz relacja «extend» (UC-15 Akceptacja Zwrotu rozszerza UC-10 Zgłoszenie Zwrotu)._

### 4.1.2 Opisy tekstowe wybranych przypadków użycia

Do szczegółowego opisu wybrano trzy przypadki użycia o najbardziej rozbudowanych przepływach alternatywnych: złożenie Zamówienia, zgłoszenie Zwrotu oraz wystawienie Recenzji.

#### UC-04 Złożenie Zamówienia (Checkout)

**Aktorzy:**

- *Główny:* Klient (lub Gość składający Zamówienie bez rejestracji)
- *Wspierający:* Bramka_Płatnicza, System_Pocztowy

**Warunki początkowe:**

- Klient ma w Koszyku co najmniej jedną pozycję o Stanie_Magazynowym ≥ 1.

**Warunki końcowe (sukces):**

- W Systemie utworzono Zamówienie ze Statusem_Zamówienia "OPŁACONE" lub "NOWE" (dla płatności przy odbiorze).
- Stan_Magazynowy odpowiednich Wariantów_Produktu został pomniejszony.
- Klient otrzymał e-mail z potwierdzeniem.

**Przepływ podstawowy:**

1. Klient wybiera akcję „Przejdź do Checkoutu" w Koszyku.
2. System wyświetla formularz wyboru Adresu_Dostawy.
3. Klient wskazuje Adres_Dostawy (lub wprowadza nowy).
4. System wyświetla dostępne sposoby dostawy (kurier / paczkomat / odbiór osobisty) i wylicza koszt dostawy.
5. Klient wybiera sposób dostawy.
6. System wyświetla dostępne metody płatności.
7. Klient wybiera metodę płatności.
8. System prezentuje podsumowanie Zamówienia (pozycje, koszt dostawy, łączna wartość, opcjonalny Kupon_Rabatowy).
9. Klient potwierdza Zamówienie.
10. System tworzy Zamówienie ze Statusem "NOWE", rezerwuje Stan_Magazynowy i nadaje numer w formacie `DK-{rok}-{numer}`.
11. System przekierowuje Klienta do Bramki_Płatniczej (z parametrami transakcji).
12. Klient finalizuje płatność w Bramce_Płatniczej.
13. Bramka_Płatnicza zwraca status „płatność_zaakceptowana".
14. System ustawia Status_Zamówienia na "OPŁACONE" i zleca System_Pocztowemu wysyłkę e-maila z potwierdzeniem.
15. System wyświetla Klientowi stronę z potwierdzeniem Zamówienia.

**Przepływy alternatywne:**

- **A1. Niedostępność pozycji w Koszyku (krok 9–10):** jeśli pomiędzy rozpoczęciem Checkoutu a potwierdzeniem Stan_Magazynowy któregoś Wariantu_Produktu spadł poniżej ilości w Koszyku, System przerywa Checkout i wyświetla listę pozycji wymagających zmiany. Klient wraca do Koszyka.
- **A2. Płatność odrzucona (krok 13):** Bramka_Płatnicza zwraca „płatność_odrzucona". Status_Zamówienia pozostaje "NOWE", Klient widzi komunikat z przyczyną i może ponowić płatność (do 5 prób).
- **A3. Timeout płatności (krok 12):** Klient nie sfinalizuje płatności w 60 minut od utworzenia Zamówienia. System ustawia Status_Zamówienia "ANULOWANE", zwalnia rezerwację Stanu_Magazynowego i wysyła e-mail informacyjny.
- **A4. Niedostępność Bramki_Płatniczej (krok 11–13):** Bramka_Płatnicza nie odpowiada w 30 sekund. System wyświetla komunikat o tymczasowej niedostępności i pozwala wybrać inną metodę płatności bez utraty danych Zamówienia.
- **A5. Płatność przy odbiorze (krok 7):** Klient wybiera „płatność przy odbiorze" — System pomija kroki 11–13, tworzy Zamówienie ze Statusem "NOWE" i przekazuje je do realizacji.
- **A6. Nieprawidłowy Kupon_Rabatowy (krok 8):** kod nie istnieje / wygasł / niespełnione warunki — System odrzuca kupon, zachowuje wartość Zamówienia bez rabatu i informuje Klienta o przyczynie.

**Częstotliwość i czas realizacji:**

- *Częstotliwość typowa:* ok. 200–400 wykonań na dobę (założenie projektowe ~10 000 klientów rocznie, konwersja ≥ 2,5%, średnio ~25 zamówień / dobę × szczyty).
- *Spiętrzenia:* okres przedświąteczny (XI–XII), wyprzedaże sezonowe — wzrost do 4–5× ruchu typowego (≈1500 wykonań / dobę).
- *Typowy czas realizacji:* 3–5 minut od rozpoczęcia Checkoutu do potwierdzenia.
- *Maksymalny czas realizacji:* 60 minut (po tym czasie Zamówienie jest automatycznie anulowane przez System).

**Wartości uzyskane przez aktorów:**

- *Klient:* złożone Zamówienie, potwierdzenie e-mail z numerem Zamówienia i przewidywanym terminem dostawy, prawo do zwrotu w terminie 14 dni.
- *Sklep (właściciel):* nowe przychody, dane do realizacji wysyłki, dane analityczne dla wskaźników K1 (przychód), K2 (konwersja), K3 (AOV).

---

#### UC-10 Zgłoszenie Zwrotu

**Aktorzy:**

- *Główny:* Klient
- *Wspierający:* System_Pocztowy, Bramka_Płatnicza (w fazie akceptacji), Administrator (w UC-15)

**Warunki początkowe:**

- Klient jest zalogowany.
- Istnieje Zamówienie Klienta o Statusie_Zamówienia "DOSTARCZONE".
- Od daty dostawy upłynęło nie więcej niż 14 dni kalendarzowych.

**Warunki końcowe (sukces):**

- Utworzony rekord Zwrotu ze statusem początkowym (przed weryfikacją Administratora).
- Wygenerowany formularz Zwrotu (PDF) udostępniony i wysłany e-mailem.

**Przepływ podstawowy:**

1. Klient otwiera historię Zamówień i wybiera Zamówienie kwalifikujące się do Zwrotu.
2. Klient wybiera akcję „Zgłoś zwrot".
3. System wyświetla pozycje Zamówienia z możliwością wskazania ilości do zwrotu.
4. Klient zaznacza pozycje i ilości (od 1 do liczby zakupionych sztuk).
5. Klient wybiera przyczynę Zwrotu z predefiniowanej listy.
6. Klient potwierdza zgłoszenie.
7. System tworzy rekord Zwrotu i generuje formularz w PDF (≤ 30 s).
8. System udostępnia formularz do pobrania oraz wysyła go e-mailem przez System_Pocztowy (≤ 5 min).
9. System wyświetla Klientowi potwierdzenie zgłoszenia z instrukcją odesłania towaru.

**Przepływy alternatywne:**

- **A1. Termin upłynął (krok 1–2):** od daty dostawy minęło więcej niż 14 dni — System odrzuca zgłoszenie i wyświetla komunikat o upłynięciu terminu, nie tworzy rekordu Zwrotu.
- **A2. Akceptacja Zwrotu przez Administratora (rozszerzenie UC-15):** po fizycznym otrzymaniu towaru Administrator akceptuje Zwrot — System zwiększa Stan_Magazynowy, inicjuje zwrot środków przez Bramkę_Płatniczą (≤ 60 s) i ustawia Status_Zamówienia na "ZWRÓCONE" (lub odnotowuje zwrot częściowy). Klient otrzymuje e-mail.
- **A3. Odrzucenie Zwrotu przez Administratora (rozszerzenie UC-15):** Administrator ocenia stan towaru jako nieakceptowalny (uszkodzenie, brak metki) — System ustawia status Zwrotu na "ODRZUCONY", nie zmienia Stanu_Magazynowego, wysyła e-mail z uzasadnieniem.
- **A4. Błąd Bramki_Płatniczej przy zwrocie środków:** System ponawia operację do 3 razy w odstępach ≥ 24 h i powiadamia Administratora o nieudanej operacji.

**Częstotliwość i czas realizacji:**

- *Częstotliwość typowa:* przy założonym wskaźniku zwrotów ~10% Zamówień: ≈ 20–40 zgłoszeń / dobę.
- *Spiętrzenia:* po sezonowych wyprzedażach i okresie świątecznym (do 100 zgłoszeń / dobę).
- *Typowy czas realizacji (zgłoszenie po stronie Klienta):* 2–4 minuty.
- *Maksymalny czas obsługi całego procesu (do zwrotu środków):* 14 dni kalendarzowych od akceptacji Zwrotu (zgodnie z prawem); operacyjny cel K6 to ≤ 5 dni roboczych do akceptacji.

**Wartości uzyskane przez aktorów:**

- *Klient:* możliwość odzyskania środków zgodnie z ustawowym prawem do zwrotu, formularz PDF, transparentny status procesu.
- *Sklep:* zorganizowany proces obsługi zwrotów, audytowalny stan magazynowy, zgodność z wymogami prawnymi.

---

#### UC-09 Wystawienie Recenzji

**Aktorzy:**

- *Główny:* Klient
- *Wspierający:* Administrator (w UC-14 — moderacja), System_Pocztowy

**Warunki początkowe:**

- Klient jest zalogowany.
- Klient zakupił Produkt w Zamówieniu o Statusie_Zamówienia "DOSTARCZONE".
- Klient nie wystawił jeszcze Recenzji dla tego Produktu w ramach tego Zamówienia.

**Warunki końcowe (sukces):**

- Utworzona Recenzja ze statusem "OCZEKUJĄCA" przekazana do moderacji.

**Przepływ podstawowy:**

1. Klient otwiera Kartę_Produktu (lub historię Zamówień) i wybiera akcję „Wystaw recenzję".
2. System weryfikuje uprawnienie Klienta do wystawienia Recenzji (zakup + Status_Zamówienia "DOSTARCZONE").
3. System wyświetla formularz: ocena 1–5 (wymagana) i komentarz (10–2000 znaków, opcjonalny).
4. Klient wprowadza ocenę i komentarz.
5. Klient zatwierdza Recenzję.
6. System zapisuje Recenzję ze statusem "OCZEKUJĄCA", ukrywa ją na Karcie_Produktu i przekazuje do kolejki moderacji (≤ 72 h).
7. System wyświetla Klientowi potwierdzenie i informuje, że Recenzja oczekuje na moderację.

**Przepływy alternatywne:**

- **A1. Brak uprawnień (krok 2):** Klient nie zakupił Produktu lub Status_Zamówienia inny niż "DOSTARCZONE" — System odrzuca żądanie i wyświetla komunikat „Recenzję mogą wystawiać wyłącznie kupujący tego produktu".
- **A2. Niepoprawny komentarz (krok 5):** komentarz krótszy niż 10 znaków lub dłuższy niż 2000 — System odrzuca zapis, zachowuje wprowadzone dane w formularzu i wyświetla komunikat o dopuszczalnej długości.
- **A3. Zatwierdzenie przez Administratora (UC-14):** Administrator zatwierdza Recenzję — System ustawia status "ZATWIERDZONA", publikuje Recenzję na Karcie_Produktu (≤ 60 s) i przelicza średnią ocenę Produktu.
- **A4. Odrzucenie przez Administratora (UC-14):** Administrator odrzuca Recenzję — System ustawia status "ODRZUCONA" i wysyła Klientowi e-mail z uzasadnieniem (≤ 60 s).
- **A5. Edycja Recenzji w 30 dni (krok 7):** Klient edytuje wcześniej zatwierdzoną Recenzję — System przywraca status "OCZEKUJĄCA", ukrywa ją na Karcie_Produktu i ponownie kieruje do moderacji.

**Częstotliwość i czas realizacji:**

- *Częstotliwość typowa:* ~10–20% klientów wystawia Recenzję — ≈ 30–80 recenzji / dobę.
- *Spiętrzenia:* po dużych kampaniach zakupowych (zwiększenie 2–3×).
- *Typowy czas realizacji (po stronie Klienta):* 1–3 minuty.
- *Maksymalny czas publikacji:* do 72 h (cel moderacji); publikacja po zatwierdzeniu w ciągu 60 s.

**Wartości uzyskane przez aktorów:**

- *Klient (autor):* możliwość podzielenia się opinią, wpływ na decyzje innych Klientów.
- *Inni Klienci:* lepsze decyzje zakupowe (korzyść niemierzalna).
- *Sklep:* materiał marketingowy, dane do wskaźnika K8 (średnia ocena ≥ 4,2 / 5,0), informacja zwrotna o jakości Produktów.

