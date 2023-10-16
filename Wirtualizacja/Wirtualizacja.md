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

[![Watch the video](https://www.youtube.com/watch?v=ni8ZOlUP4Ws/<VIDEO_ID>]

