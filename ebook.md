# Dostarczanie rozwiązania zadania za pomocą GitHuba
## Stworzenie forka repozytorium
Jeśli chcemy dostarczyć rozwiązanie zadania, to w pierwszej kolejności powinniśmy stworzyć forka, czyli kopię repozytorium, do którego chcemy dostarczyć rozwiązanie. Możemy to zrobić klikając w przycisk `Fork` widoczny na stronie repozytorium.
![Tworzenie forka](img/fork.png)

Po kliknięciu w przycisk GitHub zapyta nas jak chcemy nazwać naszego forka. Domyślną nazwą forka jest nazwa oryginalnego repozytorium i taką też możemy pozostawić. Klikamy na zielony przycisk `Create fork`
![Wybór nazwy forka](img/fork_2.png)

## Wybranie odpowiedniej gałęzi
Po kliknięciu w przycisk zostaniemy automatycznie przeniesieni na stronę naszego forka.
Rozwiązania zadań powinniśmy umieszczać na odpowiednich gałęziach (*ang. branch*).
Gałąź możemy wybrać klikając na nazwę aktualnej gałęzi w lewym górnym rogu (w naszym przypadku `main`), a następnie klikamy w nazwę gałęzi, na którą chcemy się przełączyć.
W naszym przykładzie chcemy dostarczyć rozwiązanie zadania `fibonacci`, dlatego wybieramy gałąź o tej samej nazwie.
![Wybór brancha](img/branch_selection.png)

Po przejściu na odpowiednią gałąź, przechodzimy do folderu z zadaniem domowym (w przypadku `homework/fibonacci`).
Następnie wybieramy plik, w którym znajduje się implementacja zadania (`fibonacci.hpp`).
![Wybór folderu z zadaniem domowym](img/directory_selection.png)
![Wybór pliku z implementcją](img/file_selection.png)

## Stworzenie naszej implementacji
Jeśli chcemy wprowadzić zmiany w pliku, klikamy na przycisk z ikonką ołówka.
![Wejście w tryb edycji](img/edit.png)

Naszym oczom ukaże się edytor, w którym możemy wprowadzić nasze rozwiązanie zadania.
Przykładowo zmienimy wartości zwracane przez obie funkcje na 1 zamiast 0 (co oczywiście nie jest poprawnym rozwiązaniem 😉). Dobrze jest też usunąć komentarze zaczynające się od `TODO:` jeśli zrobiliśmy implementację rozwiązania.
![Edycja pliku](img/edited_file.png)

## Dodanie commita z wprowadzonymi zmianami
Jeśli uważamy, że nasza implementacja jest gotowa, to pod edytorem mamy możliwość utworzenia commita z naszymi zmianami.
Możemy tam podać nazwę commita (np. My implementation).
Możemy też wybrać czy zmiany chcemy dodać do gałęzi, na której się znajdujemy, czy do nowo utworzonej.
Jeśli pracujemy na swoim forku, to wybieramy tę pierwszą opcję. Klikamy na przycisk `Commit changes`.
![Tworzenie commita](img/commit.png)

## Utworzenie Pull Requesta
Po dodaniu commita implementacja znajduje się już na naszym forku.
Jeśli chcemy ją dostarczyć do pierwotnego repozytorium, klikamy na zakładkę `Code`.
Możemy zauważyć baner informujący nas, że na gałęzi `fibonacci` znajduje się 1 zmiana więcej niż na pierwotnym repozytorium.
Klikamy na przycisk `Contribute`, a następnie na `Open pull request`.
![Contribute](img/contribute.png)
![Tworzenie pull requesta](img/open_pr.png)

Następnie możemy nadać naszemu pull requestowi nazwę (np. My implementation).
![Otworzenie PRa](img/pr_opening.png)

Poniżej możemy zobaczyć jakie zmiany chcemy zgłosić w pull requestcie.
![Zmiany PR](img/pr_changes.png)

Jeśli wszystko się zgadza, możemy kliknąć na zielony przycisk `Create pull request`.

Czasem w zakładce `Code` nie pojawia się informacja o nowych zmianach, ponieważ po pewnym czasie od wprowadzenia zmian znika ona automatycznie.
Jeśli tak się stanie, możemy stworzyć pull requesta w inny sposób.
W tym celu wybieramy zakładkę `Pull requests`.
![Zakładka Pull requests](img/pull_request.png)

Następnie klikamy na zielony przycisk `New pull request`.
Upewniamy się, że zostały wybrane odpowiednie repozytoria oraz gałęzie.
W naszym przypadku powinny być wybrane:
* base repository: `coders-school/cpp-fundamentals`, branch: `fibonacci`
* head repository: nasze repozytorium oraz branch `fibonacci`
![Wybór branchów](img/branch_pr_select.png)

Jeśli wszystko jest w porządku, klikamy na przycisk `Create pull request`.
Następnie możemy kontynuować tworzenie pull requesta tak jak w poprzednim przypadku.

## Wyniki testów
Po zgłoszeniu pull requesta testy sprawdzające poprawność naszej implementacji zostaną uruchomione automatycznie.
Stan wykonywania testów możemy obserwować w dolnej części strony.
![Oczekiwanie na wynik testów](img/pr_created.png)

W przypadku naszej implementacji testy oczywiście nie przejdą, o czym zostaniemy poinformowani symbolem ❌.
![Wynik testów](img/test_failed.png)

Jeśli chcemy zobaczyć szczegółowe informacje na temat wyników poszczególnych testów, możemy kliknąć na przycisk `Details`.
![Przycisk Details](img/test_details.png)

W zakładce `Run tests` możemy zobaczyć dlaczego testy nie zadziałały.
![Podsumowanie wyników](img/test_summary.png)
