Quizr
=====

Aplikacja pozwalaj�ca na rozwi�zywanie quiz�w. 

To jest tylko szkielet aplikaji, jak� studenci musz� rozwin�� w ramach �wicze�
podczas podyplomowych studi�w "Programowanie aplikacji internetowych" na Wy�szej
Szkole Nauk Humanistycznych i Dziennikarstwa w Poznaniu.


Instalacja
----------

Wejd� na github do [repozytorium projektu](https://github.com/sargo/quizr)
i stw�rz forka.

Nast�pnie przygotuj virtualenv i sklonuj Twojego forka repozytorium:

```
source /opt/python/2.7/bin/virtualenvwrapper.sh
mkvirtualenv --python=/opt/python/2.7/bin/python quizr
cdvirtualenv
git clone git@github.com:username/quizr.git
cd quizr
pip install -r requirements.txt
```

U�ycie
------

Przygotowanie do pracy:

```
workon quizr
cdvirtualenv
cd quizr
```

Uruchomienie aplikacji:

```
python quizr
```

Uruchomienie test�w jednostkowych:

```
python quizr_tests
```

Tre�� zadania
-------------

Nale�y stworzy� aplikacj�, dzi�ki kt�rej u�ytkownik b�dzie m�g� wzi�� udzia� 
w quizie. U�ytkownik, po wej�ciu na stron� g��wn� powinien zobaczy� kr�tki opis
zasad quizu, pole do wpisania swojego pseudonimu oraz przycisk �Start�. Po
rozpocz�ciu, aplikacja losuje jedno z pyta� i pokazuje je u�ytkownikowi wraz z
mo�liwymi odpowiedziami. Po udzieleniu odpowiedzi przez u�ytkownika, losowane
jest kolejne pytanie (nie s� brane pod uwag� pytania kt�re wcze�niej pad�y). Po 
dzieleniu odpowiedzi na 5 pytanie, u�ytkownikowi pokazywany jest ekran
podzi�kowania, wraz z ilo�ci� zdobytych punkt�w wraz z maksymaln� warto�ci�
oraz jako procent maksymalnej warto�ci - przyk�ad 12 / 15 (80%).

Punktacja:
 * 3 punkty za poprawn� odpowied� w czasie kr�tszym ni� 10 sekund od wy�wietlenia pytania
 * 2 punkty za poprawn� odpowied� w pomi�dzy 10 a 30 sekund� od wy�wietlenia pytania
 * 1 punkt za poprawn� odpowied� w czasie powy�ej 30 sekund

Pytania mog� mie� 2 do 5 mo�liwych odpowiedzi, ale tylko jedna jest prawid�owa.
Pytania do quizu aplikacja pobiera� b�dzie z pliku w formacie CSV.
Przyk�adowy plik znajduje si� w folderze `data`.

Struktura CSV:
 * Pierwsza kolumna - pytanie
 * Ostatnia kolumna - prawid�owa odpowied� (warto�� A, B, C, D lub E)
 * Pozosta�e kolumny - mo�liwe odpowiedzi
 
Aplikacja powinna posiada� testy jednostkowe.



