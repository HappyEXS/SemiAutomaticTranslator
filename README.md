# Dokumentacja Wstępna Projektu: Narzędzie do Półautomatycznego Tłumaczenia Zbiorów Tekstu

## Opis Zadania

Celem projektu jest stworzenie narzędzia wspierającego proces automatyzacji tłumaczenia zbiorów tekstu. Aplikacja umożliwi użytkownikowi wczytanie pliku ze zbiorem danych, wybór kolumn do tłumaczenia, określenie zakresu rzędów przeznaczonych do tłumaczenia oraz ignorowanie wybranych indeksów/rzędów. Użytkownik będzie miał możliwość wyboru języka/językow źródłowych oraz języka docelowego. Aplikacja będzie iteracyjnie prezentować dane, umożliwiając tłumaczenie wybranych fragmentów tekstu.

## Wymagania
1. **Interfejs Użytkownika:**
   - Implementacja graficznego interfejsu użytkownika (GUI) umożliwiającego łatwą obsługę narzędzia.
   - Hosting aplikacji na serwerze, z możliwością dostępu do niej przez przeglądarkę internetową.

2. **Wczytywanie danych:**
   - Implementacja mechanizmu wczytywania plików z danymi tekstowymi, z pierwszą wersją narzędzia obsługującą format .csv, z możliwością rozszerzenia do innych formatów w przyszłości.
   - Wykorzystanie biblioteki do obsługi plików CSV.

3. **Wybór danych do tłumaczenia** 
   - Użytkownik ma możliwość zaznaczania kolumn, które mają być tłumaczone.
   - Użytkownik może wybrać zakres rzędów do tłumaczenia oraz oznaczyć indeksy/zakresy rzędów, które mają być zignorowane.

4. **Wybór języków tłumaczenia:**
   - Zapewnienie użytkownikowi możliwości wyboru języków naturalnych początkowych i języka końcowego.
   - Możliwość automatycznego pobrania odpowiednich modeli tłumaczenia na potrzeby aplikacji.

5. **Tłumaczenie Tekstu:**
   - Implementacja mechanizmu iteracyjnego tłumaczenia poszczególnych rzędów danych.
   - Dla każdej wybranej kolumny pokazywana jest oryginalna wartość tej kolumny, rozpoznany język tekstu oraz zaproponowane tłumaczenie w oddzielnym, edytowalnym polu tekstowym.
   - Użytkownik ma możliwość zaakceptowania tłumaczenia, poprawy go lub zignorowania.
   - Jeśli język nie został rozpoznany, ,a to być zasygnalizowane.
   - Już przetłumaczone teskty nie są zmieniane.

6. **Obsługa Poprawek Użytkownika:**
   - Użytkownik powinien mieć możliwość edytowania tłumaczenia i jego zapisania. 

7. **Zapisywanie Wyników:**
   - Zapisywanie przetłumaczonych i zaakceptowanych rzędów danych do pliku.
   - Zapewnienie możliwości ściągnięcia nowego pliku z przetłumaczonymi i zaakceptowanymi rzędami.

8. **Zarządzanie procesem tłumaczenia:**
    - Implementacja mechanizmu pozwalającego użytkownikowi przerwać i wznowić proces tłumaczenia.
    - Wykorzystanie struktury danych do przechowywania stanu procesu tłumaczenia.

## Technologie i Narzędzia

- **Języki programowania**: `C++` i `Python`.
- **Biblioteki**: `wt` - backend API + generowanie szablonów frontendu, `HuggingFace` - modele tłumaczące.
- **Zarządzanie Zależnościami**: `poetry` dla Pythona i `conan` dla C++.
- **Zarządzanie Projektem**: `make` do budowania paczki, testowania i generacji dokumentacji.
- **Generacja Wiązań**: `pybind11` do tworzenia wiązań między Pythonem a C++.
- **Testy Jednostkowe**: `pytest` dla Pythona i `Catch2` dla C++.


Powyższa dokumentacja stanowi wstępny zarys projektu, który zostanie doprecyzowany w trakcie jego realizacji. Każdy z podpunktów będzie rozwijany o dodatkowe szczegóły techniczne i implementacyjne.