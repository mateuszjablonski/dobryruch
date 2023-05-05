# Partia w repozytorium Git

Rozważmy pomysł prowadzenia dokumentacji partii politycznej w publicznie dostępnym repozytorium.

Na wstępie musimy ustalić postawowe rzeczy:
- co to jest publicznie dostępne repozytorium
- czym jest dokumentacja partii politycznej

## Repozytorum

Definicja z [Wikipedii](https://pl.wikipedia.org/wiki/Repozytorium) mówi:

> Repozytorium (łac. repositorium) – miejsce uporządkowanego przechowywania dokumentów, z których wszystkie przeznaczone są do udostępniania. 

Takie jest też założenie naszego rozważania. Wszystkie dokumenty umieszczone w naszym repozytorium powinny być publicznie dostępne dla każdego, nawet największego polityczego oponenta. Nie oznacza to oczywiście, że wszystkie dokumenty, jakie partia kiedykolwiek wytworzy lub jakimi dysponuje, powinny się znaleźc w takim repozytorium - ale gdy już się w nim znajdą, to stają się one publicznie dostępne. Temat dokumentów zostanie omówiony w dalszej części. 

Osobnym tematem jest kwestia doboru technologii. Powinna ona
- dawać łatwy dostęp do przeglądnięcia danych
- nie wymagać instalacji skomplikowanego oprogramowania
- oferować uporządkowaną i jasną z punktu widzenia czytelnika strukturę
- umożliwiać współpracę w modelu rozproszonym
- pozwalać śledzić historię zmian wraz z datą, informacją o autorze, powodach zmiany oraz osób akceptujących te zmiany
- być ogólnodostępna
- być darmowa

## Dokumentacja partii politycznej

Dokumentacją w tym rozważaniu potraktujmy każdy tekstowy, graficzny lub audiowizualny wytwór partii.

W szczególności mogą to być:
- treści zawartych umów
- lista wpłat i wypłat na konto partyjne
- wpisy/artykuły ze strony internetowej
- posty/materiały na portale społecznościowe
- projekty ustaw
- program partii
- różnego rodzaju regulaminy, deklaracje

Do publikacji części dokumentacji partie polityczne są zobligowane przepisami prawa. Część z nich jest dostępna siłą rzeczy. Jeszcze inną część warto udostępnić w celach popularyzatorskich, marketingowych, rozwojowych. Warto potraktować samą stronę internetową jako dokumentację. Strona internetowa może być dodatkowym sposobem przeglądania wszystkich zgromadzonych w repozytorium zasobów (oprócz bezpośredniego dostępu do plików repozytorium), ale sformatowanym odpowiednio dla przeciętnego użytkownika internetu. Każdy dodany do repozytorium dokument stawałby się automatycznie łatwo dostępnym elementem strony internetowej.

## Aspekty techniczne

Narzędziami do relizacji tego projektu mogłoby być: repozytorium oparte o Git, pliki Markdown zawierające treść dokumentów, struktura oparta o katalogi/foldery. Otwartość i powszechność Gita połączona z prostotą Markdown (oraz faktem, że jest to format "plain-text") oraz dostępnością takich serwisów jak Github sprawia, że wszystkie założenia "repozytoryjne" są spełnione, a jednocześnie w żadnym stopniu nie ograniczają przyszłych większych modyfikacji, czy nawet całkowitego odejścia od tej metody.

Stronę internetową, opartą w 100% na dokumentach w repozytorium można generować za pomocą tzw. SSG (static site generator), jak np. [Hugo](https://gohugo.io/). Strona internetowa partii jest bytem statycznym, nie ma tam żadnych ankiet, komentarzy, itp. - ma to być pewnego rodzaju "encyklopedia", lub biuletyn informacji publicznej. Używanie skomplikowanych CMSów - takich jak na przykład Wordpress - zwiększa powierzchnię ataku, wymaga większych nakładów finansowych na utrzymanie, i niesie ciągłe ryzyko włamania - w przeciwieństwie do plików HTML/CSS/JS których treść i tak jest jawna do podejrzenia w inspektorze większości nowoczesnych przeglądarek.

Taka architektura pozwala też na stworzenie automatów, które w zależności od warunków, będą publikować różne treści w różnych mediach społecznościowych - Facebook, Twitter, Instagram, TikTok, Youtube, itp. Dzięki temu repozytorium byłoby de facto "pojedynczym źródłem prawdy" dla całej działalności partii, a jego historia medialna byłaby na bieżąco do prześledzenia.  

## Open Source

Prowadzenie takiego repozytorium jest pewnego rodzaju zaproszeniem dla osób, które są zainteresowane wolnym i otwartym oprogramowaniem. Zapewne zwróci ich uwagę możliwość przejrzenia historii zmian, zapoznania się z pełną treścią dokumentów, a być może zachęci do aktywnego włączenia się w działalność partii - i to pod różnymi względami. Ktoś może zaproponować nowy projekt ustawy, nowy artykuł, nowego mema, zdjęcie, poprawić literówki, rozpocząć dyskusję na temat punktu programu albo zaproponować mnóstwo innych rzeczy. Dzięki temu organizacja będzie mogła skorzysta ze wszystkich zalet wolnego i otwartego oprogramowania.

Co więcej, istnieją ruchy, które tematykę wolnego oprogramowania wiążą bezpośrednio z administracją państwową - postulując korzystanie z takiego oprogramowania przez urzędy, a także promując legislację zobowiązującą do otwierania kodu źródłowego programów tworzonych za publiczne pieniądze. Osoby wtajemniczone na pewno znają historie z oprogramowaniem ZUSU w kontekście kosztów, kodem PKP i ich z funkcją do sprawdzania `czyWybranoPsa()`. Jedną z takich inicjatyw jest np. [Public Money - Public Code](https://publiccode.eu/pl/).

## Benefity dla zaangażowanych

Ponieważ dostęp jest otwarty, każdy może kontrybuować. Serwisy takie jak Github mają bardzo prosty i intuicyjny interfejs, dzięki któremu członkowie partii mogliby na bieżąco monitorować zmiany w dokumentach, komentować, zadawać pytania i dodawać swoje własne propozycje. Dzięki takiemu rozwiązaniu osoby naprawdę zaangażowane miałyby możliwość realnego wpływu na kształt partii. Prawdziwa cyrfowa demokracja.

## Transparentność

W tym temacie chyba wszystko zostało już powiedziane. Ale jest to kolejna platforma do potencjalnej współpracy z organizacjami, które walczą o jawność w polityce, np. Watchdog Polska.

## Analiza SWOT

Strengths - mocne strony
- nikt tak nie robi, aspekt wyjątkowości
- robimy tak, jak mówimy
- wysoka transparentność, szczególnie mile widziana w obecnym kontekście politycznym
- relatywnie proste narzędzia, brak tzw. vendor lock-in

Weaknesses - słabe storny
- proponowane rozwiązanie jest nieznane, niesprawdzone

Opportunities - szanse
- redukcja kosztów utrzymania strony internetowej
- zwiększenie bezpieczeństwa strony internetowej
- automatyzacja niektórych zadań związanych z mediami społecznościowymi

Threats - zagrożenia
- nowe podejście zawsze budzi sprzeciw i opór wśród niektórych
- wymagana większa biegłość technologiczna
