# Protokół HTTPS
## I. Definicja protokołu HTTPS

HTTPS - czyli Hypertext Transfer Protocol Secure, to protokół komunikacyjny wykorzystywany w Internecie do bezpiecznej transmisji danych. Jest to bezpieczna wersja protokołu HTTP, gdzie dodano warstwę SSL/TLS w celu zaszyfrowania danych przesyłanych między klientem a serwerem. 

## II. Różnica między protokołem HTTP a HTTPS

HTTPS - czyli Hypertext Transfer Protocol Secure, to protokół komunikacyjny wykorzystywany w Internecie do bezpiecznej transmisji danych. Jest to bezpieczna wersja protokołu HTTP, gdzie dodano warstwę SSL/TLS w celu zaszyfrowania danych przesyłanych między klientem a serwerem. 

 | HTTP | HTTPS |
 | --- | --- |
 | Przesyła dane w formie niezaszyfrowanej | Przesyła dane w formie zaszyfrowanej | 
 | Nie wymaga certyfikatów SSL/TLS. | Używa protokołów kryptograficznych (SSL/TLS) do zaszyfrowania danych. |
 | Działa na standardowym porcie 80. | Działa na standardowym porcie 443. |
 | Jest podatny na przechwycenie danych przez osoby trzecie. | - |


## III. Jak działa HTTPS

Na początku uzgadniana jest tożsamość serwera oraz urządzenia użytkownika. Kolejnym krokiem jest wymiana wiadomości zawierających informacje, które umożliwią później nawiązanie interakcji pomiędzy stronami. Po zakończeniu tej interakcji, dochodzi do wymiany certyfikatów i gdy wszystko jest w porządku, przekazywane są klucze szyfrujące. Dzięki nim możliwe jest przesyłanie zaszyfrowanych danych i ich poprawne odbieranie przez uczestników komunikacji, czyli przez serwer i urządzenie odbierające, z którego korzysta użytkownik. Jednocześnie szyfrowanie sprawia, że nawet przechwycone przez niepowołane osoby dane nie zostaną odtworzone i nie dojdzie do utracenia poufnych danych. 

## IV. Rodzaje certyfikatów SSL/TLS

Istnieją trzy podstawowe typy certyfikatów SSL, które określa się na podstawie poziomu weryfikacji (walidacji) danego podmiotu, jakiemu wydaje się certyfikat. 

1. Certyfikat DV (Domain Validation) - czyli certyfikat z weryfikacją domeny. Walidacja dokonuje się w sposób zautomatyzowany i obejmuje informacje zgromadzone w systemie DNS dla domeny danego serwera oraz dane podmiotu ubiegającego się o certyfikat. Weryfikacja nie obejmuje natomiast danych organizacji. W certyfikacie DV zawarta jest jedynie nazwa domeny bez żadnych dodatkowych informacji o podmiocie. 

Certyfikat DV jest najtańszy, a jego wystawienie trwa zaledwie parę minut. Zautomatyzowanie całego procesu wiąże się jednak z pewnymi ograniczeniami. Certyfikaty te potwierdzają bezpieczeństwo danej strony, ale nie dostarczają żadnej wiedzy o jej wydawcy. Dlatego sprawdzają się w przypadku takich transmisji danych, które odbywają się między ufającymi sobie stronami.

 

 
