INSTRUKCJA OBSŁUGI WTYCZKI QGIS
1. FUNKCJONALNOŚĆ WTYCZKI:
Wtyczka "Wtyczka do projektu 2" zapewnia obliczenie wysokości dwóch punktów zaznaczonych przez użytkownika w programie Qgis na aktywnej warstwie, 
a także obliczenie pola powierzchni na podstawie trzech wybranych punktów na aktywnej warstwie.

2. WYMAGANIA DO UŻYCIA WTYCZKI:
Aby wtyczka zadziałała na danym laptopie/komputerze musi on mieć zainstalowanego Pythona wersję 3.9, QGIS wersję 3.28.4, Qt Designera with QGIS 3.28.4 custom widgets, a także zintegrowane środowisko Spyder wersja 5.1.5. Aby skorzystać z wtyczki należy pracować 
na warstwie z usługi WFS osługującej atrybuty z wartościami wysokości oznaczone w tabeli atrybutów jako id równe 6, atrybuty współrzędnej X oznaczone id równym 3, 
a atrybuty współrzędnych Y oznaczone id równym 4.

3. SYSTEM OPERACYJNY NA KOMPUTERZE A WTYCZKA: Wtyczka została utworzona dla systemu operacyjnego Windows 10

4. PRACA Z WTYCZKĄ:
Po zaintalowaniu wtyczki z pliku ZIP (wtyczka_do_programu.zip) w programie QGIS, należy dodać nowe połączenie usługi WFS ,,Podstawowa
Osnowa Geodezyjna Pozioma" i osobno dla ,,Podstawowa Osnowa Geodezyjna Wysokościowa",  po uprzednim skopiowaniu linku do 
nich ze strony https://www.geoportal.gov.pl/uslugi/usluga-pobierania-wfs. 

a) Wyznaczenie różnicy wysokośći na podstawie wysokości dwóch punktów: 
W celu wyznaczenie różnicy wysokości między punktami użytkownik musi przeciągnąć do pola "Warstwy" usługę z WFS dla osnowy wysokościowej. 
Następnie należy uruchomić w QGIS wtyczkę projekt2 (Plugin name) i rozwinięciu jej do wtyczka_do_projektu (Module name) i zaznaczyć na bieżącej warstwie dwa punkty.
W przypadku wybrania mniej niż dwa punkty zostanie wyświetlony komunikat ,,Zaznaczno  za małą liczbę punktów", a gdy użytkownik wybierze więcej niż dwa-komunikat ,,Zaznaczono za dużą liczbe punktów". 
Po zaznaczeniu dwóch punktów należy kliknąć pole o nazwie ,,Różnica wysokości", po czym w okienku po prawej pojawi się obliczona 
przez program wartość tej różnicy w jednostkach metry, zaokrąglona do części tysięcznych. W oknie komunikatów programu QGIS zostają wyświetlone również 
numery punktów na podstawie, których wyznaczono te różnicę.
Wtyczka została napisana dla wyznaczenia różnicy wysokości pobranej z warstwy atrybutów o nazwie "h_plevrf2007nh", czyli dla wartości w obecnie 
obowiązującym układzie wysokościowym w Polsce. Przy zmianie warstwy należy pamiętać o zamknięciu okna wtyczki przycikiem ,,Anuluj" i otwarci jej na nowo po załadowaniu kolejnej warstwy.

b) Wyznaczenie pola powierzchni na podstawie trzech współrzędnych punktów:
W celu wyznaczenie pola powierzchni na podstawie współrzędnych punktów użytkownik musi przeciągnąć do pola "Warstwy" usługę z WFS dla osnowy poziomej. 
Następnie należy uruchomić w QGIS wtyczkę i zaznaczyć na bieżącej warstwie co najmniej trzy punkty. W przypadku wybrania mniej niż trzech punktów zostanie wyświetlony 
komunikat ,,Zaznaczno  za małą liczbę punktów". Po zaznaczeniu co najmniej trzech punktów należy 
kliknąć pole o nazwie ,,Pole powierzchni", po czym w okienku po prawej pojawi się obliczona przez program wartość tego pola w jednostkach metry kwadratowe,
zaokrąglona do części tysięcznych. Wtyczka została napisana dla wyznaczenia pola powierzchni punktów  dla atrybutów  warstwy o nazwie "x1992" i "y1992", 
czyli dla wartości w układzie współrzędnych prostokątnych PL-1992. 

5. ZNANE BŁĘDY I NIETYPOWE ZACHOWANIA PROGRAMU:
Czasem monity wyświetlają się z opóźnieniem, jednak być może to kwestia powolnego działania programu QGIS.

