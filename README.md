# KSEF-MF
Prosty program dla wsparcia KSeF (Krajowy System e-Faktur).

> [!IMPORTANT]
> Wersja ze wsparciem dla systemu KSeF 2.0 jest już dostępna. Proszę o wysyłanie zapytań na adres email - jpk.vdek@gmail.com

## Wstęp
KSeF to platforma do wystawiania, przesyłania, otrzymywania i przechowywania faktur (https://ksef.podatki.gov.pl/). Platforma jest wdrażana w różnych etapach, ale wcześniej czy później będzie obowiązkowa dla wszystkich przedsiębiorców.

Mniejsi przedsiębiorcy nie muszą kupować specjalistycznych programów do obsługi KSeF, bo Ministerstwo Finansów przygotowało darmowe narzędzie - https://ksef.podatki.gov.pl/aplikacja-podatnika-ksef-20/. Jednak to narzędzie wymusza szereg manualnych kroków, m.in. wpisanie NIP, logowanie z hasłem, dodatkowe podanie hasła z SMS, wypełnienie pól formularza, dodatkowe hasło z SMS podczas podpisywania dokumentu. Dodatkowo, po 3 minutach nieaktywności, użytkownik jest automatycznie wylogowany.

Ten program ma ułatwić wykonanie podstawowych operacji na KSeF w prosty sposób.

## Licencja
Uznanie autorstwa-Użycie niekomercyjne-Bez utworów zależnych 3.0 Unported (CC BY-NC-ND 3.0) (https://creativecommons.org/licenses/by-nc-nd/3.0/deed.pl)

## Wymagania

Do poprawnego działania programu wymagane jest środowisko Java (Java Runtime Environment, JRE)
w wersji 17 lub nowszej.

## Instalacja

## ConsoleApp

Pobierz program `consoleapp.zip` z https://github.com/piotrkot/ksef-mf/releases.

Rozpakuj plik `consoleapp.zip` do katalogu `consoleapp`.

#### Windows

Uruchom plik `ksef-cmd.bat` z katalogu `consoleapp`.

#### Linux

Uruchom plik `ksef-cmd.sh` z katalogu `consoleapp`.

### Opcje użycia

- `--help` - Wyświetlenie komunikatu pomocy.
- `--demo` - Użycie środowiska Demo Ministerstwa Finansów. Bez tej opcji użyte zostanie środowisko produkcyjne. W środowisku Demo wymagany jest token KSeF ze środowiska Demo.
- `--out=<katalog>` - Wskazanie katalogu do zapisu potwierdzenia UPO. Bez tej opcji użyty zostanie katalog bieżący.
- `--doc=<dokument>` - Wskazanie faktury (plik XML) do wysłania.
- `--nip=<NIP>` - Numer NIP podmiotu wysyłającego fakturę.
- `--token=<token KSeF>` - Token KSeF uwierzytelniający dostęp do API Ministerstwa Finansów. Token musi mieć przyznane prawo do wysyłania faktur. Token musi być odpowiedni dla środowiska, z jakim łączy się program. Patrz opcja `--demo`. Token należy umieścić w apostrofach, bo zawiera znaki specjalne, które mogą być zainterpretowane w linii poleceń.

### Przykłady

`$> ksef-cmd --demo --doc=fa.xml --nip=1234567890 --token=\"20260226-EC-22...625\""`

`$> ksef-cmd --out=/tmp --doc=fa.xml --nip=1234567890 --token='20260226-EC-22...625'`

## Kontakt

jpk.vdek@gmail.com
