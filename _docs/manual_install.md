---
title: "Instalacja"
permalink: /docs/manual-install/
excerpt: "Dokumetacja ALTPiw - instrukcja instalacji"
---

# Instalacja ALTPiw

Instalacja ALTPiw odbywa się w taki sam sposób jak każdego innego AddOnu w SAP. 

Na tą chwilę istnieją trzy możliwości dodania AddOnu z SAP

1. Uruchom aplikację

   ![image](https://user-images.githubusercontent.com/104000700/164240180-26f72303-f81d-4b46-9ef0-3fe3a46b915e.png)

2. Administracja -> Add On -> Menadżer Add On

   ![image](https://user-images.githubusercontent.com/104000700/164240594-a34ec28e-fd78-46c8-9fa4-5a9b4237046e.png)

   https://<Server Address>:<Port>/ExtensionManager

   ![image](https://user-images.githubusercontent.com/104000700/164241145-932f9564-cad9-43ea-9211-d97c1c649f87.png)
   
3. Administracja -> Add On -> Administracja Add On
 
   ![image](https://user-images.githubusercontent.com/104000700/164240037-1e218996-869c-49f9-a4cb-7eeb1b81d28b.png)

Na serwerze powinien znajdować się katalog z AddOnem, w któym będzie przechowywana jego aktualna wersja oraz ewentualne kopie oraz pliki .zip i .ard.
Zazwyczaj znajduje się on w lokalizacji C:\Altab\ALTPIW\. Jeśli nie będzie takiego katalogu nalezy go utworzyć zgodnie z poniższą strukturą
 
C:\Altab\ALTPIW\\[*wersja*]\\[*wersja aplikacji*]
 
*wersja* - np. 3.8.2.1
 
*wersja aplikacji* - np. x64 lub x32 

**Uwaga!!!**
 
**Nowe wersje AddOnu występują tylko w wersji 64-bit**
 




## Instalacja usługi
W pierwszej kolejności tworzymy katalog SAKOL3 w którym umieszczamy katalogi z aplikacją WWW, panelem administracyjnym oraz usługą.

![image](https://user-images.githubusercontent.com/93259107/144237890-1ff27912-4976-4437-afda-64d61150f880.png)

Kolejnym krokiem jest edycja pliku konfiguracyjnego sakol3.ini, który znajduje się w katalogu SAKOL3_DataService.

![image](https://user-images.githubusercontent.com/93259107/144241631-4522f740-35ca-4807-8210-c14dec022ab3.png)

Zmieniamy parametry w pliku konfiguracyjnym.

![image](https://user-images.githubusercontent.com/93259107/147466691-626fb4c5-b422-4e69-9785-338ad42ff103.png)


W początkowej konfiguracji istotnymi parametrami są:
DataSource - jest to serwer SQL na którym jest baza danych SAKOL3
UserID - użytkownik SQL
Password - hasło SQL
DBName - nazwa bazy 
WSParam1 - Nazwa bazy SAP
HtmlAppPath - ścieżka do aplikacji WWW

Usługę instalujemy poprzez cmd z uprawnieniami administracyjnymi

![image](https://user-images.githubusercontent.com/93259107/144231064-8b4fb001-aa91-48c3-bba7-7a37f432bac1.png)

W cmd korzystamy z funkcji istallutil. 

![image](https://user-images.githubusercontent.com/93259107/144232784-b0c5285f-70f1-435a-8aa5-fb82c43ff701.png)

Jeżeli pojawi się poniższy komunikat oznacza, że usługa SAKOL3_DataService została zainstalowana

![image](https://user-images.githubusercontent.com/93259107/144233078-f430c7ee-e695-4bf2-81ba-58433f598685.png)

Konfigurujemy aplikację SAKOL3_Admin. Aplikacja znajduje się w następującej lokalizacji:
C:\Altab\Sakol3\SAKOL3_Admin

![image](https://user-images.githubusercontent.com/93259107/147468663-7f651ab9-1e62-41fd-ae0c-6520101cc751.png)
Ustawiamy poświadczenia do bazy danych oraz ważnym elementem jest parametr WsParam1, w któym określamy nazwę bazy SAP.
 
# Klient WWW
> Jak zainstalowac na IIS
W pierwszej kolejności dodajemy pulę aplikacji SAKOL3 w IIS

![image](https://user-images.githubusercontent.com/93259107/147079207-7f20cf91-b177-42a8-adbe-515b8a03ef2b.png)

Następnie konfigurujemy witrynę 

![image](https://user-images.githubusercontent.com/93259107/147083333-a6670db8-6704-47bd-aedb-9d08096e5f9d.png)

Konwertujemy nasz folder na aplikację 

![image](https://user-images.githubusercontent.com/93259107/147083597-8ddd8786-0ba5-4087-8ccf-414e32e7d7d5.png)

Zmieniamy ustawiania w pliku config.json, który znajduje się w następującej lokalizacji:

C:\Altab\Sakol3\inetpub\SAKOL3\assets

Edytujemy plik config.json. Zmianiamy wartość w polu EndPointAddress, ustawiamy adres witryny i port usługi.

![image](https://user-images.githubusercontent.com/93259107/147466858-5e653165-03c0-4494-8731-613856fc65ef.png)

Pamiętamy o pliku licencji, po któy musimy skontaktować się z firmą Altab, inaczej aplikacja SAKOL nie zadziała. Plik licencji należy skopiować do folderu z usługą:

![image](https://user-images.githubusercontent.com/93259107/147467202-4d270622-ee43-464e-919d-62778c7c9050.png)


Uruchamiamy aplikację SAKOL3 z poziomu IIS

![image](https://user-images.githubusercontent.com/93259107/147467174-76254d86-064b-4ed7-a0f5-f6969c79c411.png)

Aplikacja SAKOL z pustą bazą bez użytkowników i modułów wygląda następująco:

![image](https://user-images.githubusercontent.com/93259107/147468387-73d93790-a02d-4cfd-8529-0a7a65490be3.png)


# Sprawdzenie instalacji
Po instalacji SAKOL3 przechodzimy do weryfikacji działania aplikacji, przechodzimy do panelu administracyjnego, żeby dodać użytkownika i zalogować się do aplikacji:
Wybieramy zakładkę użytkownicy

![image](https://user-images.githubusercontent.com/93259107/147479687-8377b0fd-d78e-4c6a-9534-ae50bd24fbaa.png)

kilkamy przycisk "plus" w prawym dolnym rogu ekranu, przycisk "minus" po zaznaczaniu użytkownika usuwa go, przyciski te działają również w panelu administracyjnym na innych oknach.
W oknie edycji użytkownika dodajemy użytkownika o nazwie admin. Domyślne hasło dla każdego nowo tworzonego użytkownika to SAKOL2. Zmieniamy te hasło od razu w momencie tworzenia nowego użytkownika.

![image](https://user-images.githubusercontent.com/93259107/147479956-391e8f90-939e-4a6e-b5e9-ec2b8011bd0c.png)

Po zdefiniowaniu użytkownika przechodzimy do aplikacji SAKOL. Aby zmiany dotyczące użytkowników pojawiły się w aplikacji należy dokonać synchroniazacji.
Na oknie logowania wybieramy przycisk opcje-->synchronizacja

![image](https://user-images.githubusercontent.com/93259107/147480341-8b77cf88-4474-4d45-a675-0c6c7d9e5e48.png)

Po dokonaniu synchronizacji nowo stworzony użytkownik pojawia się na liście


![image](https://user-images.githubusercontent.com/93259107/147480397-c0e85008-13ed-48f8-9899-e509e04c4894.png)


Aby zalogować się do aplikacji SAKOL zaznaczamy użytkownika oraz klikamy przycisk dalej, nastęnie wpisujemy hasło i ponownie klikamy przycisk dalej.

Po zalogowaniu się pierwszy raz do aplikacji SAKOL powinna nam się wyświetlić pusta lista z uzupełnionym w nagłówku kodem użytkownika na któego jesteśmy zalogowani:


![image](https://user-images.githubusercontent.com/93259107/147480592-476f0d35-9950-42a3-8b2f-00d677f210aa.png)


Aby sprawdzić, czy aplikacja SAKOL jest poprawnie zainstalowana należy dodać moduł, który będzie można uruchomić. 
Aby dodać moduł w pierwszej kolejności dodajemy klasę o nazwie test. Klasę dodajemy poprzez kliknięcie w przycisk plusa.


![image](https://user-images.githubusercontent.com/93259107/147481076-9ac68236-4902-4dcf-a955-4b36d39a2d9f.png)






