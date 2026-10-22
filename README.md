# MigraPRO

**Przeprowadzka sklepu internetowego do IdoSell — 1:1, bez przepisywania ręcznie.**

MigraPRO to samoobsługowa aplikacja (SaaS), która przenosi sklep z platform
**Shoper**, **PrestaShop** i **WooCommerce** do **IdoSell** przez oficjalne API.
Podajesz dostęp do starego sklepu i klucz API IdoSell, zaznaczasz, co przenieść,
a MigraPRO robi resztę.

## Co przenosi

- Kategorie, producenci, parametry
- Produkty: nazwy, opisy, ceny, VAT, zdjęcia, warianty, stany, EAN/SKU, waga
- Klienci z adresami (hasła ustawiają na nowo — tego nie da się przenieść z żadnej platformy)
- Historia zamówień
- SEO: meta tytuły i opisy oraz przekierowania 301 ze starych adresów
- Wszystko inne, co przyjmuje API IdoSell — poza szablonem graficznym

## Jak to działa

1. Łączysz stary sklep i IdoSell (test połączenia od razu).
2. MigraPRO skanuje sklep i pokazuje, ile czego jest do przeniesienia.
3. Wybierasz zakres i ustawiasz mapowania (VAT, statusy zamówień, waluty).
4. Migracja próbna na kilku produktach — sprawdzasz efekt w IdoSell.
5. Pełna migracja w tle, ze wznawianiem po błędzie i bez dublowania danych.
6. Raport oraz dociągnięcie nowych zamówień i klientów tuż przed przełączeniem domeny.

## Status

Projekt w budowie (start: październik 2026).

## Aktualizacje

- **2026-10-17** — start projektu, plan aplikacji.
- **2026-10-17** — rozpoznanie API IdoSell, Shoper, PrestaShop i WooCommerce: co da się przenieść automatycznie; przekierowania 301 jako plik do importu w panelu IdoSell.
- **2026-10-17** — pierwsza wersja panelu (połączenie starego sklepu i IdoSell, policzenie danych do przeniesienia) działa na własnym serwerze pod adresem https://migrapro.pl.
- **2026-10-17** — działa migracja produktów Shoper → IdoSell: ustawienia w formie tabeli (parowanie pól, kreator nazwy, kolejność zdjęć, reguły, filtry), drzewo menu, parametry, migracja próbna i pełna z paskiem postępu i raportem CSV, częściowa aktualizacja istniejących produktów.
- **2026-10-18** — nowy moduł „Logistyka produktów”: przegląd i filtrowanie ustawień wysyłki, zwrotów i wymiarów wszystkich produktów sklepu IdoSell, szablony i zmiany hurtowe (zmieniają tylko wybrane pola).
- **2026-10-18** — Logistyka: wyszukiwanie i zmiana grupowa po kurierach darmowej dostawy, formach płatności i usłudze Smile; filtry po parametrach produktu, menu sklepu, wymiarach (od–do) i liście kodów; podgląd „było → będzie” przed zapisem w IdoSell; wybór kolumn i sortowanie.
- **2026-10-18** — Logistyka: pakiety (Darmowy, Start, Biznes, Pro) i automaty — reguła „produkty z filtra mają ustawienia z szablonu” sprawdzana co noc, z raportem albo automatyczną poprawką; filtr osobno dla każdego menu sklepu; czytelniejsza tabela.
- **2026-10-20** — warianty jako osobne karty łączone w grupy IdoSell (każda karta zachowuje swoją nazwę, zdjęcia, opisy i cenę); nowe narzędzie „Grupowanie towarów”: propozycje grup dla całego sklepu IdoSell, podgląd, zapis w tle, raport i cofnięcie jednym przyciskiem; wykrywanie i naprawa złych grup (karty rozbite na kilka grup, obce karty w grupie), filtr po słowach; ustawienia wszystkich grup naraz (wyświetlanie, pola wspólne) z cofnięciem.
- **2026-10-21** — naprawa stanów magazynowych przy migracji i uzupełnianie stanów ze starego sklepu; nazwy wartości w grupach (lista wyboru na karcie produktu); nowe narzędzie „Parametry z nazwy i opisu”: reguły (fraza w nazwie, opisie lub kategorii → parametr), podgląd, zapis w tle i cofnięcie.
- **2026-10-21** — Logistyka: „sprzedawaj po” (detal i hurt), dostępność ze stanu albo ręcznie z wyborem magazynów (M0, M1, M2…), cofanie każdej zmiany grupowej (także stanów przy zmianie trybu dostępności).
- **2026-10-21** — nowe narzędzie „Załączniki hurtowo”: jeden albo kilka plików (instrukcja, deklaracja zgodności, karta produktu — rodzaje dokumentów pod GPSR) na setkach i tysiącach kart IdoSell naraz; wgranie pliku do 95 MB albo link, wybór kart filtrem, podgląd z szacowanym czasem, kolejka w tle z ponawianiem, raport CSV i cofnięcie; instrukcja obsługi w zakładce.
- **2026-10-22** — nowe narzędzie „Opisy sklepów”: lista kart, które w wybranym sklepie i języku mają własną nazwę albo opis zamiast domyślnych (z porównaniem tekstów i oznaczeniem pustych opisów), lista ID do skopiowania albo pobrania (.txt, CSV) i instrukcja przywrócenia opisów domyślnych Edycją grupową IdoSell.

---
Kod aplikacji jest prywatny. To repozytorium zawiera wyłącznie informacje o projekcie.
