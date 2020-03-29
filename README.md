# Koronawirus (Covid-19) - dane ze Stanów Zajednoczonych

[ [U.S. State-Level Data](us-states.csv) ([Raw CSV](https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csv)) | [U.S. County-Level Data](us-counties.csv) ([Raw CSV](https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv)) ]

# Dane z New York Times, na podstawie raportów ze stanowych i lokalnych agencji zdrowia

New York Times wydaje serię plików danych ze skumulowaną liczbą przypadków koronawirusa w Stanach Zjednoczonych, na szczeblu stanowym i okręgowym (hrabstw), w miarę upływu czasu. Gromadzimy dane z tych szeregów czasowych z rządów stanowych i lokalnych oraz departamentów zdrowia w celu zapewnienia pełnego zapisu trwającego wybuchu epidemii.

Od końca stycznia The Times śledził przypadki koronawirusa w czasie rzeczywistym, gdy wykryto je po testach. Jednak z powodu powszechnego braku testów, dane są koniecznie ograniczone na obrazie przedstawiającym wybuch epidemii.

Wykorzystaliśmy te dane do zasilania naszych [map](https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html) i [raportowania](https://www.nytimes.com/coronavirus) śledzenia epidemii, a teraz jest to udostępniane opinii publicznej w odpowiedzi na prośby badaczy, naukowców i urzędników państwowych, którzy chcieliby uzyskać dostęp do danych, aby lepiej zrozumieć epidemię.

Dane rozpoczynają się od pierwszego zgłoszonego przypadku koronawirusa w stanie Waszyngton 21 stycznia 2020 r. Będziemy publikować regularne aktualizacje danych w tym repozytorium.

* >Raw data - surowe dane.
* >County - hrabstwo. State - stan.

## Dane - Stany Zjednoczone

Dane dotyczące skumulowanych przypadków zakażenia koronawirusem i zgonów można znaleźć w dwóch plikach dla **stanów** i **hrabstw**.

Każdy wiersz danych podaje skumulowane liczby w oparciu o nasze najlepsze raporty do momentu opublikowania aktualizacji. Dokładamy wszelkich starań, aby korygować wcześniejsze wpisy w danych, gdy otrzymujemy nowe informacje.

Oba pliki zawierają [kody FIPS](https://www.census.gov/quickfacts/fact/note/US/fips), standardowy identyfikator geograficzny, aby ułatwić analitykowi połączenie tych danych z innymi zestawami danych, takimi jak plik mapy lub dane o populacji.

Pobierz wszystkie dane lub sklonuj to repozytorium, klikając zielony przycisk „Klonuj lub pobierz” powyżej.


### Dane - poziom stanowy (w oparciu o stany)

Dane na poziomie stanu można znaleźć w pliku [states.csv](us-states.csv). ([Plik Raw CSV tutaj.](https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csv))

```
date,state,fips,cases,deaths
2020-01-21,Washington,53,1,0
...
```

### Dane - poziom hrabstwa (w oparciu o hrabstwa)

Dane na poziomie hrabstwa można znaleźć w pliku [counties.csv](us-counties.csv). ([Plik Raw CSV tutaj.](https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv))

```
date,county,state,fips,cases,deaths
2020-01-21,Snohomish,Washington,53061,1,0
...
```

W niektórych przypadkach obszary geograficzne, w których zgłaszane są przypadki, nie są odwzorowane na standardowe granice hrabstwa. Zobacz listę [wyjątków geograficznych](#geographic-exceptions), aby uzyskać więcej szczegółów na ten temat.

## Metodologia i definicje

Dane są produktem pracy dziesiątek dziennikarzy pracujących w różnych strefach czasowych w celu monitorowania konferencji prasowych, analizowania publikacji danych i szukania wyjaśnień od urzędników publicznych na temat tego, w jaki sposób kategoryzują przypadki.

Jest to również odpowiedź na rozdrobniony amerykański system zdrowia publicznego, w którym przytłoczeni urzędnicy stanowi, hrabstw i terytorialni czasami usilnie starają się przekazywać informacje dokładnie, konsekwentnie i szybko. Kilkakrotnie urzędnicy poprawiali informacje godziny lub dni po pierwszym zgłoszeniu. Czasami przypadki znikały z lokalnej bazy danych władz lub urzędnicy przenieśli najpierw pacjenta zidentyfikowanego w jednym stanie lub hrabstwie do innego, często bez wyjaśnienia. W przypadkach, które stały się bardziej powszechne w miarę wzrostu liczby przypadków, nasz zespół dołożył wszelkich starań, aby zaktualizować dane w celu odzwierciedlenia najbardziej aktualnych, dokładnych informacji, jednocześnie zapewniając, że każdy znany przypadek jest liczony.
Gdy informacje są dostępne, liczymy pacjentów tam, gdzie są leczeni, niekoniecznie w miejscu ich zamieszkania.

W większości przypadków proces rejestrowania przypadków był prosty. Ale z powodu mnogości metod zgłaszania tych danych w ponad 50 rządach stanowych i terytorialnych oraz w setkach lokalnych departamentów zdrowia, nasi dziennikarze musieli czasem dokonywać trudnych interpretacji dotyczących liczenia i rejestrowania przypadków.

Z tych powodów nasze dane w niektórych przypadkach nie będą dokładnie odpowiadały informacjom zgłaszanym przez stany i hrabstwa. Różnice te obejmują te przypadki: kiedy rząd federalny zorganizował loty do Stanów Zjednoczonych dla Amerykanów narażonych na koronawirusa w Chinach i Japonii, nasz zespół odnotował te przypadki w stanach, w których pacjenci byli następnie leczeni, chociaż lokalne oddziały zdrowia na ogół nie. Kiedy mieszkanka Florydy zmarła w Los Angeles, odnotowaliśmy, że jej śmierć miała miejsce w Kalifornii, a nie na Florydzie, chociaż urzędnicy na Florydzie odnotowali jej przypadek we własnych aktach. A kiedy urzędnicy w niektórych stanach zgłosili nowe przypadki bez natychmiastowego określenia, gdzie leczeni są pacjenci, próbowaliśmy dodać informacje o ich lokalizacji później, gdy tylko będą dostępne.

* Potwierdzone przypadki

Potwierdzonymi przypadkami są pacjenci, u których wynik testu na obecność koronawirusa jest dodatni. Uważamy przypadek za potwierdzony, gdy został zgłoszony przez federalną, stanową, terytorialną lub lokalną agencję rządową.

* Daty

Dla każdej daty pokazujemy łączną liczbę potwierdzonych przypadków i zgonów zgłoszonych tego dnia w danym hrabstwie lub stanie. Wszystkie przypadki i zgony są liczone od daty pierwszego ogłoszenia.

* Hrabstwa

W niektórych przypadkach dane z wielu hrabstw lub innych regionów poza hrabstwem zgłaszamy, jako jedno hrabstwo. Na przykład zgłaszamy jedną wartość dla Nowego Jorku, obejmującą przypadki dla hrabstw w Nowym Jorku, Kings, Queens, Bronx i Richmond. W takich przypadkach pole kodu FIPS będzie puste. (W przyszłości możemy przypisywać kody FIPS do tych obszarów geograficznych.) Zobacz listę [wyjątków geograficznych](#geographic-exceptions). 

Miasta takie jak St. Louis i Baltimore, które są administrowane oddzielnie od sąsiedniego hrabstwa o tej samej nazwie, są liczone osobno.

* Hrabstwa “nieznane”

Wiele stanowych departamentów zdrowia decyduje się na osobne zgłaszanie przypadków, gdy miejsce zamieszkania pacjenta jest nieznane lub oczekuje na ustalenie. W takich przypadkach rejestrujemy nazwę hrabstwa jako „Nieznane”. W miarę udostępniania większej ilości informacji o tych przypadkach skumulowana liczba przypadków w hrabstwach „Nieznane” może się zmieniać.

Czasami przypadki są najpierw zgłaszane w jednym hrabstwie, a następnie przenoszone do innego hrabstwa. W rezultacie skumulowana liczba przypadków może ulec zmianie dla danego hrabstwa.

### Wyjątki geograficzne

* New York City

Wszystkie przypadki dla pięciu dzielnic Nowego Jorku (hrabstwa Nowy Jork, Kings, Queens, Bronx i Richmond) są przypisane do jednego obszaru o nazwie Nowy Jork.

* Kansas City, Mo.

Cztery hrabstwa (Cass, Clay, Jackson i Platte) pokrywają się z okolicą Kansas City, Mo. Przypadki i zgony, które pokazujemy dla tych czterech hrabstw, dotyczą tylko części z wyłączeniem Kansas City. Przypadki i zgony w Kansas City są zgłaszane jako osobna linia.

* Joplin, Mo.

Joplin jest zgłaszany osobno od hrabstw Jasper i Newton.

* Chicago

Wszystkie przypadki i zgony w Chicago są zgłaszane jako część hrabstwa Cook.


## Licencja i uznanie autorstwa

Zasadniczo udostępniamy te dane publicznie do szerokiego, niekomercyjnego użytku publicznego, w tym przez badaczy medycyny i zdrowia publicznego, decydentów, analityków i lokalne media.

Jeśli korzystasz z tych danych, musisz przypisać je do „The New York Times” w dowolnej publikacji. Jeśli chcesz bardziej rozwinięty opis danych, możesz powiedzieć „Dane z New York Times, na podstawie raportów ze stanowych i lokalnych agencji zdrowia.”

Jeśli użyjesz go w prezentacji online, będziemy wdzięczni, jeśli umieścisz link do naszej strony śledzenia w USA pod adresem [https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html](https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html).

Jeśli korzystasz z tych danych, daj nam znać na adres covid-data@nytimes.com i wskaż, czy zechcesz porozmawiać z reporterem o swoich badaniach.

Zobacz naszą [LICENCJĘ](LICENSE) dla pełnych warunków korzystania z tych danych.


## Skontaktuj się z nami

Jeśli masz pytania dotyczące danych lub warunków licencyjnych, skontaktuj się z nami pod adresem:

covid-data@nytimes.com


## Współtwórcy

Mitch Smith, Karen Yourish, Sarah Almukhtar, Keith Collins, Danielle Ivory oraz Amy Harmon przewodzą naszym wysiłkom w zakresie gromadzenia danych w USA.

Dane zostały również opracowane przez Jordan Allen, Jeff Arnold, Aliza Aufrichtig, Mike Baker, Matthew Bloch, Nicholas Bogel-Burroughs, Maddie Burakoff, Christopher Calabrese, Andrew Chavez, Robert Chiarito, Carmen Cincotti, Alastair Coote, Matt Craig, John Eligon, Tiff Fehr, Andrew Fischer, Matt Furber, Rich Harris, Lauryn Higgins, Jake Holland, Will Houp, Jon Huang, Danya Issawi, Jacob LaGesse, Patricia Mazzei, Allison McCann, Jesse McKinley, Miles McKinley, Sarah Mervosh, Andrea Michelson, Blacki Migliozzi, Steven Moity, Richard A. Oppel Jr., Jugal K. Patel, Nina Pavlich, Azi Paybarah, Sean Plambeck, Scott Reinhard, Thomas Rivas, Michael Robles, Alison Saldanha, Alex Schwartz, Libby Seline, Shelly Seroussi, Rachel Shorey, Anjali Singhvi, Charlie Smart, Ben Smithgall, Steven Speicher, Michael Strickland, Albert Sun, Tracey Tully, Maura Turcotte, Miles Watkins, Jeremy White, Josh Williams and Jin Wu.

*Tłumaczenie: @[mbiesiad](https://github.com/mbiesiad)
*29/3/2020
