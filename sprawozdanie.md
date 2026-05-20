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

### 0.1 Skład zespołu i podział pracy

**Liczba członków zespołu:** 3

| # | Imię i nazwisko | Rola w zespole | Zakres odpowiedzialności / wkład w projekt |
|---|----------------|----------------|--------------------------------------------|
| 1 | Kacper S. | _not done_ | __not done__ |
| 2 | Kacper H. | _not done_ | __not done__ |
| 3 | Szymon N. | _not done_ | __not done__ |

> _Podział pracy w obecnej fazie projektu (analiza wymagań) został wykonany wspólnie; w kolejnych fazach (projekt techniczny, implementacja, testy) zadania będą rozdzielane zgodnie z kompetencjami członków zespołu._

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
