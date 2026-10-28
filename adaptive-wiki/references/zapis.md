# Zapis wiki i wejścia dla narzędzi

Ten dokument opisuje techniczny sposób udostępnienia instrukcji. Organizacja wiedzy
i treść procedur wynikają z projektu wiki.

## Jedna treść instrukcji

W nowym miejscu utrzymuj wspólne instrukcje startowe w `AGENTS.md`: rola wiki, sposób
wejścia do wiedzy, lokalne ustalenia i odesłania do pracy wymagającej szczegółów.
Pozostaw w nim to, czego sesja potrzebuje na początku. Procedury i dłuższe wskazówki
czyta się wtedy, gdy dotyczą bieżącego zadania.

Obok utwórz `CLAUDE.md` zawierający import:

```markdown
@AGENTS.md
```

Codex czyta `AGENTS.md`, Claude Code może wczytać tę samą treść przez import. Ten układ
działa także wtedy, gdy obecność nadrzędnego `CLAUDE.md` wyłącza automatyczne odnajdywanie
`AGENTS.md` przez Claude Code. Nie potrzeba kopii doktryny ani dowiązań systemu plików.

W istniejącej wiki zachowaj jej działające miejsce utrzymania instrukcji i połącz z nim
brakujące wejście. Nie nadpisuj już istniejącego `CLAUDE.md` samym importem ani nie twórz
drugiej doktryny obok pierwszej. Uwzględnij instrukcje nadrzędne i granicę katalogu wiki.

## Procedura raz, dwa wejścia

W nowej wiki zapisuj pełne lokalne procedury jako skille w `.agents/skills/<operacja>/SKILL.md`.
Codex odkrywa je tam bez osobnego pluginu. Każdy skill ma frontmatter `name` i `description`,
który jasno mówi, do jakiego zadania służy, oraz treść dopasowaną do tej wiki.

Claude Code udostępnia lokalne skille z `.claude/skills/`. Dla każdej operacji utwórz tam
krótkie wejście z nazwą, opisem i odsyłaczem do pełnej procedury. Przykład dla ingestu:

```markdown
---
name: ingest
description: Włącz wskazany materiał do wiedzy tej wiki.
---

Przeczytaj [lokalną procedurę ingest](../../../.agents/skills/ingest/SKILL.md)
i wykonaj ją dla bieżącego zamówienia. Ścieżka odsyłacza jest względna wobec tego pliku.
```

Nie umieszczaj drugiej wersji procesu w takim wejściu. `name` i opis mają odpowiadać tej
samej operacji w obu narzędziach. Pełna procedura odsyła do wspólnych lokalnych ustaleń
i potrzebnych zasobów; nie odsyła z powrotem do przejściówki.

Operator w katalogu wiki wywołuje `/ingest`, `/ask`, `/lint`, `/evolve`, `/export` w Claude Code
lub odpowiednio `$ingest`, `$ask`, `$lint`, `$evolve`, `$export` w Codexie. Jeśli istnieje
kolizja z wcześniej zdefiniowanym skillem, sprawdź faktyczne odkrywanie w danym środowisku
i wyjaśnij operatorowi wybór właściwej procedury. Nie usuwaj cudzych skilli.

Przy istniejącym innym układzie zachowaj tę samą zasadę: jedna utrzymywana procedura,
działające wejścia dla używanych narzędzi. Odesłanie tekstowe jest instrukcją dla modelu;
sprawdzenie, czy model je odczytał, wymaga rzeczywistej próby.

## Materiał i przenoszenie

Pliki należące do wiki łącz ścieżkami względnymi. Umiejscowienie źródeł zewnętrznych
wynika z ustaleń operatora; nie zaszywaj adresu jego maszyny w każdej procedurze.
Gdy przeniesiona wiki nie ma dostępu do źródła, ma ujawnić tę granicę, zamiast twierdzić,
że sprawdziła materiał. Eksport powinien zachować zrozumiałe wskazanie pochodzenia także
dla odbiorcy, który nie ma tych samych katalogów.

Źródłowe pliki instrukcji, takie jak `AGENTS.md` lub `CLAUDE.md` z badanego projektu,
nie mogą przypadkiem stać się instrukcjami tej wiki. Przechowaj ich kopię jako materiał
w formie niewczytywanej automatycznie przez narzędzie, zachowując informację o oryginale.
To dotyczy także przenoszonych konfiguracji i wykonywalnych skilli. Oryginał pozostaje nietknięty.

Nie dodawaj obowiązkowych hooków, usług, baz danych ani skryptów do utrzymania zwykłej wiki.
Narzędzie pomocnicze może wynikać z konkretnej funkcji zamówionej przez operatora.
Utworzenie wiki samo w sobie nie wymaga inicjowania Git, commitowania ani zmiany ustawień
użytkownika. Jeśli operator tego potrzebuje, jest to osobno uzgodniona część pracy.
