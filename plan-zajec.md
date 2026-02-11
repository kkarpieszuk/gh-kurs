# Github dla początkujących 1 godzina

## Uczestnicy

- Konrad Karpieszuk - prowadzący...
- Michał Majerski vel "Fin"
- Alex Szram
- Adrian Dudek (inicjal D.)

## Założenia wstępne

*   Zakładamy, że git już jest zainstalowany lokalnie (wydaj polecenie `git -v` by sprawdzić, jeśli nie ma zainstaluj)

*   Mamy już konto na githubie (bezpłatne)

*   Mamy dodany klucz ssh w [https://github.com/settings/keys](https://github.com/settings/keys) jeśli nie, to [tutaj jest instrukcja](chatgpt.com/share/698af0a2-5a44-800a-a766-df32876b1d6c)


## Szybkie wprowadzenie

* jak sklonować repozytorium
```
git clone [adres]
```
* jak zrobić zmiany w kodzie i wyslac je na zdalne repozytorium

```
git add -A # lub git add nazwa_pliku.rozszerze
git commit -m "nazwa zmian"
git push
```

* jak pobrać aktualną wersję

```
git pull
```

* sprawdzanie historii
* przełączenie na historyczną wersję

## Co się nauczymy


### współpraca w kilka osób na tym samym repozytorium

*   jak dodać współpracowników w Github

*   dzielenie kodu na gałęzie by nikt nie nadpisywał zmian kogoś innego

*   scalanie zmian od kilku programistów

```
git pull --rebase
```

*   rozwiązywanie konfliktów przy scalaniu

- podgladamy zmiany w plikach ktore maja konflikty
```
git status # pokaze oba zmienione: nazwa_pliku...
```

- otwieramy taki plik do edycji i szukamy wystapien `<<<<<`
- rozwiazujemy edytujac pliki
- `git add nazwa_pliku` dla kazdego pliku, ktory juz ma rozwiazany konflikt
- na koniec `git rebase --continue` (zapyta nas o nowa nazwe commitu)
- i oczywiscie git push

*   praca kilku programistów na jednej gałęzi

*   co się stanie gdy utworzymy gałąź ze złej?

## odkładanie na półkę

jezeli jeszcze nie zattwierdzilem zmian w repo, to moge odlozyc je na polke

```
git stash
```

i potem zrobiic cokolwiek i potem znow sciagamy z polki

```
git stash pop
```

## git bissect

[opis](https://dev.wpzlecenia.pl/2019/08/co-zrobic-gdy-twoj-kod-dzialal-ale-przestal-poznajcie-git-bisect/)

## bonus jeśli starczy czasu (do wyboru lub punkt po punkcie póki starczy czasu):

*   założymy puste repozytorium na Githubie i sklonujemy je lokalnie

*   dodatkowy wariant: lokalny kod jaki mamy na dysku zmienimy w lokalne repozytorium i wyślemy na Github

1.  jak znaleźć tę jedną zmianę sprzed miesięcy, która przeoczona teraz okazuje się wadzić

2.  jak znaleźć tego, kto napisał ten felerny kod

3.  tworzenie szablonów repozytoriów - przydatne gdy często zaczynamy projekty tak samo