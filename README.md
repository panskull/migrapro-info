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
- **2026-10-20** — warianty jako osobne karty łączone w grupy IdoSell (każda karta zachowuje swoją nazwę, zdjęcia, opisy i cenę); nowe narzędzie „Grupowanie towarów”: propozycje grup dla całego sklepu IdoSell, podgląd, zapis w tle, raport i cofnięcie jednym przyciskiem.

---
Kod aplikacji jest prywatny. To repozytorium zawiera wyłącznie informacje o projekcie.
