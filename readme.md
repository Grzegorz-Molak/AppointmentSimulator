# System umawiania wizyty u lekarza w JAVIE

##  Wymagane moduły
Należy pobrać sterownik bazy danych mariaDB

https://mariadb.com/kb/en/about-mariadb-connector-j/

Ścieżkę do pliku .jar należy dodać w project structure => dependencies

## System umawiania wizyty u lekarza w JAVIE
Celem projektu było zrealizowanie systemu umożliwiającego użytkownikowi rejestrację na wizytę u lekarza z wykorzystaniem Javy. Aplikacja połączona jest z bazą danych MariaDB za pomocą JDBC oraz udostępnia użytkownikowi interfejs graficzny wykonany przy użyciu biblioteki SWING.
Działanie programu
Po uruchomieniu programu użytkownik zostaje poproszony o zalogowanie do aplikacji za pomocą swojego login oraz hasła.
 
W przypadku gdy użytkownik nie posiada konta, może się zarejestrować, uzupełniając pola odpowiednimi wartościami i zatwierdzając.
 
Po zalogowaniu użytkownikowi ukazuje się lista jego nadchodzących wizyt, z możliwością natychmiastowej rezygnacji. Dostępne są również przycisku umożliwiające nawigację, a przy tym dostęp do innych funkcji systemu takich jak: rezerwacja wizyty, przegląd przeszłych wizyt  oraz przegląd lekarzy wraz z ich tygodniowymi zmianami.
 
Wyszukanie pasującej użytkownikowi wizyty ułatwione jest poprzez filtrację wyników w takich kategoriach jak: specjalizacja lekarza, ograniczenie do konkretnego lekarza, lokalizacja oraz przedział czasowy, w którym ma się znajdować wizyta.
 
Wybór wizyty i kliknięcie Reserve appointment powoduje rezerwację wybranej wizyty i przejście z powrotem do panelu nadchodzących wizyt
 
W przypadku gdy po pokazaniu możliwości użytkownikowi, ktoś inny zarezerwował wizyt, nie powiedzie się to, a użytkownik otrzyma stosowny komunikat
 
Historia wizyt pozwala przeglądać odbyte wizyty oraz przeniesienie do panelu lekarza przeprowadzającego daną wizytę, przykładowo w celu sprawdzenia zmian lekarza w celu ponownego umówienia się na wizytę
 
## Struktura aplikacji
Aplikacji składa się z 3 klas służących do uruchomienia i testowania aplikacji:
Main – do uruchomienia aplikacji
Test – do testowania zdolności aplikacji do połączeń z bazą danych
Initialize – do zainicjowania i wstępnego wypełnienia prostej bazy danych do obsługi aplikacji
Reszta plików została podzielona na 3 paczki
Model – znajdują się tu klasy obiektów używanych do wyświetlania danych użytkownikowi, takie jak: Patient, Doctor, Appointment
DAO – znajdują się tu klasy służące do obsługi bazy danych, takie jak połączenia z nią oraz pobieranie czy zapis obiektów klas należących do paczki Model z/do bazy danych.
VIew – odpowiada za interfejs graficzny i obsługę zdarzeń z nim związanych. 

