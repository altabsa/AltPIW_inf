---
title: "Spis funkcji"
permalink: /docs/manual-user/
excerpt: "Dokumetacja SAKOL - spis funkcji systemu"
---

# Opis funkcjonalności
Częścią integralną aplikacji SAKOL jest aplikacja SAKOL_ADMIN. 
Aplikacja ta jak sama nazwa wskazauje jest panelem administracyjnym do zarządzania aplikacją SAKOL 
Dzięki tej aplikacji możemy dodawać użytkowników, definiować klasy, słowniki, poprzez zakładkę formatki możemy zaprojektować wygląd aplikacji. Dzięki opcji Addony WF mamy możliwość zakodowania logiki, czyli do wyglądu naszych formatek możemy zakodować funkcje, które pozwolą nam na poprawne funkcjonowanie aplikacji. Poniżej przedstawione są wszystkie opcje dostępne w panelu administracyjnym

![image](https://user-images.githubusercontent.com/93259107/143850389-f0ccb4c1-b639-49d7-a501-0d52c2464562.png)



## Użytkownicy <a name="hlp_users"></a>
`hlp_users`

Zakładka użytkowicy służy do dodawania lub modyfikowania użytkowników w aplikacji SAKOL. Dzięki tej zakładce mamy możliwość zmiany hasła do logowania.

![image](https://user-images.githubusercontent.com/93259107/143865839-057ab28f-dd27-4ed2-926f-314c03cc10ed.png)

W oknie użytkownicy mamy mozliwość definowania użytkowników aplikacji SAKOL

![image](https://user-images.githubusercontent.com/93259107/143867989-6e709b09-a0e3-4d66-a4f6-f7c0e50bf7fe.png)

##### Kod
Unikalny kod użytkownika, który jest widoczny w trakcie logowania

##### Stare hasło (uzupełniane przy zmianie hasła)
Hasło zdefiniowane dla danego użytkowika. Hasło domyślne przy tworzeniu użytkownika to SAKOL2. Przy tworzeniu użytkownika od razu zmieniamy to hasło na hasło liczbowe. 

##### Nowe hasło (uzupełniane przy zmianie hasła)
Nowe hasło definiowane dla użytkownika. W hasłach wykorzystujemy tylko liczby.

##### Nowe hasło2 (uzupełniane przy zmianie hasła)
Nowe hasło definiowane dla użytkownika. W hasłach wykorzystujemy tylko liczby.

##### Aktywny 
Parametr ten jeżeli jest zaznaczony oznacza, że użytkownik jest aktywny i jego login jest dostępny w SAKOL, jeżeli jest odznaczony użytkownik ten nie może logować się do aplikacji SAKOL.

##### Stanowisko
Pole te służy do grupowania użytkowników oraz nadawania im uprawnień do logowania. Np. Jeżeli w pole stanoiwsko wpiszemy Magazyn w trakcie logowania do SAKOL pod kodem użytkownika wyświetli się nazwa z pola stanowisko. Również możemy określić, że na danym urządzeniu np. kolektorze mogą się logować tylko magazynierzy, wtedy w oknie logowania wyświetlą się tylko użytkownicy, którzy mają w polu stanowisku nazwę Magazyn.

##### Gen. etykiety
Po kliknięciu w przycisk Gen. etykiety generuje się ciąg znaków. Powstały ciąg znaków możemy przedstawić jako kod QR dzięki któremu podczas logowanie użytkownik po zaczytaniu kodu automatycznie zaloguje się do aplikacji SAKOL

##### Użytkownik NTLM 
We wskazanym polu definiujemy nazwę użytkownika domenowego służącego do logowania poprzez konto Windows np. altab\adam, dzięki czemu możemy logować się do SAKOL za pomocą poświadczeń widnows.

## Klasy <a name="hlp_class"></a>
`hlp_class`
### Zastosowanie
  Do czego służy
### Lista własnosci
  Kolejno opisane własności 
### Pola klas <a name="hlp_class_fld"></a>
`hlp_class_fld`
  Lista własności 
### Projekt

![image](https://user-images.githubusercontent.com/93259107/143887490-591e7c6d-cca2-4ae4-a99b-c20f265fd5de.png)

  
## Formatki  <a name="hlp_forms"></a>
`hlp_forms`
### Zastosowanie
- Do czego służy
- Jak tworzyć
### Lista własnosci
  Kolejno opisane własności 
### Pola formatki  <a name="hlp_forms_fld"></a>
`hlp_forms_fld`
Lista własności 
### Projekt

![image](https://user-images.githubusercontent.com/93259107/143887809-7681a1d6-242a-4ddd-94c3-84689aff2a05.png)


## Słowniki <a name="hlp_dicts"></a>
`hlp_dicts`
### Zastosowanie
-Do dczego służy
- edycja danych
- Jak tworzyć
### Lista własnosci
  Kolejno opisane własności  
### Pola słownika <a name="hlp_dicts_fld"></a>
`hlp_dicts_fld`
  Opis wszytskich własnosci
### Projekt
Przykład dla projektu

## Addony <a name="hlp_addons"></a>
`hlp_addons`
### Zastosowanie
 Do dczego służy
### Eventy <a name="hlp_addons_evts"></a>
`hlp_addons_evts`
  Opis wszytskich eventów
### Specjalne
  Przerwanie formularza
### Warunki  <a name="hlp_addons_conds"></a>
`hlp_addons_conds`
  Jak tworzyć warunki
### Akcje  <a name="hlp_addons_actions"></a>
`hlp_addons_actions`
  #### Opis
  #### Akcja SQLOp  <a name="hlp_addons_sql"></a>
  `hlp_addons_sql`
  - Opis 
  - Lista własnosci
  #### Akcja SQLOp (wewnętrzny)   <a name="hlp_addons_sqli"></a>
  `hlp_addons_sqli`
  - Opis 
  - Lista własnosci
  #### Akcja MsgBoxOp  <a name="hlp_addons_msgbox"></a>
  `hlp_addons_msgbox`
  - Opis 
  - Lista własności
  #### Akcja DocOp  <a name="hlp_addons_doc"></a>
  `hlp_addons_doc`
  - Opis 
  - Lista własności
  #### Akcja ExCallOp  <a name="hlp_addons_excall"></a>
  `hlp_addons_excall`
  - Opis 
  - Lista własności
  #### Akcja FormOp  <a name="hlp_addons_form"></a>
  `hlp_addons_form`
  - Opis 
  - Lista własności
  #### Akcja UserTableOp  <a name="hlp_addons_usertable"></a>
  `hlp_addons_usertable`
  - Opis 
  - Lista własności

### Projekt
Przykład dla projektu

## Dokumenty  <a name="hlp_docs"></a>
`hlp_docs`
 Opis

## Import / Eksport <a name="hlp_impex"></a>
`hlp_impex`
 Opis

## Sesje <a name="hlp_sess"></a>
`hlp_sess`
 Opis1

