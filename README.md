# Praca agentowa nad aplikacjami Python

Skill **`python-project-init`** przygotowuje uporządkowany szkielet nowego projektu Python. Jego celem jest spójna struktura plików i `.gitignore`, które pozwalają rozpocząć dalszą pracę z agentem.

## Co robi

- Tworzy strukturę projektu z kodem w `src/`, miejscem na testy i dokumentacją.
- Tworzy wymagany `requirements.txt` zamiast `requirements.lock.txt` i `requirements-dev.lock.txt`.
- Wydziela `data/input/` na materiały użytkownika i `data/output/` na wyniki.
- Przygotowuje `.gitignore` dla środowiska Pythona, sekretów, danych i plików generowanych.
- Uwzględnia prostszy układ dla jednorazowego skryptu.

Skill realizuje inicjalizację. Funkcje aplikacji, jej architektura i integracje wynikają z osobnego zakresu zlecenia. Nie narzuca frameworka ani dostawcy LLM.

## Co zawiera zestaw

| Plik | Zawartość |
| --- | --- |
| [SKILL.md](SKILL.md) | Punkt wejścia: nazwa, zakres i instrukcje wykonania skilla. |
| [Python.md](Python.md) | Ustalona struktura projektu i wzór `.gitignore`. |
| [Agent.md](Agent.md) | Pomocniczy wzór zasad pracy i opisów dokumentacji. |
| [CHANGELOG.md](CHANGELOG.md) | Historia opublikowanych wersji i ich zmian. |
| `README.md` | Cel zestawu, instalacja i przykłady użycia. |

Nie kopiuj samego `SKILL.md` — korzysta on z pozostałych materiałów w folderze.

## Wersjonowanie

Numer zainstalowanej wersji znajduje się w `metadata.version` w [SKILL.md](SKILL.md). Każde wydanie ma tag Git `vX.Y.Z` i odpowiadające mu [wydanie na GitHubie](https://github.com/Rybka-hub/python-project-init/releases). Historię zmian opisuje [CHANGELOG.md](CHANGELOG.md).

Stosujemy SemVer:

- `PATCH`, np. `1.0.1`: poprawki i doprecyzowania bez zmiany przyjętego standardu.
- `MINOR`, np. `1.1.0`: rozszerzenia zgodne z dotychczasowym sposobem użycia.
- `MAJOR`, np. `2.0.0`: zmiany zasad lub struktury wymagające dostosowania dotychczasowego sposobu użycia.

Oba skille są wersjonowane niezależnie. Opublikowanego tagu nie zmieniamy; kolejne poprawki otrzymują nowy numer. Gałąź `main` może zawierać zmiany jeszcze niewydane — do instalacji wybieraj konkretne wydanie. Aktualizacja skilla nie modyfikuje wcześniej utworzonych projektów.

## Instalacja w Codexie

1. Pobierz wybraną wersję ze strony [wydań](https://github.com/Rybka-hub/python-project-init/releases) przez „Source code (zip)” i rozpakuj archiwum. Możesz też użyć całego folderu z lokalnego zestawu.
2. Jeśli Twoja instalacja Codexa wczytuje własne skille z `~/.codex/skills/`, skopiuj cały folder do `~/.codex/skills/python-project-init/`. `~` oznacza katalog użytkownika; na Windows jest to `%USERPROFILE%`, czyli docelowo `%USERPROFILE%\.codex\skills\python-project-init\`.
3. Sprawdź, czy `SKILL.md` znajduje się bezpośrednio w folderze `python-project-init/`, bez dodatkowego zagnieżdżenia.
4. Jeśli skill nie pojawi się na liście, uruchom Codexa ponownie.

Aktualna [oficjalna dokumentacja skilli Codexa](https://learn.chatgpt.com/docs/build-skills) wskazuje `~/.agents/skills/` jako lokalizację użytkownika. Jeśli Twoja instalacja korzysta z tego układu, użyj `~/.agents/skills/python-project-init/`. Wybierz katalog, z którego Codex faktycznie wczytuje Twoje skille; nie kopiuj tego samego skilla do obu lokalizacji.

Instalację ograniczoną do jednego projektu wykonasz, umieszczając ten sam folder w `.agents/skills/python-project-init/` w jego katalogu.

## Użycie

Po instalacji wywołaj skill w Codexie, np.:

```text
$python-project-init Przygotuj nowy projekt Python do przetwarzania dokumentów w katalogu wskazanym w tej rozmowie. Na razie utwórz tylko szkielet.
```

```text
$python-project-init Przygotuj jednorazowy skrypt Python do zmiany nazw plików. Zastosuj uproszczony układ i uzasadnij wybór.
```

Podaj cel projektu i katalog docelowy. Skill jest przeznaczony do nowych projektów; zwykłe poprawki w istniejącej aplikacji nie wymagają jego ponownego uruchamiania.

## Globalne instrukcje i dokumentacja

Opisy dokumentów projektu są utrzymywane w globalnym `AGENTS.md`. Jeśli użytkownik ich nie ma, skill korzysta z odpowiedniej części dołączonego `Agent.md`, bez powielania opisów w swoim punkcie wejścia.

Instalacja skilla nie instaluje globalnych zasad. Opcjonalnie przejrzyj `Agent.md`, dopasuj go do własnych preferencji i włącz wybrane zasady do `~/.codex/AGENTS.md`. Zachowaj istniejące instrukcje. Domyślną lokalizację opisuje [dokumentacja AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).
