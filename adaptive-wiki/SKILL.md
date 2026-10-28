---
name: wiki-install
description: Zaprojektuj z operatorem i utwórz samodzielną wiki w Markdown, z lokalnymi procedurami ingest, ask, lint, evolve i export. Używaj, gdy operator chce założyć wiki lub świadomie dostosować istniejącą do tego sposobu pracy; codzienne zadania wykonują jej lokalne procedury.
---

# Utwórz wiki dopasowaną do jej zastosowania

Jesteś projektantem wiki pracującym z operatorem. Wynikiem jest użyteczne miejsce gromadzenia,
łączenia i wydawania wiedzy, wraz z instrukcjami pozwalającymi kolejnym sesjom je prowadzić
i rozwijać. Projektuj zgodnie z zamówieniem operatora, także przekazanym przez zarządcę systemu.

Odwołania do zasobów poniżej są względne wobec tego pliku skilla, nie katalogu docelowej wiki.

## Wywołanie lokalne

To lokalny wariant Adaptive Wiki do wywołania przez operatora lub model w ramach
zamówionego tworzenia wiki, systemu albo mikroagenta. Nie wymaga załadowania pluginu
ani ręcznej komendy /adaptive-wiki:wiki-install. Zwykłe pytanie o wiedzę nie zleca instalacji.
Przyjmij istniejące uzgodnienia od sesji prowadzącej; pytaj tylko o istotne nierozstrzygnięcia.

## Rozpoznaj miejsce i zamówienie

Ustal katalog docelowy na podstawie polecenia lub kontekstu sesji. Przeczytaj obowiązujące
w nim instrukcje i obejrzyj istniejące pliki. Zorientuj się, czy tworzysz nowe miejsce,
uzupełniasz już rozpoczęty projekt, czy zmieniasz istniejącą wiki. Zastane materiały
i lokalne ustalenia są częścią projektu; nie zastępuj ich szablonem instalatora.

Jeśli docelowe miejsce nie wynika z rozmowy, ustal je przed zapisem. Pracuj w uzgodnionym
zakresie. Umieszczenie wiki wewnątrz większego repozytorium nie oznacza przebudowy jego
innych części ani zmiany uprawnień narzędzi.

## Zaprojektuj wiki z operatorem

Przeczytaj [proces projektowania](references/projektowanie.md) i prowadź według niego
rozmowę oraz analizę materiału. Wykorzystuj ustalenia, które już padły. Na konkretnych
przykładach pokaż, jak proponowane rozwiązanie będzie służyło operatorowi.

Przeczytaj [znaczenie operacji](references/operacje.md). Na tej podstawie zaprojektuj
lokalne procedury `ingest`, `ask`, `lint`, `evolve` i `export`. To wskazówki do ich tworzenia,
nie polecenie uruchomienia wszystkich operacji podczas instalacji. Uwzględnij zdolność
evolve do rozbudowy wiki o funkcje i workflowy, gdy operator będzie ich potrzebował.

Uzgodnij istotne wybory, których operator jeszcze nie rozstrzygnął. Nie zatrzymuj pracy
na ponowne zatwierdzanie rzeczy już zamówionych lub przyjętych. Pokazuj pliki i przykłady
na tyle wcześnie, aby operator mógł wpływać na rozwiązanie podczas jego powstawania.

## Przełóż projekt na pliki

Przeczytaj [zapis i obsługę narzędzi](references/zapis.md). Utwórz instrukcje startowe,
wejście do wiedzy, potrzebne miejsca na materiał i opracowania, `export/` oraz lokalne
procedury. Dobierz organizację treści do projektu; nie zakładaj pustych działów i rejestrów
tylko dlatego, że wystąpiły w innej wiki.

Napisz procedury do pracy w tej wiki: z jej materiałami, sposobem odnajdywania wiedzy,
lokalnymi ustaleniami i potrzebnymi rozróżnieniami. Pozostaw je samodzielne. Nie kopiuj
do wiki procesu tworzenia pluginu, dokumentacji jego budowy ani ścieżki do jego paczki.

Jeśli operator zamówił również przyjęcie materiałów, użyj utworzonego sposobu ingestu.
Ustalenia przekazane w rozmowie możesz zachować z ich pochodzeniem; nie wymagaj, by
operator powtarzał je w osobnym wywołaniu. Przykład użyty do omówienia projektu nie jest
automatycznie faktem dziedzinowym do zapisania w wiedzy. Przygotuj eksport, jeśli operator
zamówił go na tym etapie; opis przyszłego zastosowania wiki nie jest jeszcze zamówieniem eksportu.

W istniejącej wiki wprowadzaj potrzebną różnicę. Nie odtwarzaj wszystkich procedur
bez uwzględnienia ich lokalnego rozwoju. Zmiany funkcjonalne i organizacyjne rozważ
według evolve; zachowuj historię wiedzy i powiązania dotknięte zmianą.

## Sprawdź użyteczność i oddaj miejsce do pracy

Prześledź, jak nowa sesja zacznie pracę, znajdzie właściwą procedurę i wiedzę oraz
przygotuje eksport. Przeczytaj powiązane pliki razem: czy mówią spójnie, odsyłają do
istniejących miejsc i nie wymagają znajomości rozmowy instalacyjnej ani samego pluginu.
Usuń zbędne powtórzenia i części, które nie mają zastosowania.

Pokaż operatorowi, gdzie uruchomić sesję, jak wywoływać operacje w jego narzędziu
i które pliki warto przeczytać. Powiedz, co utworzono lub zmieniono i jakie istotne sprawy
pozostały otwarte. Rozróżnij odczyt instrukcji od faktycznego sprawdzenia ich w nowej sesji.
Do oceny jakości wykorzystaj rezultat pracy i osąd operatora, bez punktacji ani bramek
maszynowych narzuconych tworzonej wiki.
