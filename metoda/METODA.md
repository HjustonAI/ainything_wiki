# Składanie i rozwijanie repozytorium mikroagentowego

Pracujesz z inżynierem AI, który chce prowadzić przedsięwzięcie przy pomocy wiki
i wyspecjalizowanych agentów. Twoim zadaniem jest zrozumieć jego pracę, zaproponować
najprostszy wystarczający układ i pozostawić materiały, z których kolejna sesja potrafi
korzystać bez tej rozmowy. Do tworzenia wiki wykorzystaj dołączony lokalny proces **Adaptive Wiki**
([skill](../adaptive-wiki/SKILL.md)). Zachowaj znaczenie jego operacji.

## Zacznij od pracy człowieka

Prześledź konkretną sytuację: co człowiek przynosi, jaką pracę chce wykonać, czego potrzebuje
do decyzji i co otrzymuje na końcu. Wykorzystaj wcześniejsze odpowiedzi. Rozpoznaj, co jest
wiedzą wspólną, co wymaga specjalizacji, a co jest jednorazowym zadaniem obecnej sesji.
Nie twórz agenta tylko dlatego, że umiesz nazwać rolę.

Pokaż proponowany przebieg i jego konsekwencje dla operatora. Porównaj sensowne alternatywy,
jeśli różnią się pracą lub odpowiedzialnością. Otwarte wybory wpływające na projekt omów
przed zależną realizacją. Rutynowe kroki wykonuj w przyjętym zakresie. Milczenie nie jest
wyborem. Zmiana priorytetu nie musi oznaczać ponownego projektowania wszystkiego.

## Złóż całość z potrzebnych części

Podstawą repozytorium jest główna `wiki/` oraz osobny folder nazwanego zarządcy.
Oba miejsca utwórz procesem Adaptive Wiki: pierwsze do wiedzy o przedsięwzięciu, drugie do wiedzy
o samym systemie i prowadzenia jego rozwoju. Główna wiki może początkowo nie mieć źródeł;
ma być gotowa je przyjąć, bez fikcyjnych haseł wypełniających pustą strukturę.
Zarządca od początku zna przyjęty układ i sposób dalszej pracy. Nazwę dobierz z operatorem.
Mikroagentów wykonujących zadania dodawaj, gdy są potrzebni; samo założenie systemu
nie wymaga wymyślania pierwszej specjalizacji.

W korzeniu pozostaw czytelne wejście: cel przedsięwzięcia, mapę miejsc, wspólne ustalenia
i sposób uruchomienia właściwego agenta. Korzeń kieruje do właściwej sesji; sesję
zarządcy uruchamia się w jego folderze. Instrukcje wspólne mogą ładować się także
w podkatalogach. Nie nadawaj w nich wszystkim sesjom tożsamości zarządcy.
Wspólne ustalenia nadal obowiązują w swoim zakresie. Zmienne fakty przedsięwzięcia
pozostaw w wiki, a w wejściu wskaż, gdzie je znaleźć.

Zaprojektuj obie wiki przez dołączony proces Adaptive Wiki, w uzgodnionych miejscach.
Sesja prowadząca czyta jego SKILL.md i wskazane materiały; może też zlecić wykonanie
wydzielonej sesji, przekazując rolę, folder docelowy, uzgodnienia i zakres zapisu.
Nie wymagaj wywołania zewnętrznego pluginu ani dodatkowej komendy człowieka.
Kontekst przyszłego mikroagenta wybieraj z już powstałej głównej wiki.

W folderze zarządcy zainstaluj kompletny lokalny wiki-install zgodnie z START.md.
Kolejni agenci powstają przez ten lokalny skill. Jego treść i materiały nie zależą od
paczki startowej ani ścieżek maszyny autora. Nie odtwarzaj procesu projektowania wiki
z pamięci i nie utrzymuj drugiej jego wersji w nowy-agent.

Zachowaj znaczenie `ingest`, `ask`, `lint`, `evolve` i `export`. `Evolve` może rozbudowywać
wiki w warsztat i dodawać potrzebne skille lub sposoby pracy. Nie daje samo z siebie
upoważnienia do przebudowy sąsiednich agentów. Zakres całości prowadzi zarządzający.

Nazwy i liczba plików wynikają z użycia. Wykorzystuj istniejące mechanizmy harnessu.
Nie dokładaj obowiązkowych formularzy, limitów długości, rejestrów wersji instrukcji,
punktacji, bramek, hooków ani własnej platformy orkiestracji. Narzędzie powstaje wtedy,
gdy wykazana potrzeba uzasadnia koszt jego używania i utrzymania.

## Przygotuj zarządcę do dalszej pracy

Zarządca jest wiki o systemie rozszerzoną o procesy jego tworzenia i zmieniania.
Zaprojektuj te rozszerzenia według [prowadzenia zarządcy](ZARZADCA.md), a potem zapisz
samodzielne lokalne skille. Powstały system nie powinien wymagać tej metody w każdej sesji.
Workflow jest treścią skilla; nie utrzymuj drugiego opisu tych samych kroków obok.
Podstawowe wejścia to `nowy-agent` i `przeglad`; rozwój własnego miejsca pozostaje w `evolve`.
Zmianę obejmującą inne moduły prowadzi zarządca według uzgodnionego zakresu.

Wiedza zarządcy przechowuje uzasadnienia architektury, aktualne powiązania oraz przydatne
doświadczenia. Mechanikę harnessu opisuj ze źródłem, datą i rozróżnieniem dokumentacji,
próby oraz hipotezy. Sięgaj po odpowiedni temat, nie całą bazę na starcie. Jeśli dostępne
są doświadczenia DiBi, wybierz lekcje przydatne temu systemowi, zachowując pochodzenie
i odróżniając ograniczenia prototypu od zasad nowego miejsca. Nie kopiuj jego całej bazy.

W nowych miejscach stosuj sposób wejścia Adaptive Wiki: treść w `AGENTS.md`, import
`@AGENTS.md` w `CLAUDE.md`. Pełne procedury w `.agents/skills/`, krótkie wejścia Claude
w `.claude/skills/`. Procedury zarządcy pozostają w jego folderze; nie umieszczaj ich
w korzeniu tylko po to, by były wszędzie widoczne. Nie zakładaj, że otwarcie pliku
innego agenta przełącza tożsamość sesji. Przeczytanie instrukcji odbiorcy pozwala go
zrozumieć; wykonawca nadal realizuje swoje zlecenie. Sprawdź to w używanym harnessie.

## Daj agentowi wystarczający własny kontekst

Przy dodawaniu agenta ustal, co ma robić, z jakiej wiedzy korzysta, jaki wynik oddaje
i gdzie kończy się jego odpowiedzialność. Przejdź przez prawdziwe przykładowe zadanie.
Zbadaj dostępne narzędzia i ograniczenia zamiast obiecywać możliwości na podstawie nazwy roli.

Umieść jego instrukcje i potrzebne materiały w folderze, w którym można rozpocząć osobną
sesję. Wybierz z głównej wiki wystarczający lokalny kontekst. Zachowaj pochodzenie, czas
i istotne niepewności; wyciąg nie jest nowym źródłem potwierdzenia. **Aktualność i dobór
kontekstu należą do człowieka — inżyniera AI korzystającego z rozwiązania.** Agent przygotowuje
lub odświeża wyciąg na jego prośbę. Pracuje na dostarczonym kontekście;
nie dodawaj obowiązku porównywania go z wiki przed każdym zadaniem. Zauważony brak lub
sprzeczność sygnalizuje w związku z wykonywaną pracą. Nie buduj nadzorcy świeżości.

Rozróżnij lokalnie to, co pomaga działać w danym przedsięwzięciu, własne rzemiosło agenta
i stan konkretnego zadania. Nie każde rozróżnienie wymaga osobnego katalogu. Każdy nowy
mikroagent ma mini-wiki utworzoną lokalnym wiki-install, gotową do `ingest`, `ask`, `lint`, `evolve`
i `export`. Zwykle sam folder agenta może być tą wiki, rozszerzoną o warsztat;
nie twórz dodatkowego zagnieżdżenia `wiki/` bez potrzeby. Paczkę z głównej wiki przyjmij
jako źródło lokalnej wiedzy. Nie utrzymuj obok drugiej, konkurencyjnej bazy kontekstu.
Brak wiedzy w głównej wiki nie blokuje zaprojektowania roli: nazwij, czego nie da się
jeszcze wykonać i jakie materiały trzeba dostarczyć. Nie deklaruj gotowości do pracy,
która wymaga brakujących faktów lub narzędzi.

Zmiennych ustaleń nie zamieniaj w trwałe zasady roli. Na przykład „nie wymyślaj liczby
uczestników” pozostaje użyteczne po potwierdzeniu tej liczby, a „nie podawaj liczby
uczestników” może wtedy blokować pracę. Aktualne dane i ich znaczenie trzymaj w kontekście.

Instrukcje mają pomagać znaleźć potrzebny materiał, nie ładować cały folder do każdej
rozmowy. Wymień istotne zależności od innych miejsc, narzędzi i dostępu. Nie wpisuj sekretów
ani ścieżki jednej maszyny jako uniwersalnej zasady.

## Współpraca i export

Agent rozpoznaje potrzebną pomoc po zadaniu i dostępnych współpracownikach. W małym
repozytorium mapa w korzeniu może wystarczyć do ich znalezienia. Instrukcja agenta opisuje,
jakiej pomocy potrzebuje; dostępność tej pomocy wynika z otoczenia, do którego został wpięty.
Chwilowego braku redaktora nie utrwalaj jako stałej cechy warsztatu. Brak współpracownika
oznacza wykonanie sensownego dostępnego zakresu i jasne wskazanie brakującej zdolności;
zastępstwo nie staje się automatycznie równoważnym wynikiem specjalisty.

Przekazując zadanie, podaj potrzebny rezultat, materiały, kontekst i ograniczenia.
Odbiorca pracuje według własnych instrukcji. Samo zlecenie nie upoważnia go do zmiany
zasad innych agentów. Wynik wraca do zlecającego z podstawą i ograniczeniami.

Dobierz sposób do harnessu i pracy: brief oraz osobna sesja mogą wystarczyć. Jeśli
bezpośrednie delegowanie istotnie pomaga, użyj dostępnego mechanizmu i sprawdź jego
rzeczywiste zachowanie. Subagent harnessu nie jest automatycznie samodzielną sesją
w folderze mikroagenta. Sprawdź, jakie instrukcje, narzędzia, katalog i historię otrzymał.
Nie twórz dodatkowego protokołu komunikacji bez potrzeby.

`export/` mieści materiały wystawiane na prośbę operatora do zewnętrznego użycia: wynik,
brief, wiedzę lub propozycję. Nie wymaga własnego formatu paczki ani zapisu po każdym zadaniu.
Odbiorca ma rozumieć, co dostał, na czym to się opiera
i co pozostaje nieustalone. Sam zapis eksportu niczego nie wysyła ani nie zmienia u odbiorcy.
Operator wybiera, czy i gdzie wykorzysta materiał. Może przenieść plik do `raw` głównej wiki
albo wiki innego agenta (lokalna nazwa miejsca na źródła może być inna) i zlecić jej `ingest`.
Może też podać plan zmian zarządzającemu. Nie buduj samoczynnego obiegu export → raw → ingest.
Zlecenie utworzenia agenta może obejmować tę drogę: zarządca deleguje przygotowanie paczki,
przekazuje ją do źródeł nowego agenta i zleca ingest w uzgodnionym zakresie. Operator nie musi
ręcznie kopiować każdego pliku. To wykonanie konkretnego zamówienia, nie stała synchronizacja.
Eksportów nie trzeba umieszczać w Git; wybrany materiał można wersjonować, jeśli operator
widzi w tym wartość. Gdy eksporty pozostają lokalne, odsyłacz do takiego pliku nie zapewni
odbiorcy jego treści — do przekazania dołącz potrzebną treść lub odpowiednie pliki.
Przyjęcie zachowuje pochodzenie; propozycja agenta nie staje się decyzją człowieka.
Eksport może też zawierać obserwacje i wyniki wykonanej pracy. Oceniaj je według podstawy
i ograniczeń, zamiast uznawać każdy materiał od agenta za propozycję.

## Przenieś bez ukrytych zależności

Preferuj folder gotowy do skopiowania z własnymi instrukcjami i wystarczającym kontekstem.
Przy projektowaniu pokaż koszt tej gotowości: czasem wymaga lokalnej kopii zasobu,
a czasem rozsądniej pozostawić jawną zależność i ograniczoną pracę bez niej.
Zależności wewnątrz folderu łącz względnie. Wskazanie pochodzenia może prowadzić do
niedostępnego źródła, ale brak źródła trzeba odróżnić od awarii niezbędnego wejścia do pracy.

Przy przeniesieniu rozpatrz, które materiały wolno przenieść, co jest potrzebne odbiorcy
i czy kontekst nadal odpowiada jego przedsięwzięciu. Nowy korzeń może mieć inne zasady.
Ustal z inżynierem istotne różnice. Nie przenoś automatycznie uprawnień, sekretów,
historii sesji ani kontekstu poprzedniego zlecenia jako faktów o nowym.

Zacznij porównanie od zwykłych folderów i niezależnej kopii. Git może zachować historię
lub ułatwić późniejszą wymianę ulepszeń. `Subtree` rozważ przy regularnej wymianie zmian,
`submodule` przy potrzebie osobnego projektu z przypiętą wersją. Nie wymagaj synchronizacji.
Poprawka po scaleniu nadal wymaga oceny, czy pasuje do miejscowego zastosowania.

## Rozwijaj po rzeczywistej pracy

Agent doskonali siebie w zakresie zlecenia operatora. Wnioski dotyczące innych przekazuje
jako propozycje. Zarządzający rozpatruje konsekwencje dla całości. Zmiana wewnętrznych
zasad innego agenta wymaga zgody nadzorującego inżyniera; delegacja zadania jej nie zastępuje.
Zlecenie operatora może już zawierać tę zgodę — nie wymagaj wtedy osobnego potwierdzenia.
Lokalna instrukcja jest materiałem do rozwijania na jego zlecenie, nie zakazem, którego
operator nie może zmienić. Odróżniaj ocenę planu od polecenia jego wykonania.

Rozwijając strukturę, przejrzyj dotknięte instrukcje, wejścia, odsyłacze i zależności.
Wiedzę utrzymuj w jej właściwym miejscu; aktualny opis ma odpowiadać temu, co działa.
Historyczny zapis nadal opisuje stan i decyzję z tamtego czasu. Decyzje człowieka zachowuj
osobno od rekomendacji modelu. Odróżniaj trwałe ustalenie od zakresu pojedynczego zlecenia:
„nie twórz teraz agenta” nie zakazuje jego późniejszego dodania. Zapis stanu i wyborów ma umożliwiać wznowienie pracy,
nie tworzyć obowiązku dokumentowania każdego kroku.

Dobierz Git do przedsięwzięcia. Zamówienie założenia systemu obejmuje lokalne repozytorium:
jeśli Git nie został jeszcze zainicjowany w docelowym folderze, utwórz go na gałęzi roboczej
wybranej dla projektu (domyślnie praca). Zastanego repo ani gałęzi nie przestawiaj.
Nie wykonuj commitów, publikacji ani zdalnej konfiguracji bez ich zamówienia.
Sprawdź rozstrzygnięty korzeń, aby nie uznać nadrzędnego repo za Git nowego projektu.
 Rozpatrz instrukcje, wiedzę, źródła, wartościowe wyniki,
duże pliki i koszt ich odtworzenia. Sekrety, pamięć podręczna i ustawienia jednej maszyny
potrzebują innego traktowania niż współdzielone instrukcje. Sprawdź znaczenie reguł
ignorowania na rzeczywistych ścieżkach. Na przykład `**/export/*` pomija także skill
o nazwie export; wyłączenie wyników powinno wskazywać ich folder, np. `/export/*`
w `.gitignore` danego modułu. Lokalne reguły przenoszą się z nim. Ignorowanie pliku przez
Git nie blokuje jego odczytu. Markdown opisuje reguły, lecz nie egzekwuje granicy dostępu.

## Oddaj użyteczne miejsce

Pokaż operatorowi powstałe pliki i sposób rozpoczęcia pracy. Sprawdź nową sesję z jej
normalnym kontekstem, użyteczny wynik, przeniesienie i wybrany sposób współpracy.
Dobieraj próby do niewiadomych; nie zamieniaj ich w framework zgodności z szablonem.
Odróżniaj przeczytaną instrukcję, ręczne przekazanie i wykonane delegowanie.

Po doświadczeniu uprość metodę i lokalne instrukcje. Jeżeli sesja wymaga wiedzy z rozmowy
założycielskiej, popraw brakujący materiał, a nie tylko podpowiedz jej odpowiedź.
Opisz jawnie ograniczenia i to, czego nie sprawdzono. Odbiór należy do operatora.
