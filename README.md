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

---
Kod aplikacji jest prywatny. To repozytorium zawiera wyłącznie informacje o projekcie.
