# Ainything_wiki

Skopiuj **cały ten folder** do nowego folderu projektu. Uruchom w korzeniu projektu
Claude Code i napisz:

> Start. Przeczytaj Ainything_wiki/START.md.

AI omówi z Tobą zastosowanie, utworzy główną wiki i nazwanego zarządcę oraz zainstaluje
u niego proces tworzenia kolejnych wiki. Nie potrzebujesz `--plugin-dir`, globalnej
instalacji ani ręcznych wywołań pluginu. Sama paczka nie instaluje programu Claude Code.

Po konfiguracji pracuj w wiki lub folderze zarządcy. Gotowy system może tworzyć kolejnych
agentów także po odłożeniu tej paczki. Kopie instalatora rozwijają się lokalnie;
aktualizacja paczki nie zmienia istniejących systemów.

[Instrukcja operatora](INSTRUKCJA.html) działa lokalnie, bez internetu.

## Pochodzenie

Wydanie 2026-10-28. Adaptive Wiki pochodzi z paczki adaptive-wiki 0.1.0: zachowano proces
projektowania i trzy materiały references. W tym wariancie dodano wywołanie lokalne
w ramach zamówienia, usunięto disable-model-invocation i nie przeniesiono polityki
allow_implicit_invocation: false. Nie jest to załadowany plugin ani zmiana jego globalnej
instalacji. Metoda mikroagentowa uwzględnia doświadczenia DiBi i prób z 26–28 października.

Pierwszy sprawdzany harness: Claude Code. Pliki AGENTS.md oraz wspólne procedury
umożliwiają adaptację do innych narzędzi; nie oznacza to potwierdzenia ich identycznej pracy.
