# Protokół IPv6
## I. Definicja

IPv6 (Internet Protocol version 6) to zaawansowany protokół internetowy, który umożliwia przesyłanie danych w sieciach komunikacyjnych. Stanowi rozwinięcie poprzedniej wersji protokołu, IPv4 i został stworzony w celu zaspokojenia rosnących potrzeb adresowych oraz zapewnienia lepszej wydajności, bezpieczeństwa i rozszerzalności systemów telekomunikacyjnych. 

W przeciwieństwie do IPv4, który używał 32-bitowych adresów IP, IPv6 korzysta z 128-bitowych adresów IP, co pozwala na znacznie większą przestrzeń adresową. Dzięki temu można przypisać o wiele więcej unikalnych adresów IP dla różnych urządzeń w sieci, co jest niezbędne w erze rozwoju urządzeń internetu rzeczy (IoT) oraz dla zapewnienia stałego dostępu do sieci dla rosnącej liczby użytkowników. 

IPv6 wprowadza również kilka innych udoskonaleń w stosunku do poprzedniej wersji protokołu. Zapewnia lepsze mechanizmy kontroli i zabezpieczeń, w tym obsługę automatycznego konfigurowania adresów IP, a także uwierzytelnianie, szyfrowanie i integralność danych. Wprowadza również wsparcie dla jakości obsługi (QoS), co jest niezwykle ważne dla usług strumieniowych, wideo HD, gier online i innych aplikacji wymagających wysokiej przepustowości. 

## II. Budowa adresu IPv6

Adresy IPv6 są reprezentowane w formie 128-bitowych ciągów heksadecymalnych, co sprawia, że są one zdecydowanie dłuższe niż adresy IPv4. Ta długa sekwencja bitów umożliwia stworzenie ogromnej przestrzeni adresowej, co stanowi kluczową różnicę w porównaniu do starszej wersji, IPv4. Adres IPv6 składa się z 8 grup, a każda z nich zawiera 16 bitów, co daje łącznie 128 bitów. Te grupy są zazwyczaj zapisywane w formie heksadecymalnej, oddzielane dwukropkami. Przykładowy adres IPv6 to: 2001:0db8:85a3:0000:0000:8a2e: 0370:7334. Aby uprościć zapis, istnieje notacja skrócona. Możemy pominąć wiodące zera w każdej grupie, a także skompresować grupy składające się tylko z zer. Na przykład, poprzedni adres można zapisać skrócenie jako: 2001:db8:85a3::8a2e:370:7334. 

Znaczenie każdej grupy: 

Pierwsze 64 Bity: Pierwsze 64 bity są zwykle przeznaczone na identyfikację podsieci, a pozostałe 64 bity na identyfikację hosta w danej podsieci. 

## III. Adresy specjalne

- **: :/128** – adres nieokreślony 
(odpowiednik 0.0.0.0 w IPv4)
- **: :1/128** – loopback, adres wskazujący na host lokalny. 
(odpowiednik 127.0.0.1 w ipv4), 
- **: :ffff: 0:0/64** – pula zarezerwowana dla zachowania kompatybilności z protokołem IPv4 pozwalająca wykorzystywać komunikację według protokołu IPv6 w sieci IPv4 (np.: :ffff:192.0.2.128),
- **2002: :/24** – adresy typu 6to4. (Są to adresy wygenerowane na podstawie istniejących, publicznych adresów IPv4, dostępne dla każdego użytkownika.),
- **2001:7f8: :/32** – pula zarezerwowana dla punktów IPX, każdy z nich dostaje jedną podsieć /48,
- **2001:db8: :/32** – pula wykorzystywana w przykładach i dokumentacji – nigdy nie będzie wykorzystywana produkcyjnie,
- **c00: :/7** – pula lokalnych unikatowych adresów IPv6 typu unicast (odpowiednik adresów prywatnych IPv4),
- **ff00: :/8** – pula używana do komunikacji multicast.

 ## IV. Wady i zalety IPv6

 | Zalety | Wady |
 | --- | --- |
 | Ogromna Przestrzeń Adresowa | Złożoność Konfiguracji |
 | Poprawione Bezpieczeństwo | Koszty Migracji |
 | Efektywność | Utrudnione zarządzenie adresami |
 | Automatyczna konfiguracja adresów | Problemy związane z adresem NAT |
 | Współpraca z nowoczesnymi aplikacjami | - |

 ## V. Różnica między IPv4 a IPv6

 | IPv4 | IPv6 |
 | --- | --- |
 | Oferuje jedynie 32 bity, co przekłada się na około 4,3 miliarda unikalnych adresów. | Znacznie większa przestrzeń adresowa, 128 bitów, co generuje około 3,4 × 10^38 unikalnych adresów. |
 | Konfiguracja adresów może być ręczna lub dynamiczna (DHCP). | Wprowadza Stateless Address Autoconfiguration (SLAAC) dla automatycznej konfiguracji adresów. |
 | Bezpieczeństwo nie jest wbudowane; musi być dodawane przez zewnętrzne protokoły, takie jak IPsec. | Wprowadza wbudowane wsparcie dla IPsec, co zwiększa bezpieczeństwo komunikacji w sieci. |
 | Adresy są zapisywane w formie czterech dziesiętnych bloków, oddzielonych kropkami (np. 192.168.0.1). | Adresy są reprezentowane jako ósemkowe bloki heksadecymalne, oddzielone dwukropkami (np. 2001:0db8:85a3::8a2e:0370:7334) |
 | Jest powszechnie używane, ale dostępne adresy zaczynają się wyczerpywać. | Projektowane z myślą o przyszłości, aby zaspokoić rosnące zapotrzebowanie na adresy. |
 | Wykorzystuje broadcast do wysyłania komunikatów do wszystkich urządzeń w danej sieci. | Zamiast broadcast, IPv6 preferuje multicast, co jest bardziej efektywne i elastyczne. |

## VI. Podsumowanie

IPv6 to nie tylko kolejna wersja protokołu internetowego, to ewolucja, która kształtuje przyszłość sieci. Z jego ogromną przestrzenią adresową, bezpieczeństwem wbudowanym i elastycznymi funkcjami konfiguracyjnymi, IPv6 odgrywa kluczową rolę w przekształcaniu sposobu, w jaki postrzegamy, korzystamy i rozwijamy Internet. Mimo wyzwań związanych z migracją, korzyści płynące z wdrożenia IPv6 są niezaprzeczalne, stanowiąc fundament dla innowacji i rozwoju w erze cyfrowej. 
