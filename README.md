# Task 6

## Subtask 1


## Subtask 2

14/15 pkt

# Task 5 

## Subtask 1 (Podstawy SQL)

Poniżej przedtawiono podstawowe komendy SQL

  * **SELECT** -is used to select data from a database.
  
        SELECT column1, column2, ...
        FROM table_name; 
  
  * **WHERE**- is used to filter records.
  
        SELECT column1, column2, ...
        FROM table_name
        WHERE condition; 
* **AND, OR, NOT**
	
	The WHERE clause can be combined with AND, OR, and NOT operators.
	
	The AND and OR operators are used to filter records based on more than one condition:

    The AND operator displays a record if all the conditions separated by AND are TRUE.
    The OR operator displays a record if any of the conditions separated by OR is TRUE.
    The NOT operator displays a record if the condition(s) is NOT TRUE.
 
 * **ORDER BY**- is used to sort the result-set in ascending or descending order.

        SELECT column1, column2, ...
        FROM table_name
        ORDER BY column1, column2, ... ASC|DESC; 
        
  * **INSERT INTO**- is used to insert new records in a table.

        INSERT INTO table_name (column1, column2, column3, ...)
        VALUES (value1, value2, value3, ...); 
	
  * **BETWEEN**- selects values within a given range.
  
        SELECT column_name(s)
        FROM table_name
        WHERE column_name BETWEEN value1 AND value2; 
  
  * **IN Operator**- allows to specify multiple values in a WHERE clause.
  		
		SELECT column_name(s)
		FROM table_name
		WHERE column_name IN (value1, value2, ...); 
		
* **LIKE**- is used in a WHERE clause to search for a specified pattern in a column.

		SELECT column1, column2, ...
		FROM table_name
		WHERE columnN LIKE pattern; 

* **NULL**

		SELECT column_names
		FROM table_name
		WHERE column_name IS NULL; 

## Subtask 3

**1. Wyświetl tabelę actors w kolejności alfabetycznej sortując po kolumnie surname.**

    SELECT* FROM actors
    ORDER BY surnamer;

![1](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/c51c95d7-4b66-40e9-b3f2-a8b5bdba39ab)

**2. Wyświetl film, który powstał w 2019 roku.**

    SELECT* FROM movies
    WHERE year_of_production=2019;

![2](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/aaf61a9e-54a9-49ff-bf24-fcfb34814d83)

**3. Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.**

    SELECT* FROM movies
    WHERE year_of_production BETWEEN 1900 AND 1999;

![3](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/ca14b42b-9f99-4cc5-9790-d9c2dc522ed6)

**4. Wyświetl JEDYNIE tytuł i cenę filmów, które kosztują poniżej 7$**

    SELECT title
	        ,price
    FROM movies
    WHERE price<=7
    
![4](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/1ea4ecd0-d520-4591-8dcb-6024e5b9a82a)

**5. Użyj operatora logicznego AND, aby wyświetlić aktorów o actor_id pomiędzy 4-7 (4 i 7 powinny się wyświetlać). NIE UŻYWAJ operatora BETWEEN**

	SELECT*FROM actors
	WHERE actor_id>3 AND actor_id<8
	
![5](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/0c85e38c-bad5-4969-b4e5-b988e12c5830)

**6. Wyświetl klientów o id 2,4,6 wykorzystaj do tego warunek logiczny.**

	SELECT*FROM customer
	customer_id=2 OR customer_id=4 OR customer_id=6

![6](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/81e87091-3318-4ca8-a7b9-fc59fc8227dd)

**7. Wyświetl klientów o id 1,3,5 wykorzystaj do tego operator IN.**

	SELECT*FROM customers
	WHERE customer_id IN ('1', '3', '5');
	
![7](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/0f68cc6f-0c92-4dfc-bd58-15d505e03dac)
	
**8. Wyświetl dane wszystkich osób z tabeli ‘actors’, których imię zaczyna się od ciągu “An”.**

	SELECT * FROM actors
	WHERE name LIKE 'An%';
	
![8](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/51d46e49-0dc2-4ae2-a6ee-144809fa071c)

**9. Wyświetl dane klienta, który nie ma podanego adresu email.**

	SELECT * FROM Customers
	WHERE email IS NULL;
	
![9](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/a758c442-56c5-4beb-b6e4-1b2e64494e76)

**10. Wyświetl wszystkie filmy, których cena wynosi powyżej 9$ oraz ich ID mieści się pomiędzy 2 i 8 movie_id.**

	SELECT * FROM movies
	WHERE price>8 AND movie_id BETWEEN 2 AND 8;
	
![10](https://github.com/olawydmuch/challenge_portfolio_olaw/assets/131545880/280fa9e9-17e2-4012-9c06-057af6cf6e61)

# Task 4

## Subtask 1(Utworzenie formatki do zgłaszania błędów systemu)

https://docs.google.com/spreadsheets/d/1WBr9Xo1XxDcdA_ZOh1VSphqnukiDetgTTx60npSo8ZA/edit?usp=share_link

## Subtask 2 (Testowanie eksploracyjne i raportowanie błędów)

https://docs.google.com/spreadsheets/d/1i28ax2TFhAKJHSJEqkT3xm_xIemu4t17nmkXsiB7mzU/edit?usp=share_link

## Subtask 3 (Do czego służy aplikacja OLX?)

1. Aplikacja OLX jest portalem ogłoszeniowym, na którym osoby fizyczne lub firmy mogą sprzedawać/oddawać/wymieniać/kupować wszelkiego rodzaju przedmioty, jak akcesoria domowe, telefony, ubrania, samochody i wiele innych. Istnieje również możliwość wyszukiwania/ dodawania ogłoszeń o dotyczących pracy, czy wynajmu mieszkań. 
2. Użytkownikiem końcowym aplikacji jest każda osoba, która chce coś sprzedać lub oddać za darmo oraz każda osoba, która chce coś zakupić,czy pozyskać.
3. W moim odczuciu aplikacja jest user-friendly. W łatwy, przejrzysty i intuicyjny sposób można wyszukiwać przedmioty zarówno w wyszukiwarce, jak i poprzez wybór kategorii. Na żadnym etapie korzystania z aplikacji nie miałam kłopotów z odnalezieniem, czy zrozumieniem wybranej przeze mnie funkcjonalności. Już po pierwszym otwarciu aplikacji jasnym było, do czego ona służy.
4. W celu usprawnienia działania aplikacji poprawiłabym wykryte błędy w niedokładnym filtrowaniu. Dodatkowo dodałabym możliwiość licytowania przedmiotów wystawianych na sprzedaż. 
5. Główną różnicą między testowaniem aplikacji webowych, a natywnych jest sposób, w jaki wykonywane są testy. Aplikacje webowe tetowane są przy użyciu przeglądarki internetowej, natomiast aplikacje natywne można testować na 2 sposoby: pobierając daną aplikację na telefon komórkowy lub na symulator telefonu znajdującysię na komputerze. Kolejną różnicą jest to, że aby przetestować aplikację natywną, musimy mieć zainstalowaną aplikację na naszym urządzeniu, co wiąże się z tym, że jeśli testujemy aplikacjęna kilku urządzeniach, to za każdymrazem musi być ona instalowana. W przypadku testowania aplikacji webowych jest to nieco prostsze, ponieważ wystarczy w przeglądarkę internetową wpisać link do testowanej aplikacji. Przewagą aplikacji natywnych nad webowymi jest to, że mogą działać bez dostępu do internetu, a więc ich testy można wykonywać offline.

# Task 3

## Subtask 1 (Formatka do zgłaszania błędów)

https://docs.google.com/spreadsheets/d/15MGNENRVk_6UoSbtmVaFUjBIOa5s60bWrBhrS-yqOo0/edit#gid=0

## Subtask 2 (Testowanie według planów testów i raportowanie błędów)

https://docs.google.com/spreadsheets/d/1S52Uq8oKFw8aQkvxeRAc96_uXJGvja0tZA1Gitp-yuU/edit

## Subtask 3 (Raport z wykonanych testów)

https://docs.google.com/document/d/10FrAqNUED2g2QteEixXeDuzbrjEzMS6IsWJeUmGgHAA/edit

# Task 2
## Subtask 1 (Pisanie przypadków testowych na podstawie User Story)

https://docs.google.com/spreadsheets/d/15B_kxponXvDJuRT9Ur2NUWHkwNsxYgYmJvy-sK0NoB0/edit#gid=0

## Subtask 2 (Pisanie przypadków testowych na podstawie własnych doświadczeń)

https://docs.google.com/spreadsheets/d/1w4nM4VuyFe33rlqD2l506WPaFX1tNcxaw4cTY2Weafc/edit#gid=0

## Subtask 3 Po co piszemy test case’y?

Przypadki testowe piszemy, aby dobrze rozplanować wszystko to co chcemy przetestować. Dzięki nim mamy wiekszą kontrolę nad tym co jest testowane i większą pewność, że żadna ważna funkcjonalność nie została pominięta. Przypadki testowe ułatwiają również tworzenie raportu z testów. Dobrze opisane przypadki testowe mogą być również pomocne dla całego teamu testerskiego- każda osoba, która będzie je czytać, będzie wiedziała co i jak zostało przetestowane.

# Task 1

## Subtask 1

8 punktów

## Subtask 3

Cześć, mam na imię Ola. Zdecydowałam się na udział w challengu, ponieważ już od jakiegoś czasu myślę o przebranżowieniu się na testera, a to wyzwanie z pewnością mi w tym pomoże. Liczę, że wzięcie udziału w tym przedsiewzięciu doda mi dodatkowej motywacji i inspiracji do samodzielnej pracy, a ukończenie go zaowocuje fajnym projektem, którym będę mogła pochwalić się w portfolio. 

## Subtask 4

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
