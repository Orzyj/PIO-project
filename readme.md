# Projekt Przychodnia 

Projekt realizowany na przedmiocie Podstawy inżynieri Oprogramowania

## Cel Projektu

Stworzenie wirtualnej przychodni umożliwiające pacjentom i lekarzom zdalne korzystanie z zasobów przychodni.

## Zakres Projektu
> przedstawienie funkcjonalności projektu

Ograniczmy sie do aplikacji, która będzie obsługiwać pacjentów danej przchodni umożliwiając im rejestrowanie, logowanie, umawianie/edycje wizyt, przechowywanie dokumentacji medycznej pacjentów oraz danych osobowych lekarzy lub pacjentów.


### Wymagania funkcjonalne

Do wymagań funkcjonalnych należą: 
* Logowanie Pacjentów
* Logowanie Lekarzy
* Rejestrowanie Pacjentów
* Generowanie/Wydawnie recept
* Porowadzenie dokumentacji wizyt
* Przechowywanie informacji o danych osobowych
* Zarządzanie wizytami
* Zarządzanie historią medyczną pacjentów
* Przechowywanie dokumentacji medycznej pacjentów
* Integracja z użytkownikiem

### Wymagania niefunkcjonalne

Do wymagań nie funkcjonalnych należą: 
* Bezpieczeństwo danych osobowych
* Bezpieczeństwo informacji na temat wizyt
* Ograniczenie logowania do 3 prób później blokada czasowa
* Hashowanie danych (haseł)
* Zabezpieczenie przed błędnym podaniem danych


### Diagram klas
W przypadku systemu dla Przychodni  wyróżniamy takie klasy. 

    Klasa Pacjent:

    *Imię (string)
    *Nazwisko (string)
    *PESEL (string)
    *Adres (string)
    *Telefon (string)
    *Email (string)
    *Data urodzenia (data)
    *Płeć (enum: mężczyzna, kobieta)

    Klasa Lekarz:

    *Imię (string)
    *Nazwisko (string)
    *Specjalizacja (string)
    *Telefon (string)
    *Email (string)
    *Numer prawa wykonywania zawodu (string)

    Klasa Wizyta:

    *Data (data)
    *Godzina rozpoczęcia (godzina)
    *Godzina zakończenia (godzina)
    *Opis wizyty (string)
    *Pacjent (obiekt klasy Pacjent)
    *Lekarz (obiekt klasy Lekarz)

    Klasa Rejestracja:

    *Numer identyfikacyjny (string)
    *Data rejestracji (data)
    *Pacjent (obiekt klasy Pacjent)
    *Lekarz (obiekt klasy Lekarz)

    Klasa Historia Medyczna:

    *Data pierwszej wizyty (data)
    *Diagnoza (string)
    *Opis leczenia (string)
    *Pacjent (obiekt klasy Pacjent).
