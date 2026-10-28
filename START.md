# Ainything_wiki — rozpocznij lub wznów tworzenie systemu

Operator kopiuje tę paczkę do folderu projektu, uruchamia tam AI i pisze:
„Start. Przeczytaj Ainything_wiki/START.md”. Poprowadź całość w jednej rozmowie.
Paczka jest zapleczem tworzenia; nie jest główną wiki ani zarządcą powstającego systemu.
Nie wymaga instalacji globalnej, ładowania pluginu ani kolejnych komend operatora.

## Najpierw rozpoznaj, gdzie jesteśmy

Korzeniem docelowym jest folder wskazany przez operatora — zwykle rodzic tej paczki.
Sprawdź katalog sesji, rzeczywisty korzeń i obowiązujące instrukcje. Obejrzyj zastane
pliki oraz stan lokalnego Gita. Nie nadpisuj materiałów ani cudzych instrukcji szablonem.
Przed przeniesieniem sprawdź pełne ścieżki źródła i celu oraz czy cel jest wolny.
Wszystkie własne pliki, również pomocnicze, pozostają w uzgodnionym projekcie.

Sprawdź KONFIGURACJA.md w korzeniu, a jeśli go nie ma — istniejącą mapę systemu
i stan w indeksie nazwanego zarządcy. Rozróżnij:

- **Nowe miejsce:** zacznij od pracy, którą system ma ułatwiać. Samo „start” nie mówi,
  czy chodzi o wydarzenie, codzienność czy dział firmy. Zapytaj o cel i wykorzystaj
  dostarczone materiały. Nie wymyślaj przedsięwzięcia ani agentów.
- **Praca rozpoczęta:** sprawdź ustalenia i pliki, po czym kontynuuj od brakującego
  kroku. Nie powtarzaj wywiadu, instalacji ani przyjęcia tego samego źródła.
- **Gotowy system:** krótko wskaż, gdzie pracować z wiedzą i gdzie zamawiać agentów.
  Nie przeinstalowuj go. Nowe polecenie może zamawiać konkretną zmianę.

## Poprowadź projekt i wykonanie

Przeczytaj [metodę](metoda/METODA.md). Rozmowa ma prowadzić od rzeczywistej pracy do
najprostszego użytecznego układu. Pokaż konsekwencje ważnych wyborów, nazwij założenia,
odróżniaj decyzje operatora od własnych rekomendacji. Nie wymagaj wypełnienia formularza
ani ponownej zgody na już zamówione kroki. Gdy brakuje istotnej odpowiedzi, zapytaj;
w tym czasie wykonuj tylko niezależną pracę.

W KONFIGURACJA.md zachowaj cel, uzgodnienia, wykonane części i następny krok. To krótki
stan do wznowienia, nie nowy framework ani rejestr każdej czynności. Gdy istniejący
projekt ma już odpowiedni zapis, połącz się z nim zamiast utrzymywać konkurencyjny stan.
Natywny goal jest możliwością tylko wtedy, gdy operator go jawnie zleci i harness go
obsługuje. Brak tej funkcji nie zatrzymuje rozmowy ani konfiguracji.

Zbuduj główną wiki gotową na wiedzę oraz osobny, nazwany z operatorem folder zarządcy.
Obie wiki tworzy dołączony [Adaptive Wiki](adaptive-wiki/SKILL.md) wraz z jego
materiałami. Przeczytaj i wykonaj ten proces lub przekaż go wydzielonej sesji z pełnym
zamówieniem. Użyj ustaleń z rozmowy; nie zaczynaj drugiego wywiadu o tym samym.
To lokalny wariant wywoływany przez model, nie zastrzeżony instalator osobnego pluginu.

Rozwiń zarządcę według [procesów zarządcy](metoda/ZARZADCA.md): własna wiedza o układzie,
lokalne nowy-agent i przeglad, evolve także do zamówionych zmian całości. Instrukcje
korzenia zawierają mapę i wspólne zasady, nie tożsamość zarządcy dla wszystkich sesji.
Zainicjuj lokalny Git, jeśli go nie ma, i dobierz reguły ignorowania do projektu.
Nie twórz commitów, zdalnego repo ani zmian globalnych ustawień bez osobnego zamówienia.

## Zainstaluj zdolność tworzenia kolejnych wiki

W folderze zarządcy umieść pełną kopię `adaptive-wiki/` z tej paczki jako
`.agents/skills/wiki-install/`: SKILL.md i całe references/. Zachowaj względne odsyłacze
wewnątrz tego skilla. W `.claude/skills/wiki-install/SKILL.md` utwórz krótkie wejście
z name i description oraz odesłaniem do `../../../.agents/skills/wiki-install/SKILL.md`.
Nie twórz drugiej kopii procedury w wejściu Claude. Ten wariant pozwala na wywołanie
przez model; nie dodawaj disable-model-invocation: true ani allow_implicit_invocation: false.
Nie nadawaj mu rozszerzonych uprawnień; zwykłe zasady harnessu nadal obowiązują.

Jeśli docelowy wiki-install już istnieje, rozpoznaj jego przeznaczenie i lokalne zmiany.
Nie zastępuj go po cichu kopią paczki. Przy zgodnym, kompletnym procesie wykorzystaj
istniejący; rzeczywisty konflikt rozstrzygnij z operatorem. Nie usuwaj cudzych skilli.

Lokalny nowy-agent ma korzystać z tego zainstalowanego procesu. Nie odsyła operatora
do ręcznego wywołania pluginu i nie zależy od Ainything_wiki. Wiedzę oraz warsztat
mikroagenta rozwija jego sesja w zamówionym zakresie. Wybór i aktualność kontekstu
pozostają odpowiedzialnością operatora; proces może wykonać zamówione przekazanie.

## Domknij i zostaw samowystarczalny system

Sprawdź zgodność wejść i ścieżek oraz użyteczność kolejnej sesji. Odróżnij przeczytanie
plików od rzeczywistej próby działania. Nie dodawaj uniwersalnych testów zgodności,
limitów ani bramek. Główna wiki może pozostać pusta, a mikroagenci powstaną według potrzeb.

Gdy zarządca już działa, przenieś KONFIGURACJA.md do jego dokumentacji zmian i wskaż
zapis w indeksie. Zachowaj jeden bieżący stan; zapis nie może wyglądać jak nowa decyzja
operatora. W mapie korzenia wskaż folder zarządcy i jego indeks, aby kolejne „start”
odnalazło stan po przeniesieniu. Jeśli istnieje wcześniejsza notatka, nie nadpisuj jej.

Zostaw lokalną wiedzę i procesy potrzebne do dalszego rozwoju, bez obowiązkowego czytania
tej paczki, jej metody lub instrukcji autora. Geneza może być wspomniana, lecz nie jako
niezbędne wejście do pracy. Pierwotne materiały paczki pozostają niezmienione; projektowe
ustalenia trafiają do systemu. Paczkę operator może później odłożyć. Nie kasuj jej sam.

Pokaż, gdzie uruchomić sesję wiki i zarządcy, jak przyjąć materiał oraz zamówić agenta.
Nazwij istotne ograniczenia i nierozstrzygnięcia. Konfiguracja kończy się użyteczną
podstawą zaakceptowaną przez operatora, nie samym utworzeniem folderów.
