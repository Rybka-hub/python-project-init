---
name: python-project-init
description: "Przygotuj strukturę i .gitignore nowego projektu Python. Używaj przy inicjalizacji aplikacji lub jednorazowego skryptu, nie przy zwykłym rozwijaniu istniejącego projektu."
metadata:
  version: "1.0.0"
---

# Praca agentowa nad aplikacjami Python

Przygotuj szkielet nowego projektu Python zgodnie ze standardem użytkownika. Ten skill obejmuje etap inicjalizacji; dalszy zakres pracy wynika ze zlecenia.

## Przygotowanie projektu

- Przeczytaj [Python.md](Python.md) i zastosuj wskazaną strukturę oraz `.gitignore`. Dopuszczone uproszczenia dobierz do rodzaju projektu.
- Ustal katalog docelowy na podstawie zlecenia. Przed zapisem sprawdź jego zawartość i istniejące repozytorium; zachowaj wcześniejsze pliki i unikaj zagnieżdżania repozytoriów.
- Utwórz potrzebne katalogi i początkowe pliki. Pliki oraz środowiska generowane przygotuj właściwymi narzędziami, bez wymyślonych wersji zależności.
- Zainicjalizuj lokalny Git, jeśli katalog nie należy do repozytorium. Nie twórz commita ani nie publikuj projektu bez polecenia użytkownika.
- Sprawdź, czy dane wejściowe, wyniki i lokalne środowisko są ignorowane, a bezpieczne wzory konfiguracji oraz kod pozostają dostępne do wersjonowania.

## Dokumentacja

Opis przeznaczenia i wymaganej zawartości dokumentów `.md` znajduje się w globalnym `AGENTS.md`. Korzystaj z tych zasad, jeśli są dostępne w obowiązujących instrukcjach.

Jeśli brakuje takich opisów, przeczytaj część „Przeznaczenie dokumentów projektu” w dołączonym [Agent.md](Agent.md), do nagłówka „Nowa aplikacja”. To materiał pomocniczy dla osób korzystających ze skilla bez tych globalnych zasad.

Uzupełnij dokumentację stanem wynikającym z utworzonego projektu. Nie instaluj ani nie podmieniaj globalnych instrukcji automatycznie. Projektowy `AGENTS.md` i `CLAUDE.md` przygotuj zgodnie z `Python.md`.

## Zakończenie

Podaj katalog utworzonego projektu, istotne elementy szkieletu i sposób rozpoczęcia pracy. Wskaż niewykonane elementy, jeśli środowisko lub dostęp do narzędzi uniemożliwił ich przygotowanie.
