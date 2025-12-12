# AGH Analiza Trendów

## Jak zrobić fork repozytorium w GitHub

### Krok 1: Zaloguj się do GitHub
Przejdź na stronę [GitHub.com](https://github.com) i zaloguj się do swojego konta.

### Krok 2: Znajdź repozytorium
Przejdź do repozytorium, które chcesz sforować. W tym przypadku jest to:
```
https://github.com/marcinkieruzel/agh-analiza-trendow
```

### Krok 3: Kliknij przycisk "Fork"
W prawym górnym rogu strony repozytorium znajdziesz przycisk **"Fork"**. Kliknij go.

### Krok 4: Wybierz swoje konto
GitHub zapyta Cię, gdzie chcesz utworzyć fork. Wybierz swoje konto użytkownika.

### Krok 5: Poczekaj na utworzenie forka
GitHub automatycznie skopiuje repozytorium do Twojego konta. Proces może potrwać kilka sekund.

### Krok 6: Sklonuj swój fork lokalnie
Po utworzeniu forka, możesz sklonować go na swój komputer:

```bash
git clone https://github.com/TWOJA-NAZWA-UŻYTKOWNIKA/agh-analiza-trendow.git
cd agh-analiza-trendow
```

Zastąp `TWOJA-NAZWA-UŻYTKOWNIKA` swoją rzeczywistą nazwą użytkownika GitHub.

### Krok 7: Skonfiguruj upstream (opcjonalne)
Aby móc synchronizować swój fork z oryginalnym repozytorium, dodaj upstream:

```bash
git remote add upstream https://github.com/marcinkieruzel/agh-analiza-trendow.git
```

### Krok 8: Sprawdź konfigurację
Sprawdź czy wszystko jest poprawnie skonfigurowane:

```bash
git remote -v
```

Powinieneś zobaczyć:
- `origin` - Twój fork
- `upstream` - Oryginalne repozytorium

## Synchronizacja z oryginalnym repozytorium

Aby zaktualizować swój fork najnowszymi zmianami z oryginalnego repozytorium:

```bash
# Pobierz najnowsze zmiany z upstream
git fetch upstream

# Przełącz się na branch main
git checkout main

# Zmerguj zmiany z upstream/main
git merge upstream/main

# Wypchnij zmiany do swojego forka
git push origin main
```

## Tworzenie Pull Request

1. Wprowadź zmiany w swoim forku
2. Wypchnij zmiany do swojego repozytorium na GitHub
3. Przejdź na stronę swojego forka na GitHub
4. Kliknij przycisk **"New pull request"**
5. Opisz swoje zmiany i kliknij **"Create pull request"**

## Jak utworzyć GitHub Pages

GitHub Pages pozwala na darmowe hostowanie statycznych stron internetowych bezpośrednio z repozytorium GitHub.

### Krok 1: Przejdź do ustawień repozytorium
1. Otwórz swoje repozytorium na GitHub
2. Kliknij zakładkę **"Settings"** (po prawej stronie nad kodem)

### Krok 2: Znajdź sekcję Pages
1. W lewym menu przewiń w dół i kliknij **"Pages"**

### Krok 3: Wybierz źródło
1. W sekcji **"Source"** wybierz **"Deploy from a branch"**
2. W polu **"Branch"** wybierz **"main"** (lub **"master"** jeśli tak nazywa się Twój główny branch)
3. W polu **"Folder"** zostaw **"/ (root)"** jeśli Twoje pliki HTML są w głównym folderze
4. Kliknij **"Save"**

### Krok 4: Poczekaj na deployment
GitHub automatycznie zbuduje i wdroży Twoją stronę. Proces może potrwać kilka minut.

### Krok 5: Sprawdź adres strony
Po zakończeniu procesu, GitHub wyświetli adres Twojej strony:
```
https://TWOJA-NAZWA-UŻYTKOWNIKA.github.io/agh-analiza-trendow
```

### Video tutorial
Szczegółowy tutorial wideo znajdziesz tutaj:
[![GitHub Pages Tutorial](https://img.youtube.com/vi/d4kd0gPlfhw/0.jpg)](https://www.youtube.com/watch?v=d4kd0gPlfhw)

### Dodatkowe wskazówki
- Twój główny plik powinien nazywać się `index.html`
- Zmiany w repozytorium są automatycznie odzwierciedlane na stronie (może potrwać kilka minut)
- Możesz używać własnej domeny - instrukcje w ustawieniach Pages
- GitHub Pages obsługuje Jekyll do generowania statycznych stron

## Przydatne linki

- [Oficjalna dokumentacja GitHub o forkach](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks)
- [Guide po Pull Requestach](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- [Dokumentacja GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)