# Task 1

### Subtask 1

8/10 punktów

### Subtask 3

Cześć, mam na imię Ola. Zdecydowałam się na udział w challengu, ponieważ już od jakiegoś czasu myślę o przebranżowieniu się na testera, a to wyzwanie z pewnością mi w tym pomoże. Liczę, że wzięcie udziału w tym przedsiewzięciu doda mi dodatkowej motywacji i inspiracji do samodzielnej pracy, a ukończenie go zaowocuje fajnym projektem, którym będę mogła pochwalić się w portfolio. 

### Subtask 4

Testowana aplikacja jest platformą skautingową dla łowców talentów piłki nożnej. Znajduje się tu baza danych zawodników oraz informacje o ich statystykach (wygrane, przegrane), ich pozycji, drużynie. 
W aplikacji są następujące funkcjonalności:
- dodawanie zawodnika 
- dodawanie rozegranych meczy 
- tworzenie raportu z meczu 
- przeglądanie listy wszystkich graczy
- wylogowanie
- zmiana jezyka na angielski

#### Dodawanie gracza

Po wybraniu opcji "dodaj gracza" rozwija się formularz, w którym do wypełnienia są dane takie jak: imię i nazwisko zawodnika, telefon, waga, wzrost, data urodzenia, dominująca noga, klub, poziom rozgrywek, głowna oraz alternatywna pozycja, województwo osiągnięcia. 

#### Dodawanie meczu

Po zapisaniu gracza istnieje możliwość dodania rozegranych przez niego meczy. Ponownie wyświetla się formularz do wpisania danych takich jak: drużyna zawodnika oraz przeciwna, zdobyte oraz stracone gole, data, wybór mecz wyjazdowy/domowy, kolor koszulki, liga, czas gry, numer, recenzja. 


W moim odczuciu funkcjonalności oraz interfejs nie do końca są intuicyjne. Na stronie głównej wyświetlone są ala przyciski "Ilość graczy", "Ilość meczy", "Ilość raportów", "Ilość akcji", w które niestety nie można kliknąć, by zobaczyć informacje o graczach, meczach itd. 
W pierwszej chwili niezrozumiały był też raport, a dokładnie edycja danych statystycznych. Nie wiadomo było w jaki sposób dodać informacje o podaniach, dośrodkowaniach itd. Dopiero po dłuższej pracy ze stroną dostrzegłam, że w sekcji dodawania meczu jest opcja "rozpocznij mecz" gdzie można wybrać te wszystkie informacje klikając na planszy boiska. 
Dodatkowo po wpisaniu danych gracza w odpowiednim formularzu i zapisaniu wyświetla się komunikat, że gracz został dodany, ale formularz z wpisanymi danymi cały czas pozostaje. Według mnie lepiej byłoby, gdyby ten formularz po dodaniu gracza się zamykał i wyświetlone zostały np. informacje o nim, ale już bez możliwości ich zmiany. Gdyby ktoś chciał edytować, powinien być do tego stosowny przycisk, po którego naciśnięciu strona powinna ponownie przenieść się do formularza. 
Jest też parę rzeczy, które należałoby poprawić:
1) Podczas przewijania kolejnych stron w liście graczy zauważyłam, że jeden z nich miał na imię "Imieeeeee...e", co spowodowało brak możliwości przewijania na kolejną stronę(by to zrobić, należało przesunąć widok w prawo, co było uciążliwe). Dlatego też uważam, że w formularzu do wprowadzania danych zaowdnika powinny być ograniczenia w ilości możliwych wpisanych znaków, np. max 30 na imię oraz max. 30 na nazwisko. 
2) W formularzu w miejscu do wpisania imienia, nazwiska nie powinno być możliwości wpisania liczy. Podobnie w miejscu do wpisania telefonu, formularz nie powinien pozwolić na wpisanie tekstu- powinien wyświetlić komunikat, że format jest niepoprawny i należy wpisać tylko cyfry. Korzystnym również byłoby, gdyby formularz przepuszczał tylko właściwą ilośc wpisanych cyfr (telefon komórkowy jest 9 cyfrowy).
3) Kolejną sprawą jest eksport danych do Excela, co jest z pewnością przydatną funkcją, jednak niestety eksport jest niepoprawny. Dane eksportują się do 1 formuły i jest to bardzo nieczytelne.
4) Po wylogowaniu się ze strony, nie ma możliwości ponownego zalogowania. Po wpisaniu danych do logowania (tych samych co podczas pierwszego logowania) wyświetlony został komunikat, że nazwa użytkownika lub hasło są niepoprawne. Aby ponownie zalogować się na stronę, należało na nowo wejść w podany w instrukcji link. 
5) W formularzu dodawnia meczu oraz gracza dopuszczny został rok 0003 :) W takiej sytuacji powinien być wyświetlony komunikat o nieprawidłowej dacie. 
6) W opcji "rozpocznij mecz" powyżej boiska piłkarskiego są ikonki np. play, pauza. Po najechaniu na nie kursorem myszy powinien być wyświetlonby tekst z informacją jaką ten przycisk ma funkcję.

Jeśli chodzi o zalety strony, to fajnie, że można ustawić kolejność graczy alfabetycznie po imieniu, nazwisku czy po ocenie lub liczbie raportów, co z pewnościa ułatwi wyszukiwanie i wybór gracza. Fajną funkcjonalnością jest także "lupka" do wyszukiwania gracza np. po imieniu lub nazwisku oraz filtracja np. wieku. Test wprowadzania daty urodzenia gracza przeszedł pozytywnie- formularz nie pozwolił na wpisanie błędnej daty, np. 29 luty lub 31 kwietnia.
