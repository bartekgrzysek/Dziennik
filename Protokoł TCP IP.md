# Protokół TCP/IP
## I. Definicja

TCP/IP, czyli Transmission Control Protocol/Internet Protocol, to zestaw protokołów używanych do komunikacji w sieciach komputerowych. Protokół ten jest fundamentem dla funkcjonowania Internetu. Składa się z dwóch głównych warstw: warstwy transportowej (TCP) i warstwy internetowej (IP).

![alt text](https://signal.avg.com/hs-fs/hubfs/Blog_Content/Avg/Signal/AVG%20Signal%20Images/What%20is%20TCPIP%20(Signal)/TCP-IP.png?width=1980&name=TCP-IP.png)

## II. Odbieranie i wysyłanie wiadomości

Każda wiadomość wysłana przez aplikację przechodzi przez wszystkie warstwy TCP/IP, od warstwy aplikacji do najniższej warstwy dostępu do sieci. Następnie jest transmitowana przez sieć do drugiego komputera. Na koniec przechodzi przez wszystkie warstwy w przeciwnym kierunku, aż do warstwy aplikacji i docelowego procesu.

Podczas przesyłania danych z aplikacji do sieci, każda warstwa dodaje swój własny nagłówek (ang. header) do każdej wiadomości. Każdy z tych nagłówków jest potem odczytywany przez odpowiednią warstwę w komputerze odbierającym wiadomość (gdzie, jak to już było powiedziane wcześniej, wiadomości są przesyłane z sieci do warstwy aplikacji i dalej). Zarówno zawartość jak i wielkość nagłówków zależą od użytych protokołów.

**Odbieranie wiadomości**
![alt text](http://www.crypto-it.net/Images/theory/tcpip/tcpip_flow_receive_pl.png)

**Wysyłanie wiadomości**
![alt text](http://www.crypto-it.net/Images/theory/tcpip/tcpip_flow_send_pl.png)

## III. Warstwy modelu TCP/IP

**1.Warstwa aplikacji (application layer)**

W tej warstwie pracują takie usługi jak np. serwer WWW lub przeglądarka internetowa. Aplikacje korzystają z zestawu protokołów, określających standardy komunikacji, w sieciach. Takimi protokołami są między innymi:

- Telnet - umożliwia prace w konsoli tekstowej.
-  FTP - umożliwia transmisje plików.
-  SMTP i POP3 - protokoły poczty elektronicznej, pierwszy umożliwia wysyłanie, drugi odbieranie wiadomości.
-  HTTP i HTTPS - pierwszy protokół przesyła stronę WWW, a drugi odpowiada za szyfrowanie transmisji.
-  DNS - tłumaczy adresy domen na adres IP i odwrotnie.
-  DHCP - w sposób dynamiczny konfiguruje urządzenia sieciowe, przydziela adresy IP, DNS i adres bramy domyślnej.

**2.Warstwa transportowa (transport layer)**

Korzystając z odpowiednich portów, warstwa przesyła dane i informacje do odpowiednich aplikacji. Warstwa transportowa może nawiązywać i zrywać połączenia z innymi komputerami w sieci. Warstwa ta korzysta z dwóch ważnych protokołów: są to protokół TCP, które po odebraniu danych informują o ich odebraniu, oraz protokół UDP który nie informuje o odebraniu danych. 

**3. Warstwa internetowa (internet layer)**

Jej głównym zadaniem jest dzielenie segmentów z danymi na pakiety i wysłanie ich do sieci docelowej. W tej warstwie pracuje protokół IP. Protokół IP ściśle współpracuje z protokołem TCP z warstwy transportowej. Pierwszy z nich wybiera najlepszą drogę, a drugi zapewnia bezproblemowy transport. 

Innymi ważnymi protokołami są:

- protokół ICMP - który jest używany w konsoli przez polecenia sprawdzające jakość połączenia np. polecenie ping.
- protokoły ARP i RARP - pierwszy z nich szuka adresu MAC dla znanego adresu IP, a drugi protokół odwrotnie, znajduje adres IP dla znanego adresu MAC.

W warstwie internetowej pracują także protokoły routingu np. RIP, IGRP, EIGRP, OSPF, BGP. 

**4. Warstwa dostępu do sieci (network access layer)**

W tej ostatniej warstwie dane dostarczane są do odbiorcy przez fizyczne połączenie między komputerami za pomocą np. karty sieciowej, lub modemu. Warstwa ta korzysta z protokołów służących do dynamicznego określania adresów IP. W warstwie dostępu do sieci, pracują trzy ważne protokoły, jeden z nich zapewnia dostęp do sieci w sieciach lokalnych czyli Ethernet, oraz dwa zapewniające dostęp w sieciach rozległych czyli ATM i Frame Relay. 

## IV. TCP

Transmission Control Protocol, czyli TCP, to kluczowy protokół warstwy transportowej w sieciach komputerowych. Jego główną cechą jest niezawodność transmisji danych między urządzeniami. Poprzez mechanizmy potwierdzania odbioru, numerację sekwencyjną i kontrolę przepływu, TCP gwarantuje kompletność i poprawność przesyłanych informacji. Proces "handshakingu" przed transmisją umożliwia skuteczną synchronizację. Kontrola przepływu reguluje prędkość, zapobiegając zatłoczeniu sieci. Elastyczność TCP sprawia, że jest używany w różnych kontekstach, od przeglądania stron internetowych po transfer plików. Wraz z rozwojem technologii, TCP pozostaje kluczowym elementem niezawodnej komunikacji sieciowej. 

-  Nagłówek TCP
Nagłówek TCP składa się z 20 lub więcej bajtów. Dokładna wielkość zależy od tego czy opcjonalne pole opcji (ang. options) jest używane. Maksymalna wielkość tego pola to 40 bajtów, więc maksymalna wielkość całego nagłówka to 60 bajtów.

![ALT TEXT](http://www.crypto-it.net/Images/theory/tcpip/tcp_header_pl.png)

**Zastosowanie TCP**

TCP jest szeroko wykorzystywane w protokołach i aplikacjach, które wymagają wysokiej niezawodności. Nie jest tak szybkie jak UDP, ale -jeśli skonfigurowane poprawnie- TCP zapewnia wciąż dobrą szybkość transmisji połączoną z dobrą jakością przesyłanych danych. 

## V. IP

Adres IP, czyli Internet Protocol, to unikalny identyfikator przypisany każdemu urządzeniu w sieci. Wersje IPv4 (32-bit) i IPv6 (128-bit) pozwalają na identyfikację i lokalizację urządzeń. Składają się z oktetów lub grup heksadecymalnych, oddzielonych kropkami lub dwukropkami. 

Adresy IP mogą być publiczne (dostępne w Internecie) lub prywatne (wewnątrz sieci). Wykorzystywane są w routingu danych, umożliwiając komunikację między urządzeniami. Dynamiczne przydzielanie adresów przez serwery DHCP ułatwia konfigurację. 

## VI. Zalety i Wady TCP/IP

| Zalety | Wady |
| --- | --- |
| Protokół TCP/IP jest skalowalny, co oznacza, że może obsługiwać zarówno małe, lokalne sieci, jak i ogromne globalne infrastruktury, takie jak Internet.| Podstawowa implementacja TCP/IP nie zapewnia wystarczającego bezpieczeństwa |
| TCP/IP obsługuje różne rodzaje urządzeń i aplikacji, co sprawia, że jest elastyczny w dostosowywaniu się do różnych wymagań sieciowych. | Problemy z adresacją IPv4 |
|  Protokół TCP/IP jest dobrze sprawdzony i stabilny. | Wprowadzenie nowszych wersji protokołu (np. IPv6) może rodzić wyzwania związane z kompatybilnością wsteczną |
| Jest dostępny publicznie | Overhead - potwierdzanie odbioru i kontroli przepływu, wiąże się to z stratą wydajności |



