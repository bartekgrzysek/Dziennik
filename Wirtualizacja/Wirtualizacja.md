# Wirtualizacja
## Wirtualizacja - ogólna definicja
**Wirtualizacja** to technologia pozwalająca na tworzenie wirtualnych instancji zasobów komputerowych, takich jak systemy operacyjne, serwery, pamięć czy sieci. W skrócie, umożliwia ona jednemu fizycznemu systemowi komputerowemu udostępnianie swoich zasobów w taki sposób, jakby były one osobnymi, niezależnymi jednostkami. Wirtualizacja jest szeroko stosowana w celu optymalnego wykorzystania zasobów, zwiększenia elastyczności infrastruktury IT i ułatwienia zarządzania systemami komputerowymi.

Na przykład, wirtualizacja serwera pozwala uruchomić wiele serwerów wirtualnych na jednym fizycznym serwerze. Każdy z tych serwerów wirtualnych może działać niezależnie, posiadając własny system operacyjny i aplikacje, chociaż fizycznie dzieli się zasobami z innymi serwerami wirtualnymi na tym samym sprzęcie.

![Wirtualizacja](https://www.inprox.pl/storage/uploads/news/72cf484e90c41a32b5f68dc58a2fb941.jpg)

## Zarys historyczny - początki rozwoju wirtualizacji

Wirtualizacja to kluczowa technologia w dziedzinie informatyki, umożliwiająca efektywne zarządzanie zasobami komputerowymi i optymalne wykorzystanie infrastruktury IT. Historia wirtualizacji sięga lat 60., kiedy to IBM wprowadziło koncepcję maszyn wirtualnych. Początkowo skupiała się ona na możliwości uruchamiania wielu systemów operacyjnych na jednym komputerze, co otworzyło drogę do efektywnego dzielenia zasobów.

![IBM](https://www.virtual-it.pl/grafika/art/histwirt/IBM-System-360-Model-65_operator-console.jpg) 

W latach 80. pojawiły się pierwsze produkty komercyjne, takie jak VM/370 firmy IBM, umożliwiające jednoczesne uruchamianie wielu instancji systemu operacyjnego na jednym fizycznym komputerze. Kolejne dziesięciolecia przyniosły rozwój technologii wirtualizacji na poziomie procesora, z dominacją firm takich jak Vmware, które wprowadziły produkty umożliwiające elastyczne uruchamianie różnych systemów operacyjnych na jednym sprzęcie. 

![IBM System/370](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/IBM_System_370-145_und_Bandlaufwerke_2401.png/300px-IBM_System_370-145_und_Bandlaufwerke_2401.png)

W latach 2000. wirtualizacja serwerów zyskała na znaczeniu, a Vmware stało się liderem w efektywnym dzieleniu zasobów serwerowych. Przejście do lat 2010. przyniosło powszechne zastosowanie wirtualizacji w środowiskach biznesowych, wspierane przez produkty takie jak Hyper-V od Microsoft czy KVM dla systemów opartych na jądrze Linux.

Obecnie wirtualizacja jest integralną częścią centrów danych, chmur obliczeniowych i środowisk IT.

## Rodzaje wirtualizacji

**Istnieją trzy główne rodzaje wirtualizacji:**
- Wirtualizacja sprzętowa
- Wirtualizacja pulpitu
- Wirtualizacja na poziomie systemu operacyjnego.

![Rodzaje wirtualizacji](https://main.pl/wp-content/uploads/2022/12/Wirtualizacja.png)

**Wirtualizacja sprzętowa** - Wirtualizacja sprzętowa to technologia, która umożliwia jednemu fizycznemu komputerowi, zwanej hostem, udostępnianie swoich zasobów sprzętowych do jednoczesnego uruchamiania wielu maszyn wirtualnych. W tym kontekście, maszyna wirtualna (VM) to emulowana maszyna komputerowa, która działa jako niezależny system operacyjny na wspólnym sprzęcie. Kluczowym elementem wirtualizacji sprzętowej jest hypervisor, który to oprogramowanie jest odpowiedzialne za zarządzanie maszynami wirtualnymi i alokację zasobów sprzętowych.

**Wirtualizacja pulpitu** - to technologia umożliwiająca użytkownikom zdalny dostęp do środowiska pulpitu komputerowego, niezależnie od tego, gdzie fizycznie znajduje się sprzęt komputerowy. To rozwiązanie jest szczególnie przydatne w kontekście zarządzania dostępem do aplikacji, danych i zasobów z różnych urządzeń, bez konieczności fizycznego znajdowania się przy danym komputerze.

**Przykłady wirtualizacji pulpitu:**
- Oprogramowanie TeamViewer do pomocy zdalnej
- Protokoły open source używane między innymi w systemach z rodziny Linux, takie jak VNC
- Pulpit zdalny korzystający z protokołu RDP

**Wirtualizacja na poziomie systemu operacyjnego ( wirtualizacja kontenerów)**  - umożliwia uruchamianie i izolowanie różnych aplikacji na jednym fizycznym serwerze. Izolacja kontenerów pozwala na jednoczesne działanie wielu aplikacji, zachowując jednocześnie separację i bezpieczeństwo między nimi. Kontenery współdzielą i korzystają z jądra systemu operacyjnego, który je uruchamia, co pozwala na minimalizację spadków wydajności, widocznych przy pełnej wirtualizacji.

Przykłady wykorzystania konteneryzacji to m.in. oprogramowanie **Docker** czy **Kubernetes**.

## Typy wirtualizacji

**1. Wirtualizacja typu pierwszego**

**Wirtualizacja typu pierwszego** charakteryzuje się tym, iż hipernadzorca (ang. Hypervisor), czyli program komputerowy realizujący zadania związane z wirtualizacją, pracuje bezpośrednio na sprzęcie komputera fizycznego i przydziela zasoby sprzętowe maszynom wirtualnych bez pośrednictwa systemu operacyjnego gospodarza (ang. host). Każda maszyna wirtualna w takiej technologii staje się niejako osobnym obszarem, osobnym blokiem, czasem nazywanym partycją obsługiwanym przez hypervizora, który przydziela jej zasoby.

  ![Wirtualizacja typu pierwszego](https://pasja-informatyki.pl/pliki/wirtualizacja-typ-1.png)

**Zalety wirtualizacji typu pierwszego:**
- Hypervisor bezpośredni na sprzęcie
- Bezpośredni dostęp do zasobów
- Wyższa wydajność
- Bezpośrednia kontrola nad zasobami
- Minimalny narzut systemowy

  **Przykłady hypervisorów typu pierwszego to:**
- Vmware ESXi
- Microsoft Hyper-V w trybie "bare-metal"
- KVM (Kernel-based Virtual Machine) w trybie bezpośrednim

Wirtualizacja typu pierwszego jest często stosowana w środowiskach data center, centrach danych i chmurach obliczeniowych, gdzie kluczową rolę odgrywa efektywne wykorzystanie zasobów sprzętowych i zapewnienie wydajności maszyn wirtualnych.

**2.Wirtualizacja typu drugiego**

**Wirtualizacja typu drugiego** polega na tym, że hypervisor działa w systemie operacyjnym gospodarza, czyli fizycznego komputera i poprzez system operacyjny przydziela zasoby dla maszyn wirtualnych. W oparciu o tę technologię wirtualizacji pracują programy takie jak VirtualBox, VM Player czy nieco starszy i nierozwijany już Virtual PC. Jest to po prostu aplikacja instalowana na systemie operacyjnym pozwalająca na tworzenie maszyn w jej obszarze.

![Wirtualizacja typu drugiego](https://pasja-informatyki.pl/pliki/wirtualizacja-typ-2.png)

**Zalety wirtualizacji typu drugiego:**
- Pełny system operacyjny hosta
- Elastyczność i łatwość instalacji
- Środowisko deweloperskie
- Dostępność dla użytkowników indywidualnych
- Małe koszty i łatwa dostępność

**Przykłady hypervisorów typu drugiego:**
- Oracle VirtualBox
- VMware Workstation
- Microsoft Hyper-V w trybie hostowanym

## Co można wirtualizować ?
- Aplikacje
- Systemy operacyjne
- Sieci komputerowe
- Pamięci masowe
- Maszyny wirtualne
- Serwery
- Kontenery
- Usługi ( WWW, bazy danych, aplikacje serwerowe)

## Wirtualizacja - Zalety - Wady

| **ZALETY** | **WADY** |
| --- | --- |
| Efektywne wykorzystanie zasobów | Złożoność zarządzania |
| Izolacja | Wydajność aplikacji czasu rzeczywistego |
| Szybkie wdrażanie i testowanie | Zależność od hypervisora |
| Oszczędność kosztów energetycznych | Ograniczenia na poziomie sprzętu |
| Zarządzanie zasobami ( Hypervisory) | Złożoność odzyskiwania po awarii |

*Poniżej przedstawiono filmik, w którym dokładnie przedstawiono plusy i minusy wirtualizacji.*

[![Plusy i minusy Wirtualizacji](https://www.youtube.com/watch?v=ni8ZOlUP4Ws)]

## Zastosowanie - czyli, kiedy nam przydaje się wirtualizacja

Jednym z kluczowych obszarów zastosowania wirtualizacji jest efektywne wykorzystanie centrum danych i chmury obliczeniowej. Wirtualizacja umożliwia konsolidację serwerów, co prowadzi do zwiększenia efektywności energetycznej, oszczędności kosztów operacyjnych i lepszego zarządzania zasobami. W kontekście rozwoju oprogramowania, wirtualizacja pozwala programistom na szybkie tworzenie i testowanie różnych konfiguracji systemów operacyjnych i środowisk, co skraca cykle rozwoju i ułatwia poprawki błędów. To także narzędzie używane w celu przenoszenia aplikacji między różnymi środowiskami. Wirtualizacja pulpitów, znana również jako VDI, umożliwia zdalny dostęp do środowiska pulpitu komputerowego, co jest szczególnie ważne w dobie elastycznych modeli pracy i mobilności zawodowej. W obszarze bezpieczeństwa, izolacja maszyn wirtualnych przyczynia się do zwiększenia bezpieczeństwa, ponieważ problemy w jednej maszynie nie przenoszą się na pozostałe, co minimalizuje ryzyko ataków. Wirtualizacja jest również kluczowym elementem rozwiązań związanych z odzyskiwaniem po awarii. Dzięki możliwości przenoszenia maszyn wirtualnych między różnymi serwerami, organizacje mogą szybko przywrócić działanie systemów po wystąpieniu awarii.

## Bezpieczeństwo w Wirtualizacji

Bezpieczeństwo w wirtualizacji stanowi kluczowy obszar z uwagi na izolację różnych środowisk, a także potencjalne zagrożenia wynikające z dostępu do współdzielonych zasobów. Oto kilka aspektów bezpieczeństwa wirtualizacji:
- **Izolacja Maszyn Wirtualnych (VMs):** Jednym z kluczowych elementów jest skuteczna izolacja między maszynami wirtualnymi. To zapobiega przenoszeniu zagrożeń z jednej maszyny na drugą.
- **Bezpieczeństwo Hypervisora:** Bezpieczeństwo samego hypervisora (warstwy wirtualizacyjnej) jest kluczowe. Ataki na hypervizor mogą prowadzić do kompromitacji wszystkich maszyn wirtualnych działających na danej platformie.
- **Zarządzanie Dostępem:** Kontrola dostępu do zarządzania wirtualizacją jest ważna. Ograniczenie uprawnień administratorów do konkretnych funkcji może zminimalizować potencjalne zagrożenia.
- **Monitorowanie Aktywności:** Regularne monitorowanie aktywności maszyn wirtualnych, dostępu do hypervizora oraz ruchu sieciowego pozwala na wczesne wykrywanie potencjalnych ataków.
- **Aktualizacje i Łatki:** Regularne stosowanie aktualizacji i łatek zarówno dla hypervizora, jak i systemów operacyjnych gości jest kluczowe dla zminimalizowania ryzyka związanego z lukami w zabezpieczeniach.
- **Bezpieczeństwo Sieciowe:** Skonfigurowanie bezpiecznych polityk sieciowych, zastosowanie firewalli wewnątrz i na zewnątrz maszyn wirtualnych, a także monitorowanie ruchu sieciowego to kluczowe aspekty bezpieczeństwa.

## Różnica między wirtualizacją a parawirtualizacją

1. Czym jest parawirtualizacja ?

Parawirtualizacja to technika wirtualizacji, która zapewnia interfejs dla maszyn wirtualnych, które są podobne do ich podstawowego sprzętu. W parawirtualizacji system operacyjny gościa jest jawnie przenoszony przed instalacją maszyny wirtualnej, ponieważ nie dostosowany system operacyjny gościa nie może działać na monitorze maszyny wirtualnej (VMM).

**Główne cechy parawirtualizacji:**
- modyfikowanie kodu źródłowego gościa
- interakcja z Hypervisorem
- wydajność
- współdzielenie ressursów

**RÓŻNICA MIĘDZY WIRTUALIZACJĄ A PARAWIRTUALIZACJĄ

|Wirtualizacja | Parawirtualizacja |
| --- | --- |
|System operacyjny gościa nieświadomie działa w wirtualnym środowisku. | System operacyjny gościa jest dostosowany do współpracy z hypervisorem |
| Możliwa do użycia bez potrzeby modyfikacji systemu operacyjnego gościa. | Wymaga dostosowania systemu operacyjnego gościa |
| W związku z koniecznością emulacji nieobsługiwanych instrukcji, mogą wystąpić dodatkowe luki bezpieczeństwa. | W związku z bezpośrednią komunikacją, istnieje mniejsze ryzyko dodatkowych luk bezpieczeństwa. |
| Hypervisor tłumaczy lub emuluje niektóre instrukcje procesora. | Hypervisor nie emuluje nieobsługiwanych instrukcji |

## Przykładowe programy do wirtualizacji

**Programy służące do wirtualizacji:**

*1.VMware Workstation/Player*

VMware Workstation to zaawansowane oprogramowanie do wirtualizacji dla profesjonalistów, umożliwiające jednoczesne uruchamianie wielu maszyn wirtualnych na jednym komputerze. Oferuje zaawansowane opcje konfiguracyjne, możliwość tworzenia snapshotów i integrację z chmurą VMware.

VMware Player to darmowa wersja VMware Workstation, przeznaczona głównie do użytku osobistego. Posiada prosty interfejs użytkownika i umożliwia uruchamianie maszyn wirtualnych stworzonych w innych platformach wirtualizacyjnych, ale ma ograniczone funkcje zaawansowane w porównaniu do wersji komercyjnej.

*2.Microsoft Hyper-V*

Hyper-V to wbudowany w systemy Windows hipernadzorca do wirtualizacji, umożliwiający uruchamianie wielu maszyn wirtualnych z różnymi systemami operacyjnymi na jednym fizycznym serwerze. Działa na bazie wirtualizacji sprzętowej, oferuje migrację maszyn wirtualnych, elastyczną konfigurację i jest dostępny bezpłatnie w systemach Windows Server oraz niektórych edycjach Windows 10.

*3.Oracle VirtualBox*

Oracle VirtualBox to darmowe i otwarte oprogramowanie do wirtualizacji, umożliwiające uruchamianie różnych systemów operacyjnych na jednym komputerze. Posiada intuicyjny interfejs, obsługuje snapshoty, oferuje wsparcie dla wielu systemów operacyjnych gości i jest dostępny bezpłatnie zarówno do użytku osobistego, jak i komercyjnego.

*4.KVM*

Kernel-based Virtual Machine (KVM) to rozszerzenie jądra Linux umożliwiające wirtualizację sprzętową. Działa jako moduł jądra, umożliwiając uruchamianie maszyn wirtualnych na platformie Linux. KVM jest darmowy, open-source i efektywny, wykorzystując funkcje wirtualizacji procesora.

*5.XEN*

Xen to hipernadzorca wirtualizacji, który umożliwia uruchamianie wielu systemów operacyjnych na jednym fizycznym serwerze. Jest darmowy, open-source i stosuje technikę parawirtualizacji, gdzie goście są dostosowane do współpracy z hypervisorem. Xen jest często używany w centrum danych i chmurach obliczeniowych do efektywnego zarządzania zasobami i izolacji maszyn wirtualnych.

## Czym jest emulacja ?

**Emulacja - definicja**

Emulacja to proces, w którym jeden system (najczęściej komputerowy lub urządzenie) imituje zachowanie innego systemu, najczęściej za pomocą oprogramowania. Głównym celem emulacji jest umożliwienie jednemu systemowi, znanemu jako emulator, na udawanie działania innego systemu, nazywanego emulowanym. Emulatory są często używane w kontekście gier komputerowych, platform wirtualizacyjnych, czy też do symulacji urządzeń.

W skrócie, emulacja pozwala na działanie oprogramowania stworzonego dla jednego systemu na innym, często inaczej zbudowanym lub przeznaczonym na różne cele. Oprogramowanie emulacyjne tłumaczy instrukcje i funkcje jednego systemu na zrozumiałe dla drugiego, umożliwiając imitację jego działania.

## Jak będzie wyglądała wirtualizacja w przyszłości ?

Wirtualizacja w przyszłości prawdopodobnie będzie rozwijana w kilku kierunkach, wprowadzając nowe technologie i dostosowując się do zmieniających się potrzeb. Oto kilka prognoz dotyczących tego, jak mogłaby wyglądać wirtualizacja w przyszłości:

- Zintegrowane Środowiska Wirtualizacyjne
- Wirtualizacja Krawędzi (Edge Virtualization)
- Wirtualizacja GPU
- Efektywniejsza Wirtualizacja Kontenerów
- Automatyzacja i Sztuczna Inteligencja w Zarządzaniu Zasobami
- Bezpieczeństwo Wirtualizacji



