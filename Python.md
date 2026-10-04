# Praca agentowa nad aplikacjami Python

## 1. Struktura nowego projektu Python

Dla nowego projektu Python utwórz poniższą strukturę. `nazwa_pakietu` zastąp nazwą właściwą dla aplikacji.

- Jednorazowy skrypt może mieć prostszy układ. Uzasadnij uproszczenie zamiast automatycznie tworzyć cały szkielet aplikacji.

```text
projekt/
├── .git/                       # Tworzony przez Git, nie ręcznie
├── .venv/                      # Lokalne środowisko Pythona, poza Git
├── AGENTS.md                   # Może być pusty
├── CLAUDE.md                   # Zawiera wyłącznie: @AGENTS.md
├── PLANS.md
├── PROJECT_CONTEXT.md
├── HANDOFF.md
├── README.md
├── README_SHORT.md
├── ARCHITECTURE.md
├── DECISIONS.md
├── .gitignore
├── .env.example                # Bezpieczny wzór zmiennych środowiskowych
├── .python-version             # Wersja Pythona dla projektu
├── pyproject.toml              # Konfiguracja projektu i zależności
├── requirements.lock.txt       # Dokładne wersje zależności aplikacji
├── requirements-dev.lock.txt   # Dokładne wersje aplikacji i narzędzi do pracy
├── data/
│   ├── input/                  # Materiały dostarczane przez użytkownika
│   └── output/                 # Wygenerowane wyniki
├── src/
│   └── nazwa_pakietu/
│       ├── __init__.py
│       ├── __main__.py         # Punkt wejścia: python -m nazwa_pakietu
│       ├── main.py             # Główny punkt startowy aplikacji
│       └── settings.py         # Konfiguracja aplikacji
└── tests/
    ├── conftest.py             # Wspólne fixtures, jeśli są potrzebne
    └── test_*.py               # Rzeczywiste pliki testowe
```

`test_*.py` oznacza wzorzec nazw plików, nie dosłowną nazwę. `conftest.py` dodaj, gdy potrzebne są wspólne fixtures. Nazwy plików blokady zależności dostosuj, jeśli projekt korzysta z narzędzia używającego innej blokady.

Pliki dokumentacji uzupełnij zwięzłą treścią dopasowaną do tworzonego projektu.

Opis przeznaczenia i wymaganej zawartości plików dokumentacyjnych `.md` znajduje się w globalnym `AGENTS.md`.

### Dane wejściowe i wyniki

- Stosuj nazwy `data/input/` i `data/output/`, małymi literami.
- `input/` zawiera materiały użytkownika, np. dokumenty, obrazy i assety; `output/` zawiera wygenerowane raporty, pliki i inne rezultaty.
- Utwórz oba katalogi i ignoruj je w Git w całości.
- Kod, prompty i zasoby aplikacji przechowuj poza tymi katalogami. Bezpieczne dane testowe mogą znajdować się w `tests/fixtures/`.

### Elementy dodawane według potrzeb

```text
config/                        # Ustawienia bez sekretów
scripts/                       # Skrypty pomocnicze
docs/                          # Dodatkowa dokumentacja
tests/fixtures/                # Bezpieczne dane testowe
tests/integration/             # Testy integracyjne
runtime/                       # Lokalny stan aplikacji, poza Git
.env                           # Lokalne ustawienia i sekrety, poza Git
```

## 2. `.gitignore`

### Domyślna zawartość

```gitignore
# Lokalne środowiska
.venv/
venv/

# Sekrety i lokalne pliki środowiskowe
.env
.env.*
!.env.example
!.env.*.example
/secrets/

# Pliki generowane przez Pythona i narzędzia
__pycache__/
*.py[cod]
.pytest_cache/
.mypy_cache/
.ruff_cache/
.hypothesis/
.tox/
.nox/
build/
dist/
*.egg-info/

# Raporty pokrycia testami
.coverage
.coverage.*
htmlcov/
coverage.xml
coverage.json

# Logi i pamięć podręczna
*.log
*.log.*
logs/
.cache/
/cache/
/tmp/
/temp/

# Prywatne dane i lokalny stan aplikacji
/data/input/
/data/output/
/runtime/

# Lokalne pliki edytorów
.idea/
.vscode/
*.swp
*.swo
*~

# Osobiste ustawienia Claude Code w projekcie
CLAUDE.local.md
.claude/settings.local.json

# Pliki systemu operacyjnego
.DS_Store
Thumbs.db
Desktop.ini
```
