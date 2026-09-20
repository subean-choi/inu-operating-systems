# 운영체제

### ✏️ 수업시간 필기
		- 1주차 (3/5)
		- 2주차 (3/11)
		- 2주차 (3/12 보강)
		- 4주차
		- 4주차 - 2
		- 5주차
		- 6주차
		- 7주차
	
	
		### 💻 실습 파일
		- 어셈블리 자료 첫번째
			[attached course file]
		- 어셈블리 자료 두번째
			[attached course file]
				

- 11주차 
- 11주차 - 2
- 13주차
- 14주차
---
### 요약본
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]
[attached course file]

---

# 1️⃣ 1주차 (3/5)

# Computer System Structure
Computer system can be divided into four components:
	### 1. Hardware 
	### 2. Operating system
	### 3. Application programs
	### 4. Users
	### 5. Network
# Abstract View of Components of Computer
[image omitted: personal or temporary Notion asset]
▶️ application이 직접적으로 hardware에 접근하지 못하고 중간에 operating system을 통하여 접근할 수 있다.
# What is an Operating System?
→ A program that acts as an intermediary <span color="yellow_bg">between a user of a computer and the computer hardware</span>
→ Operating system goals:
	1) Execute user programs and make solving user problems easier.
	2) Make the computer system convenient to use.
	3) Use the computer hardware in an efficient manner.
> # 운영 체제란?
	→ <span color="yellow_bg">컴퓨터 사용자와 컴퓨터 하드웨어 간의 중개 역할을 하는 프로그램</span>
	→ 운영 체제 목표:
		1) 사용자 프로그램을 실행하고 사용자 문제를 더 쉽게 해결할 수 있습니다.
		2) 컴퓨터 시스템을 편리하게 사용할 수 있도록 합니다.
		3) 컴퓨터 하드웨어를 효율적으로 사용합니다
# What Operating Systems Do
= OS가 대상으로 삼아야 할 관점/환경 들
	→ Depends on the point of view
	→ User want convenience , ease of use and good performance 
		- Don’t care about resource utillzation
	→ But shared computer such as mainframe or server conputer must keep all users happy
		- Operating system is a resource allocator and control program making dffcient use of HW and managing execution of user programs
	→ User of dedicate system such as workstations have dedicated resources but frequently use shared resources from servers
	→ Mobile devices like smartphones and tablet are resources poor, optimized for usability and battery life.
		- Mobile user interfaces such as touch screens, voice recognition
	→ Some computer have no user interface, such as embedded computers in devices 
	> # 운영 체제가 하는 일
	= = OS가 대상으로 삼아야 할 관점/환경 들
		→ 시점에 따라 다름
		→ 사용자는 편리함, 사용 편의성 및 우수한 성능을 원합니다
			- 리소스 활용에 신경 쓰지 않음
		→ 그러나 메인프레임 또는 서버 컴퓨터와 같은 공유 컴퓨터는 모든 사용자를 행복하게 유지해야 합니다
			- 운영체제는 HW를 효율적으로 사용하고 사용자 프로그램의 실행을 관리하는 자원 할당자 및 제어 프로그램입니다
		→ 워크스테이션과 같은 전용 시스템의 사용자는 전용 리소스가 있지만 서버의 공유 리소스를 자주 사용합니다
		→ 스마트폰과 태블릿과 같은 모바일 장치는 사용성과 배터리 수명에 최적화된 자원이 부족합니다.
			- 터치 스크린, 음성 인식과 같은 모바일 사용자 인터페이스
		→ 장치에 내장된 컴퓨터와 같은 일부 컴퓨터에는 사용자 인터페이스가 없습니다
# OS를 다시 한번 정의해보자면,
### Recource allocator 
### Control program
### Kernel
# Operating system Definitions
→ No universally accepted definition
→ “Everything a  vendor ships when you order an operating system” is a good approximation 
	- But varies wildly
→ “The one program running at all times on the computer” is the kernel, part of the operating system
→ Everything else is either
	- a system program(ships with the operating system, but not part of the kernel), or 
	- an application program, all programs not associated with the operating system
→ Today’s OSes for general purpose and mobile computing also include middleware 
	- a set of software frameworks that provide addition services to application developers such as databases, media, graphics
	> # 운영 체제 정의
	→ 보편적으로 인정되는 정의가 없습니다
	→ "운영 체제를 주문할 때 공급업체가 배송하는 모든 것"은 적절한 근사치입니다
		- 하지만 천차만별입니다
	→ "컴퓨터에서 항상 실행되는 하나의 프로그램"은 운영 체제의 일부인 커널입니다
	→ 다른 것들도 다
		- 시스템 프로그램(운영 체제와 함께 제공되지만 커널의 일부는 제공되지 않음) 또는
		- 응용 프로그램, 운영 체제와 연결되지 않은 모든 프로그램
	→ 오늘날의 범용 및 모바일 컴퓨팅용 OS에는 미들웨어도 포함됩니다
		- 데이터베이스, 미디어, 그래픽과 같은 애플리케이션 개발자에게 부가 서비스를 제공하는 소프트웨어 프레임워크 세트
# Computer Systme Organization
### Computer-system operation
→ One or more CPUs, device controllers connect through common bus providing access to shared memory
→ Concurrent execution of CPUs and devices computing for memory cycles
> # 컴퓨터 시스템 조직
	### 컴퓨터-시스템 운영
	→ 공유 메모리에 대한 액세스를 제공하는 하나 이상의 CPU, 장치 컨트롤러가 공통 버스를 통해 연결됩니다
	→ 메모리 사이클을 위한 CPU와 디바이스 컴퓨팅의 동시 실행
[image omitted: personal or temporary Notion asset]
# Computer-System Operation
→ I/O devices and the CPU can execute <span color="red">concurrently</span>
→ Each device controller is in charge of a particular device type
→ Each device controller has a local buffer
→ Each device controller type has an operating system <span color="blue">device driver</span> to manage it
→ CPU moves data from/to main memory to/from local buffers
→ I/O is from/to the device to/from local buffer of controller
→ Device controller informs CPU that it has finished its operation by causing an <span color="blue">interrupt.</span>
> # 컴퓨터-시스템 작동
	→ I/O 장치와 CPU가 <span color="red">동시에</span> 실행할 수 있습니다
		→ 각 장치 컨트롤러는 특정 장치 유형을 담당합니다
	→ 각 장치 컨트롤러에는 로컬 버퍼가 있습니다
	→ 각 장치 컨트롤러 유형에는 이를 관리하기 위한 운영 체제 <span color="blue">장치 드라이버</span>가 있습니다
		→ CPU가 데이터를 메인 메모리에서 로컬 버퍼로 이동합니다
	→ I/O는 컨트롤러의 로컬 버퍼에서 디바이스로/또는 디바이스로/로
	→ 장치 컨트롤러는 CPU에 <span color="blue">인터럽트</span>를 발생시켜 동작을 완료했음을 알려줍니다.
# Common Functions of Interrupts
→ Interrput transfers control to the interrupt service routione generally, through the interrupt vector, which contains the addresses of all the service routines
→ Intterupt architecture must save the address of the interrupted instruction
→ A trap or exception is a software-generated interrupt caused either by an error or a user request
→ An operating system is interrupt driven.
> # 인터럽트의 공통 기능
	→ 인터럽트는 일반적으로 인터럽트 벡터를 통해 모든 서비스 루틴의 주소를 포함하는 인터럽트 서비스 루틴에 제어권을 전달합니다
	→ 인터럽트 아키텍처는 중단된 명령어의 주소를 저장해야 합니다
	→ 트랩 또는 예외는 오류 또는 사용자 요청으로 인해 발생하는 소프트웨어에서 생성된 인터럽트입니다
	→ 운영 체제는 인터럽트 구동됩니다.
# Interrupt Timeline
[image omitted: personal or temporary Notion asset]

---

# 2️⃣ 2주차 (3/11)

# Storage Structure
- Main memort - only large storage media that the CPU can access directly
	- Random access
	- Typically volatile
	- Typically random-access memory in the form of Dynamic Random- access Memory(DRAM)
- Secondary storage - extension of main memory that provides large nonvolatiles storage capacity
- Hard Disk Drives (HDD) - rigid metal or glass platters covered with magnetic recording material
	- Disk surface is logically divided into tracks, which are subdivided into sectors 
	- The dis controller determines the logical interaction between the device and the computer
- Non-volatile memory(NVM) devices - faster than hard disks, nonvolatile (SATA → NVMe, SSD)
	- Various technologies
	- Becoming more popular as capacity and performance increases, price drops
	> # 저장 구조
	- 메인 메모장 - CPU가 직접 액세스할 수 있는 대용량 저장 매체만 해당
		- 랜덤 액세스
		- 일반적으로 휘발성입니다
		- 일반적으로 DRAM(Dynamic Random-access Memory) 형태의 랜덤 액세스 메모리
	- 2차 저장 - 대용량 비휘발성 저장 용량을 제공하는 메인 메모리 확장
	- 하드 디스크 드라이브(HDD) - 자기 기록 재료로 덮인 단단한 금속 또는 유리 플래터
		- 디스크 표면은 논리적으로 트랙으로 나뉘며 섹터로 세분화됩니다
		- 디스컨트롤러는 장치와 컴퓨터 사이의 논리적 상호작용을 결정합니다
	- 비휘발성 메모리(NVM) 장치 - 하드 디스크보다 빠른 비휘발성(SATA → NVMe, SSD)
		- 각종 기술
		- 용량과 성능이 증가함에 따라 인기가 높아짐에 따라 가격이 하락함
# Storage Hierarchy
[image omitted: personal or temporary Notion asset]
⭐ 위로 올라갈수록 빠르면서 휘발성을 띄고 있다.
⭐ 레지스터는 엄청 빠르며 cpu 안에 있다
⭐ cache는 cpu안에 있는 cache와 밖에 있는 cache로 나뉜다 
	메모리에서 cpu로 넘길 때 잠깐 보관해주는 곳
⭐ nonvolatile memory = RAM
⭐ magnetic tapes  아직 까지 사용 이유 - 오랫동안 사용할 수 있으며 가격이 싸다
# Caching
- Important principle, performed at many levels in a computer (in hardware, operating system, software)
- Information in use copied from slower to faster storage temporarily
- Faster storage(cache) checked first to determine if information is there
	- if it is, information used directly from the cache (fast)
	- if not, data copied to cache and used there
- Cache smaller than storage being cached
	- Cache management inportant design probelm
	- Cache size and replacement policy
> #캐싱
	- 컴퓨터의 여러 수준에서 수행되는 중요한 원리(하드웨어, 운영 체제, 소프트웨어)
	- 사용 중인 정보가 더 느린 스토리지에서 더 빠른 스토리지로 일시적으로 복사됨
	- 정보가 있는지 확인하기 위해 먼저 빠른 스토리지(캐시) 확인
		- 만약 그렇다면, 캐시에서 직접 사용되는 정보(빠른)
		- 그렇지 않은 경우 데이터를 캐시에 복사하여 캐시에 사용합니다
	- 캐시 중인 스토리지보다 작은 캐시
		- 캐시 관리 중요 설계 문제
		- 캐시 크기 및 교체 정책
# How a Modern Computer Works
[image omitted: personal or temporary Notion asset]
- A Von Neumann architecture
	= 프로그램과 데이터를 똑같이 취급하고(같은 버스) 처리는 순차적으로 한다. 메모리에 넣고 불러내는 프로그램에 따라 하는 일이 달라지게 된다. 프로그램 중심의 컴퓨터 구조. 현대의 기본적인 컴퓨터 형태 그 밖의 모든 가능한 형태 비노이만형 컴퓨터
	- DMA - CPU가 관여하지 않고 데이터를 주고 받음. (cpu가 일을 할 때는 dma와 메모리가 주고받는 것을 멈춘다)
# Computer System Architecture
- Most systems use a <span color="red">single general-purpose processor</span>
	- Most systems have special-purpose processors as well
- Multiprocessors systmes growing in use and importance 
	- Also known as parallel systems, tightly-coupled systems
	- Advantages include:
		1. Increased throughtput
		2. Economy of scale
		3. Increased reliability - graceful degradation or fault tolerance
	- Two types
		1. Asymmetric Multiprocessing - each processor is assigned a specific task
		2. Symmetric Multiprocessing - each porcessor performs al tasks
		> # 컴퓨터 시스템 아키텍처
	- 대부분의 시스템은 단일 범용 프로세서를 사용합니다
		- 대부분의 시스템에는 특수 목적 프로세서도 있습니다
	- 사용 및 중요도가 증가하는 멀티프로세서 시스템
		- 병렬 시스템, 긴밀하게 결합된 시스템으로도 알려져 있습니다
		- 이점은 다음과 같습니다:
			1. 처리량 증가
			2. 규모의 경제
			3. 신뢰성 향상 - 우아한 성능 저하 또는 내결함성
		- 2종류
			1. 비대칭 다중 처리 - 각 프로세서에 특정 작업이 할당됩니다
			2. 대칭 다중 처리 - 각 포서가 작업을 수행합니다
# Symmeric Multiprocessing Architecture
[image omitted: personal or temporary Notion asset]
⭐ 위의 그림은 2개의 CPU가 모든 일을 나눠서 함 
	메인 메모리(버스)를 공유해서 사용함. 버스 사용 경쟁. 비효율의 가능성
	→ 길은 여러 개이지만 대상은 하나이기에  <span color="yellow_bg">병목현상</span>이 생길 수 있음
		# A Dual-Core Design
- Multi-chip and multicore
- Systems containing all chips
	- Chassis containing multiple separate systems
> #듀얼 코어 디자인
	- 멀티칩 및 멀티코어
	- 모든 칩을 포함하는 시스템
		- 여러 개의 개별 시스템이 포함된 섀시
[image omitted: personal or temporary Notion asset]
⭐ cache에 main memory 안에 있는 것을 많이 넣어 놓으면 버스를 없앨 수 있으며 main memory가 부담이 덜 갈 수 있다.
# Non-Uniform Memory Access System
[image omitted: personal or temporary Notion asset]
⭐ 내가 하는 일은 빠르지만 남의 것을 가져올 수는 있도록 하는 것이 앞에서 이야기 했던 몇몇 문제를 개선하는 노력이 될 수 있다.
# Clustered Systems
- Link multiprocessor systmes, but multiple systems working together
	- Usually sharing storage via a storage-area network(SAN)
	- Provides a high-availability service which survives failures
		- Asymmeric clustering has one machine in hot-standby mode
		- Symmetric clustering has multiple nodes running applications, monitoring each other
	- Som clusters are for high-performance computing(HPC)
		- Applications must be written to use parallelization
> #클러스터된 시스템
	- 다중 프로세서 시스템을 연결하지만 여러 시스템이 함께 작동합니다
		- 일반적으로 SAN(Storage-Area Network)을 통해 스토리지를 공유합니다
		- 장애에도 끄떡없는 고가용성 서비스를 제공합니다
			- 대칭 클러스터링에 핫 스탠바이 모드의 시스템이 하나 있습니다
			- 대칭 클러스터링은 여러 노드가 애플리케이션을 실행하고 서로를 모니터링합니다
		- 일부 클러스터는 고성능 컴퓨팅(HPC)용입니다
			- 병렬화를 사용하려면 응용 프로그램을 작성해야 합니다
[image omitted: personal or temporary Notion asset]

---

# 2️⃣ 2주차 (3/12 보강)

# Operating-System Operations
- Bootstrap program - simple code to initialize the system, load the kernel
- Kernel loads
- Starts system daemons(services provided outside of the kernel)
- Kernel interrupt driven(hardware and software)
	- Hardware interrupt by one of the devices
	- Software interrupt (execption or trap)
		- software error(e.g., division by zero)
		- Request for operating system service -system call
		- Other process problems include infinite loop, proccesses modifying each other or the operating system
# Multiprogramming and Multitasking
- <span color="blue">Multiprogramming (Batch system)</span> needed for effciency 
	- Single user cannot keep CPU and I/O devices busy at all times
	- Multiprogramming organizes jobs(code and data) so CPU always has one to execute
	- A subset of total jobs in system is kept in memory
	- One job selected and run via <span color="blue">job schuduling</span>
	- When is has to wait (for I/O for example), OS switches to another job
	- <span color="blue">Timesharing(multitasking) </span>is logical extension in which CPU switches jobs so frequenfly that users can interact with each job while it is running, creating <span color="blue">interactive </span>computing
	- <span color="blue">Response time</span> should be \<1 second
	- Each user has at least one program executing in memory → <span color="blue">Process</span>
	- If several jobs ready to run at the same time →<span color="blue"> CPU scheduling</span>
	- If processes don’t fit in memory, <span color="blue">swapping </span>moves them in and out to run
	- <span color="blue">Virtual memory </span>allows execution of processes not completely in memory
	# Memory Layout for Multiprogrammed System
[image omitted: personal or temporary Notion asset]
# Dual-mode and Multimode Operation
- <span color="blue">Dual-mode</span> operation allows OS to protect itself and other system components
	- <span color="blue">User mode</span> and <span color="blue">kernel mode</span>
	- <span color="blue">Mode bit</span> provided by hardware
		- Probvides ability to distinguish when system is running user code or kernel code
		- Some instructions designated as <span color="blue">privileged</span>, Only executable in kernel mode
		- System call changes mode to kernel, return from call resets it to user
- Increasingly CPUs support multi-mode operations 
	- i.e<span color="blue">. virtual machine manager(VMM)</span> mode for guest <span color="blue">VMs</span>
# Transition from User to Kernel Mode
- Timer to prevent infinite loop/ process hogging resoures 
	- Set interrupy after sepcific period
	- Operating system decrements counter
	- When counter zero generate an interrupt
	- Set up before scheuling process to regain control or terminate program that exceeds allotted time
	[image omitted: personal or temporary Notion asset]
	# Process Management
- A process is a program in execution. It is a unit of work within the system. Program is a passive entity, process is an active entity.
- Process needs resources to accomplish its task 
	- CPU, memory, I/O/ ,files
	- Intialization data
- Process termination requires reclaim of any reusable resources
- Single-threaded process has one program counter specifying location instructions sequentially, one at a time, until completion
- Multi-threaded process has one program counter per thread Typically system has many processes, some user, some operating system running concurrently on one or more CPUs
	- Concurrency by multiplexing the CPUs among the proccesses threads
# Process Management Activites
The operating system is responsible for the following activites in connection with process management:
	- Creating and deleting both user and system processes
	- Suspending and resuming processes
	- Providing mechanisms for process synchronization
	- Providing mechanisms for process communication
	- Providing mechanisms for deadlock handling
# Memory Management
- To execute a program all (or part) of the instructions must be in memory
- All (or part) of the data that is needed by the program must be in memory
- Memory management determines what is in memory and when
	- Optimizing CPU utilization and computer response to users
- Memory management activities
	- Keeping track of which parts of memory are currently being used and by whom
	- Deciding which processes (or parts thereof) and data to move into and out of memory
	- Allocating and deallocating memory space as needed
# File-system Management
- OS provides uniform, logical view of information storage
	- Abstract physical properties to logical storage unit - file
	- Each medium is controlled by device (i,e., disk drive, tape drive)
		- Varying properties include access speed, capacity, data-transfer rate, access method(sequential or random)
- File - System management
	- file usually organized into directories
	- Access control on most systems to determine who can access what
	- OS activites include
		- Creating and deleting files and directories
		- Primitives to manipulate files and directories
		- Mapping files onto secondary storage
		- Backup files onto stable (non-volatile) storage media
# Mass-Storage Management
- Usually disks used to store data that does not fit in main memory or data that must be kept for a “Long” period of time
- Proper management is of central importance
- Entire speed of computer operation hinges on disk subsystem and its algorithms
- OS activities
	- Mounting and ummounting
	- Free-space management
	- Storage allocation
	- Disk scheduling
	- Partitioning
	- Protection
- Some storage need not be fast
	- Tertiary storage includes optical storage, magnetic tape
	- Still must be managed - by OS or applications
# Characteristics of Various Types of Storage
[image omitted: personal or temporary Notion asset]
▶️ Movement between levels of storage hierarchy can be explicit or implicit
# Migration of data “A” from Disk to Register
- Multitasking environments must be careful to use most recent value, no matter where it is stored in the storage hierarchy
[image omitted: personal or temporary Notion asset]
- Multiprocessor environment must provide cache coherency in hardware such that all CPUs have the most recent value in their cache
- Distributed environment situation even more complex
	- Several copies of a datum can exist
	- Various solutions covered in Chapter 19
# I/O Subsystem
- One purpose of OS is to hide peculiarities of hardware devices from the user
- I/O subsystem responsible for
	- Memory management of I/O including buffering (storing data temporarily while it is being transferred), caching (storing parts of data in faster storage for performance), spooling (the overlapping of output of one job with input for other jobs) 
	- General device-driver interface
	- Drivers for specific hardware devices
# Protection and Security
### Protection
- any mechanism for controlling access of processes or user to resources defined by the OS
### Security 
- defense of the system against internal and external attacks
	- Huge range, including denial-of-service, worms, viruses, identity theft, theft of service
### Systems generally first distinguish among users, to determine who can do what
- User identities (user IDs, security IDs) include name and associated number, one per user
- User ID then associated with all files, processes of that user to determine access control
- Group identifier (group ID) allows set of users to be defined and controls managed, then also associated with each process, file
- Privilege escalation allows user to change to effective ID with more right
# Computing Environment
## computing environments - Traditional
- Stand-alone general purpose machines
- But blurred as most systems interconnect with others( i.e. the internet)
- <span color="blue">Portals</span> provide web access to internal systems
- <span color="blue">Network computers (thin clients) </span>are like Web terminals
- Mobile computers interconnect via <span color="blue">wireless networks</span>
- Networking becoming ubiquitous - even home systems use<span color="blue"> firewalls</span> to protect home computers from Internet attacks.
# Distributed Systems
### Distributed computing
- Collection of separate, possibly heterogeneous, systems networked together
	- Network is a communications path, TCP/IP most common
		- Local Area Network (LAN)
		- Wide Area Network (WAN)
		- Metropolitan Area Network (MAN)
		- Personal Area Network (PAN)
- Network Operating System provides features between systems across network
	- Communication scheme allows systems to exchange messages
	- Illusion of a single system
## Computing Environments - Client Server
- Client-Server Computing
	- Dumb terminals supplanted by smart PCs
	- Many systems now servers, responding to requests generated by clients
		- Compute - server system provides an interface to client to request services (i,e., database)
		- File0server system provides interface for clients to store and retrieve files
			[image omitted: personal or temporary Notion asset]
## Computing Environments - Peer-to-Peer
- Another model of distributed system
- P2P does not distinguish clients and servers
	- Instead all nodes are considered peers
	- May each act as client, server or both
	- Node must join P2P network
		- Registers its service with central lookup service on network, or
		- Broadcast request for service and respond to requets for service via discovery protocol
	- Examples include Napster and Cnutella, Voice over IP(VoIP) such as Skype
## Computing Enviroments - Virtualization
- Allows operating systems to run applications within other OSes 
	- Vast and growing industry
- Emulation used when source CPu type different from target type (i.e. PowerPc to Intel x86)
	- Generally slowest method
	- When computer language not compiled to native code - Interpretation
- Virtualization - OS natively compiled for CPU, running guest OSes also natively compiled
	- Consider VMware running WinXP guest, each running applications, all on natvie WinXP host OS
	- VMM provides virtualization services
## Computing Environments - Cloud Computing
- Delivers computing, storage, even apps as a service across a network
- Logical extension of virtualization as based on virtualization 
	- Amazon EC2 has thousands or servers, milions of VMs, PBs of storage available across the Internet, pay based on usage
- Many types
	- Public cloud - available vai Internet to anyone willing to pay
	- Private cloud - run by a company for the company’s own use
	- Hybrid cloud - includes both public and private cloud components
	- Software as a Service (SaaS) - one or more applications available via the Internet (i.e. word processor)
	- Platfrom as a Service (PaaS) - software stack ready for application use via the Internet (i.e a database server)
	- Infrastructure as a Service (IaaS) - servers or storage available over Internet (i.e. storage available for back up use)
- Cloud compute environments composed of traditional OSes, plue VMMs, plus cloud management tools
	- Internet connectivity requires security like firewalls
	- Load balancers spread traffic across multiple applications
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
## Computing Environments - Real-Time Embedded Systems
- Real-time embedded systems most prevalent form of computers 
	- Vary considerable, special purpose, limited purpose OS, real-time OS
	- Use expanding
- Many other special computing environments as well 
	- Some have OSes, some perform tasks without an OS
- Real-time OS has well-defined fixed time constraints
	- Processing must be done within constraint
	- Correct operation only if constraints met
- Hard real time :
	- Secondary storage limited or absent, data stored in short tern memory, or read-only memory(ROM)
	- Confilcts with time-sharing systems, not supported by general-purpose operating systems.
- Soft real-time
	- Limited utility in industrial control of robotics
	- Useful in applications (multimedia, virtual reality) requiring advanced operating-system features.
# Free and Open-Source Operating Systems
- Operating systems made available in source-code format rather than just binary closed-source and proprietary 
- Counter to the copy protection and Digital Rights Management (DRM) movement
- Started by Free Software Foundation (FSF), which has “copyleft” GNU Public License(GPL)
	- Free software and open-source software are two different ideas championed by different groups of people
- Examples include GNU/Linux and BSD UNIX (including core of Mac OS X), and many more
- Can use VMM like VMware Player(Free on Windows), Virturalbox (open source and free on many plaforms)
	- Use to run guest operating systems for exploration
# Kernel Data Structures
Many similar to standard programming data structures 
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
# chapter 2: Operating-System Structures
- Operating System Services
- User and Operating System-Interface
- System Calls
- System Services
- Linkers and Loaders
- Why Applications are Operating Systme Specific
- Operating-System Design and Implementation
- Operating System Structure
- Building and Booting an Operating System
- Building and Booting and Operating System
- Operating System Debugging
# Operating System Services
- Operating systems provide an environment for execution of programs and services to programs and users
- One set of operating-system services provides functions that are helpful to the user:
	- User interface - Almost all operating systems have a user interface(UI).
		- Varies between Command - Line (CLI), Graphics User Interface(GUI), touch-screen, Batch
	- Program execution - The system must be able to load a program into memroy and to run that program, end exectuion, either normally or abnormally (indicating error)
	- I/O operations -  A running program may require I/O, which may involve a file or an I/O device
	- File- system manipulation - The file system is of particular interest. them, search them, list file information, permission management.
	- Communications - Process may exchange information, on the same computer or between computers over a network
		- Communications may be via shared memory or through message passing (packets moved by the OS)
	- Error detection - OS needs to be constantly aware of possible errors 
		- May occur in the CPU and memory hardware, in I/O devices, in user program
		- For each type of error, OS should take the appropriate action to ensure correct and consistent computing 
		- Debugging facilities can greatly enhance the user’s and programmer’s abilities to efficiently use the system.
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]

---

# 4️⃣ 4주차

# Interrupt & Trap
- interrupt : 하드웨어적인 사건 (clock, 디스크 쓰기 완료, 패킷 도착)
- trap : 소프트웨어적인 사건 (페이지 부재 결함, divided by zero, 시스템 호출, access violation)
	        : 사용자가 운영체제 내부로 서비스를 받기 위해 (시스템 콜) 안으로 들어가는 절차
	        : 사용자 프로그램이 하기 어려운 일을 운영체제에게 부탁하기 위해 시스템 콜을 호출한다.
	<span color="yellow_bg">▶️ 하드웨어적이진 않지만 하드웨어적인 척 하면서 일부로 트러블 발생</span>
💡 handler : 어떤 일이 일어났을 때, 핸들러가 처리해준다.
[image omitted: personal or temporary Notion asset]
### Interrupt Time Line for a Single Process Doing Output
[image omitted: personal or temporary Notion asset]
▶️ Polling과 Interrupt 
▶️ I/O interrupt processing - handler가 처리
▶️ I/O는 아무것도 하지 않거나 아니면 데이터를 내보내거나 받는다 
	그렇지만 하루 종일 기다릴 수 없기에 interrupt 사용한다.
▶️ I/O에 신호가 들어왔을 때, CPU는 일단 하고 있던 일을 계속하고 i/o는 데이터를 들여보낸다.
handler에는 해야 할 일들이 쌓여있고 데이터가 다 들어왔을 때 cpu에 interrupt가 걸리고 cpu가 원래 하던 일을 잠깐 멈추고 새로 들어온 일을 한다. 그러고 handler가 가져온 일을 끝내면 원래 하던 일을 다시 돌아와서 한다. i/o는 새로운 interrupt가 생기기 전까지는 쉬고 있는다. 
⭐ \<i/o input 장치는 많아도 들어오는 bus는 하나밖에 없다\>
▶️ bus의 관점에서는 cpu와 i/o가 동시에 사용하기 때문에 위 사진을 확대하면 아마 점으로 끊겨있을 것이다. 
▶️ polling : cpu에서 interrupt가 왔는지 안 왔는지 계속 보는 것. interrupt가 오면 즉각 처리할 수 있다.
# Direct Memory Access Structure
- Too Much data transfer via CPU
- 일반적인 메모리 처리
	- 메모리 → cpu 통과 → 메모리 느려지고, 버스를 차지하여 i/o 전송 못하고, cpu가 원래 해야 하는 일 못함
- 그래서 중간에 DMAC를 둬서 필요할 때 일처리를 일임시킴. CPU를 거치지 않게 됨.
- CPU가 메모리를 사용해야 할 때, 일처리를 위한 처리 방법이 필요하게 됨. 
	- (언제 어떻게 DMA를 처리할건가?)
	[image omitted: personal or temporary Notion asset]
- DMA 제어기는 메모리의 속도를 비슷한 속도로 정보를 전송할 수 있는 고속의 입출력 장치를 위해 사용된다.
- 장치 제어기는 전체 자료 블록을 CPU의 간섭 없이 직접 기억장치에서 버퍼 저장 장치로 블록 단위로 전송한다. (by DMAC)
- Word mode : Word 단위로 데이터로 전송한다. → 제일 작은 것
- Burst mode : 바이트(혹은 워드) 당 하나의 인터럽트를 발생시키는 것이 아니라 블록 단위로 전송하고 인터럽트를 발생시킨다.  ⭐전송 중 버스를 득점 → 제일 큰 것
- DMAC의 처리보다 CPU의 처리가 더 빠르다. Word mode에서는, 전송을 위해 동시에 버스를 요청할 때, CPU가 DMAC에게 Bus 사용의 우선순위를 주어 먼저 처리하게 한다. 1 Word 정도이므로. 이것을<span color="red" underline="true"> cycle stealing</span>이라고 한다. 다른 말로, DMA가 전송을 위해 word mode에서는 CPU에게 1 메모리 사이클을 중지할 것을 요청한다는 것이다.
# Storage Structure
### Main memory 
▶️ Only large storage media that the CPU can access directly.
### Secondary storage
▶️ extension of main memory that provides large nonvolatile storage capacity.
### Magnetic disks
▶️ rigid metal or glass platters covered with magnetic recording material
	- Disk surface is logically divided into tracks, which are subdivided into sectors.
	- The disk controller determines the logical interaction between the device and the computer.
### HDD
[image omitted: personal or temporary Notion asset]
### HDD 데이터 기록 판독원리
[image omitted: personal or temporary Notion asset]
### Moving-Head Disk Mechanism
[image omitted: personal or temporary Notion asset]
▶️ 인터리브 → 고속 회전에 따른 지연을 고려해서 효율을 높이기 위함. 속도를 고려해야 
[image omitted: personal or temporary Notion asset]
- 표현의 차이가 있긴 한데, 보통
- 1:2 혹은 2:1 방식이면, 자기 섹터 포함, 2개 뒤에 다음 섹터가 있다는 뜻이다.
- 1:3 혹은 3:1 방식이면, 3개 뒤에 있고, 1:1 이면 바로 뒤에 붙어 있다는 뜻이다.
- 따라서 1:2 방식은 전체 섹터를 읽기 위해 2회전, 1:3은 3회전이 필요하다.
# RAID(Redundant Array of Inexpensive)
- 여러대의 물리적 디스크를 하나의 논리적 디스크로 인식시키는 기술
- 성능을 향상시키거나, 안정성을 향상시키는 목적으로 사용
- 각각의 목적에 따라 여럭자ㅣ의 결합 방법으로 구성시킬 수 있다.
▶️ RAID 0 - 빠르지만 안전하지 않다.
[image omitted: personal or temporary Notion asset]
▶️ RAID 1 - 미러링, 각 디스크에 중복저장 2배의 공간이 필요, 읽기 빠름
[image omitted: personal or temporary Notion asset]
▶️ RAID 4 - 블록별로 데이터를 나눠 저장하고, 비트 패리티 사용 디스크 1개의 디스크에 패리티 비           트를 저장. 오류 정정 가능.
[image omitted: personal or temporary Notion asset]
이 외에도 많은 방식을 이용하여 속도/ 안정성 등을 목표로 응용 사용
# Storage-Device Hierarchy
[image omitted: personal or temporary Notion asset]

---

# 4️⃣ 4주차 - 2

# System Calls
- Programming interface to the services provided by the OS
- Typically written in a high-level language (C or C++)
- Most common APIs are Win32 API for Windows, POSIX API for POSIX-based systems (including virtually all versions of UNIX, Linux, and Mac OS X), and Java API for the Java virtual machine(JVM)
- 보호하고 있는 HW 처리를 위해서, 혹은 순수 서비스 제공을 위해서 커널에서의 사용을 위해 필요.
# Example of System Calls
- System call sequence to copy the contents of one file to another file
[image omitted: personal or temporary Notion asset]
▶️ 이 각각을 system call을 사용해서 처리한다
# Example of Standard API
[image omitted: personal or temporary Notion asset]
▶️ System call로 되어있는 것을 코드가 너무 복잡하고 어렵기 때문에 API를 사용해서 좀 더 보기 쉽게 사용한다. → 우리가 흔히 알고 있는 함수형태
# System Call Implementation
- 컴퓨터 시스템과 운영체제마다 조금씩 다르겠지만, 시스템콜은 system call 10H(sub) function 2와 같은 형태로 호출됨.
- 시스템콜을 호출하면, OS 커널 내의 해당 기능을 불러내서, 해당 기능을 수행하고, 끝나고 나면 다시 원래 호출된 자리로 복귀하는 방식, 일반 함수를 호출하는 것과 사실 같은 것
- 호출하는 쪽은 그것이 어떻게 구현되어있는지는 전혀 알 필요가 없음. 그저 API의 형태와 사용법을 잘 숙지하고 따르면 해당 기능은 원활히 동작될 것.
- 그리고 모르는게 아니라, 사실 완전히 막혀있는 것. 알 필요도 없고, 손대지도 마라는 뜻. 왜냐하면 하드웨어 제어는 운영체제가 보호해야 할 부분이니까.
### Standard C Library Example
- C program invoking printf() library call, which calls write() system call
[image omitted: personal or temporary Notion asset]
▶️ system call은 user처럼 들락날락 거리는 사람 말고 kernel에 있어서 잘 만질 수 없도록 한다.
▶️ kernel을 많이 사용하고 system call을 많이 사용하면 효율이 떨어진다. (왔다갔다를 많이 하니까)
# System Call Parameter Passing
- System call 은 컴퓨터에 따라 방법이 서로 다를 수 있다.
	- 파라미터가 복잡하게 길 수도 있고, 묵시적으로 정해질 수도 있다.
	- Three general methods used to pass parameters to the OS
	- Simplest: pass the parameters in registers
		- In some cases, may be more parameters than registers
	- Parameters stored in a block, or table, in memory, and address of block passed as a parameter in a register
		- This approach taken byt Linux and Solaris
	- Parameters placed, or pushed onto the stack by the program and popped off the stack by the operating system
	- Block and stack methods do not limit the number or length of parameters being passed 
# Types of System Calls
1. Process control
2. File manipulation
3. Device management
4. Information maintenance
5. Communication
6. Protection
### 1. PROCESS Example : Process control
- end, abort
- load, execute
- create process, terminate process
- get process attributes, set process attributes
- wait for time
- wait event, signal event
- allocate and free memory
- Dump memory if error
- Debugger for determining bugs, single step 
### 2. PROCESS Example : Single Tasking
- Shell invoked when system booted
- Simple methoed to run program
	- No process created
- Single memory space
- Loads program into memory, overwrirting all but the kernel
- Program exit → shell reloaded
### 3. FreeBSD (Multi Tasking)
- Unix variant
- Multitasking
- User login → invoke user’s choice of shell
- Shell executes fork() system call to create process
	- Executes exec() to load program into process
	- Shell waits for process to terminate or continues with user commands
- Process exits with code of 0 - no error or \> 0 - error code
[image omitted: personal or temporary Notion asset]
# Examples of Windows and Unix System calls
[image omitted: personal or temporary Notion asset]
# Linkers and Loaders
- Source code compiled into object files desinged to be loaded into any physical memroy loaciton -  relocatable object file
- Linker combines thses into single binary executable file 
	- aslo brings in libraries
- Program resieds on secondary storage as binary executable
- Must be brought into memory by<span color="blue"> loader </span>to be executed 
	- <span color="blue">Reloation </span>assigns final addresses to program parts and adjusts code and data in program to match those addresses
- Modern general purpose systems don’t link libraries into executables
	- Rather, <span color="blue">dynamically linked libraries</span> (in Winodws, <span color="blue">DLLs</span>) are loaded as needed, shared by all that use the same version of that same library(loaded once)
- Object, executable files have standard formats, so operating system knows how to load and start them.
# The Role of the Linker and Loader
[image omitted: personal or temporary Notion asset]
▶️ linker 은 여러 object를 묶는 역할 → object를 묶은 것은 library
▶️ ojbect는 c파일 complie한 것.
▶️ loader는 실행파일쪽에 있음 
# Why Applications are Operating System Specific
- Apps compiled on one system usually not executable on other operating systems
- Each operating system provides its own unique system calls 
	- Own file formats, etc
- Apps can be multi-operating system
	- Written in inerpreted language like Python, Ruby, and interpreter available on multiple operating systems
	- App written in language that includes a VM containging the running app (like Java)
# Operating Systme Structure
- General-purpose OS is very large program
- Various ways to structure ones
### 1. Simple Structure
- Monolithic Sturture
- i.e. MS-DOS - wriiten to provide the most functionality in the least space
	- not divided into modules
	- Although MS-DOS has some structure, its interfaces and levles of functionality are not well seperated
### 2. Layered Approach
- The operating system is divided into a number of layers.(levles). The bottom layer(layer 0), is the hardware; the highest (layer N) is the user interface.
[image omitted: personal or temporary Notion asset]
### 3. Microkernel System Structure
- Moves as much from the kernel into user space
- Mach example of microkernel
	- Mac OS X kernel(Darwin) partly based on a Mach
	- mach 커널 + BSD 커널 → XUN 커널
	[image omitted: personal or temporary Notion asset]
▶️ 커널의 역할은 최소로 하고 서비스로 기능을 수행하며, 서비스 끼리는 커널을 통한 메시지 전달로 통신한다. 안전적 구조. 많은 통신(메시지)이 생기면 효율이 저하될 수도. 그러나 복구 또한 간편한 편
### 4. Modules
- Mose modern operating systems implement loadable kernel modules
	- Uses object-oriented approach
	- Each core component is separate
	- Each talks to the others over known interfaces
	- Each is loadable as needed within the kernel
	- 커널을 포함해서 각 모듈을 따로 관리할 수 있다. 부분적인 교체/업그레이드 등, 기능보다는 형태의 관점
## 참고로 linux system 구조는
MONOLITIC PLUS MODUELAR DESING → 하이브리드
[image omitted: personal or temporary Notion asset]
# Building and Booting an Operating System
- Operating systems generally desinged to run on a class of systems with variety of perpherais
- Commonly, operaing system already installed on purchaed compuer
	- But can build and install some other operating systems
	- if generating an operating system from scratch
		- Write the operating system scource code
		- Configure the operating system for the system on which it will run
		- Compile the operating system
		- Install the operating sytstem
		- Boot the computer and its new operating system.
# Opertaing-system Debugging
- Debugging is finding and fixing errors, or bugs
- OSes generate log files containing error information
- Failure of an application can generate core dump file capturing memroy of the process
- Operating system failure can generate crash dump file containing kernel memory
“Debugging is twice as hard as writting the code in the first place. Therefore, if you write the code as cleverly as possibel, you are by definition not smart enough to debug it.”

---

# 5️⃣ 5주차

# Chapter 3 : Processes
## Process Concept
- 운영체제는 다양한 프로그램들을 실행한다 :
	- 일괄처리 시스템(Batch system)은 작업(jobs)들을 실행
	- 시분할 시스템(Time -shared systems)은 사용자 프로그램이나 태스크(tasks)를 수행시킨다.
- 이 책에서는 작업(job)과 프로세스(process)를 거의 유사하게 사용한다
- Process - <span color="yellow_bg">수행중인 프로그램</span>; 프로세스의 실행은<span color="red"> 순차적인 방식</span>(sequential fashion)으로 진행된다.
	⇒ 어떤 시점에서든지 하나의 명령어만이 프로세스를 위하여 실행된다.
- <span underline="true">프로세스란 단순히 프로그램 그 자체를 의미하는 것이 아니라 다음을 포함한 </span><span color="blue" underline="true">능동적인</span><span underline="true"> 실체이다</span>:
	- program counter
	- stack
	- data section
	- 레지스터
	- 프로그램 코드
## Process in Memory
[image omitted: personal or temporary Notion asset]
## Memory layout in c program
[image omitted: personal or temporary Notion asset]
## Process State
- As a process executes, it changes <span color="blue">state</span>
	- new : The process is being created
	- running : Instructions are being executed
	- waiting : The process is waiting for same event to occur
	- ready : The process is waiting to be assigned to a processor
	- terminated : The process has finished execution
	- 프로세스를 체계적으로 관리하려면 이렇게 상태를 나눌 필요가 있다.
## Diagram of Process State
[image omitted: personal or temporary Notion asset]
terminated는 running에서만 waiting에서는 I/O기다리다가 들어오면 ready로 갔다가 running으로감.
⭐ 모든 상태는 ready에서 만나고 딱 한놈만 running으로 간다. terminated는 running으로 넘어가서의 상태 그 한 놈 빼고 나머지는 ready와 waiting에 있는 것.
⭐ ready에서 running으로 가는 것을 scheduling이라고 한다.
## Process Control Block (PCB)
- 각 프로세스는 운영체제에서 프로세스 제어 블록(PCB)에 의해 표현된다.
- 프로세스 제어 블록은 특정 프로세스에 대하여 많은 정볼르 갖는 데이터 블록이나 레코드들로서 다음과 같은 것들이 있다.
	- Prcoess state (프로세스 상태) - 생성, 준비, 수행 대기, 정지 상태
	- Program counter(프로그램 카운터) - 다음에 실행될 명령어의 주소
	- CPU registers (CPU 레지스터) : 컴퓨터 구조에 따라 다양한 수와 형태를 갖는다.
	- CPU scheduling information : 프로세스 우선 순위, 스케줄 큐의 포인터와 다른 스케줄 매개 변수들을 포함한다.
	- Memory-management information : 기준과 한계 레지스터의 값, 운영체제가 사용하는 기억장치 시스템의 페이지 테이블 또는 세그먼트 테이블의 정보를 포함한다.
	- Accounting information : CPU가 사용된 실시간의 양, 시간 범위, 계정 번호, 작업 또는 프로세스 번호를 포함한다.
	- I/O status information
[image omitted: personal or temporary Notion asset]
## CPU Switch From Process to Process
[image omitted: personal or temporary Notion asset]
▶️ PCB0를 어딘가 저장해놓는다. (그때동안 CPU는 운영체제(커널)이 차지하고 있다 → 두 process 아무도 cpu차지 하고있지 않음)
▶️  어딘가 저장되어 있는 PCB1을 다시 불러온다. → 그 후 PCB1 실행 
▶️ 등등 여러가지 이유로 PCB1가 끝이나면 PCB1을 저장한다.
▶️ PCB0을 불러와서 실행한다. 
⭐ 이 모든게 바로가 아니라 . . . (지연)이 필요하다.
	= 이 모든 과정을 <span color="red">“Switching” </span>이라고 한다.
## Threads
- So far, process has a single thread of executin
- Consider having multiple program counters per process
	- Multiple loactions can execute at once
		- Multiple threads of control → <span color="blue">threads</span>
- Must then have storage for thread details, multiple program counters in PCB
- <span color="red">Explore in detail in Chapter 4</span>
## Process Scheduling
- Maximize CPU use, quickly switch processes onto CPU for time sharing
- <span color="blue">Process scheduler</span> selects among available processes for next execution on CPU
- Maintains <span color="blue">scheduling queues</span> of processes
	- <span color="blue">Ready queue</span> - set of all processes residing in main memory, ready and waiting to execute
	- <span color="blue">Wait queues</span> - set of processes waiting for and event (i.e. I/O)
	- <span color="blue">Device queues </span>- set of processes waiting for an I/O device
	- Porcesses migrate among the various queues
	## Ready and Wait Queues
[image omitted: personal or temporary Notion asset]
## Representation of Process Scheduling
[image omitted: personal or temporary Notion asset]
▶️ time slice expired → 타임 슬라이스가 끝나려면 <span color="red">주어진 시간</span>이 있어야한다. 
## Schedulers
- 프로세스는 실행되는 동안 다양한 스케줄러 큐들 사이를 이주하게 된다. 운영체제는 어떤 방법으로든지 이들 큐에서 프로세스들을 선택해야 한다.
	- 장기 스케줄러(Long-term scheduler (or job scheduler)) - <span color="red">프로세스를 선택하여 실행하기 위해 기억장치로 적재</span>하는 것 (새로 만든 프로세스 중에 ready 큐로 보낼 것을 선택, 서버 같이 아주 프로세스가 많을 때)
	- 단기 스케줄러(Short-term scheduler (or CPU scheduler)) - 실행 준비가 되어 있는 프로세스 중에서 하나를 선택하여 cpu를 할당
	- 단기 스케줄러는 실행 빈도수(milliseconds), 즉 cpu에 의해 매우 빈번히 선택되기 때문에, 매우 빨라야한다.
- 장기 스케줄러는 시스템에서 자주 선택되지 않으므로 (seconds, minutes) 실행 빈도수가 낮아 느리게 수행되어오 된다.
	- 따라서, 장기 스케줄러는 다중 프로그래밍의 수(기억 장치에 있는 프로세스들의 수)를 제어한다.
	- 프로세스들은 다음과 같이 두가지로 묘사될 수 있다.
	- 입출력 중심 프로세스(I/O-bound process) - 이는 연산보다 입출력 수행에 더 많은 시간을 소비하는 프로세스ㅡ
	- CPU 중심 프로세스(CPU-bound process) - 이는 입출력 중심 프로세스보다 연산에 더 시간을 소비하여 입출력 요청이 드물게 발생하는 프로세스,
		- 롱텀 스케줄러는 good process mix를 위해 노력을 해야 한다.
		- 시 분할 시스템과 같은 일부 운영 체제들은 부수적인 중간 단계의 주익 스케줄링을 도입한다. (장기 스케줄러가 없는 경우도)
	- 스와핑 처리( 프로세스들 중에서 필요한(기준이 있겠지요) 것을 골라 디스크로 메모리 덤프/디스크에서 읽어옴
## Addition of Medium Term Scheduling
[image omitted: personal or temporary Notion asset]
- Medium-term scheduler can be added if degree of multiple programming needs to decrease
	- Remove process from memory, store on disk, bring back in from disk to continue execution : swapping
## Multitasking or Multiprocessing
- 여러 개의 프로세스(or Task)를 번갈아서 처리 할 때 이 것을 멀티태스킹이라고 한다.
- 큰 메모리에서 단기 스케줄러가 빠르게 문맥을 교환하여 처리할 수 있으면, 여러개의 프로세스가 동시에 동작하는 것처럼 보인다. (실제로 동시에 동작하는 것이기도 하다)
- 그러나 이러헥 동작한다고 해서 “체감적으로” 문제없이 여러 개의 프로세스가 잘 동작하는 것은 아니다.
- 멀티태스킹이 된다는 것이, 곧 실시간으로 번갈아 처리된다는 뜻은 아니다. 관점이 다른 이야기 이다.
- 예를 들어, 적은 용량의 메모리 환경에서 스와핑이 많이 발생하는 경우, I/O 처리의 시간이 지나치게 많이 소요 될 수도 있다. 
## Multitasking in Mobile Systems
- Some mobile systems (e.g ., early verion of IOS) allow only one process to run, others suspended
- Due to screen real estate, user interface limits iOS provides for a 
	- Single foreground process - controlled via user interface
	- Multiple backgroud processes - in memory, running, but not on the display, and with limits
	- Limits include single, short task, receiving notification of events, specific long-running task like audio playback
- Android runs foreground and background, with fewer limits
	- Background process uses a service to perform tasks
	- Service can keep running even if background process is suspended
	- Service has no user interface, small memory use

---

# 6️⃣ 6주차

# Basic Concepts
- Maximum CPU utilzation obtained with multiprogramming
- CPU-I/O Burst Cycle - Process execution consists of a <span color="blue">cycle</span> of CPU execution and I/O wait.
- <span color="blue">CPU burst</span> floowed by<span color="blue"> I/O burst</span>
- CPU burst distribution is of main concern
[image omitted: personal or temporary Notion asset]
# Histrogram of CPU-burst Times
[image omitted: personal or temporary Notion asset]
▶️ 생각보다 cpu가 차지하는 burst time은 별로 없다.
▶️ 조금 일하고 i/o 오고 한다 (i/o는 물리적인 행동) 나머지는 전기적인 행동이기에 i/o가 제일 김 그래서 i/o를 받는 동안 cpu 일을 시킴
# CPU Scheduler
- <span color="blue">Short-term scheduler</span> selects from among the processes in ready queue, and allocates the CPU to one of them
	- Queue may be ordered in various ways
- CPU scheduling decisins may take place when a process:
	1. Switches from running to wating state
	2. Switches from running to ready state
	3. Switches from wating to ready → 여기는 빼먹을 확률이 있음
	4. Terminates
- Scheduling under 1 and 4 is <span color="blue">nonpreemptive (비강제적, 자발적으로) </span><span color="yellow_bg">→1,4번은 모든 일이 수행</span>
- All other schedulingis <span color="blue">preemptive (강제로 끄집어 내리다) </span><span color="yellow_bg">→ 실행할게 좀 남아있음(강제 내려감)</span>
	- Consider access to shared data
	- Consider preemption while in kernel mode
	- Consider interrupts occurring during crucial OS activities.
	# Dispatcher
- dispatcher module은 단기 스케줄러가 <span color="red">선택한 프로세서에게 CPU의 제어를 부여하는 모듈</span>이다.
- 이 기능은 다음을 포함
	- switching context
	- switching ti user mode
	- jumping to the proper location in the user program to restart that program
- <span color="blue">Dispatch latency </span>- time it takes for the dispatcher to stop one process and start another running
	= Dispatch가 다 할 때까지의 시간(지연)
	= 빈번한 switching은 dispatch latency의 시간이 길어진다.
	= 좋은 dispatch는 우선순위와 시간 등 다양한 방법을 짠다.
[image omitted: personal or temporary Notion asset]
# Scheduling Criteria
- 중앙처리장치 이용률(CPU utilization) - 가능한 CPU를 바쁘게 이용한다.
- 처리율(Throughput) - 단위 시간당 실행 완료된 프로세스의 개수
- 반환시간, 소요시간(Turnaround time) - 프로세스를 실행하는데 소요된 시간, 즉 , 진입한 시간과 완료된 시간의 차이.
- 대기시간(Waiting time) - ready queue에서 대기하면서 보낸 시간 <span color="yellow_bg">→ 줄이는게 가장 좋음</span>
- 응답시간(Response time) - 하나의 작업을 요청한 후, 첫번째 응답이 나올 때까지의 시간. 출력이아님.
# Fisrt-Come, Fisrt-Served (FCFS) Scheduling
- Suppose that the processes arrive in the order : P1,P2,P3
	The Cantt Chart for the schdule is:
	[image omitted: personal or temporary Notion asset]
▶️ 선착순, 처음 온 것 먼저 수
▶️ 총 걸린 시간은 30
# FCFS Schduling 
Suppose that the processes arrive in the order p2, p3, p1
[image omitted: personal or temporary Notion asset]
- FCFS에서처럼 몇몇 느린 프로세스떄문에 전체가 늚
# Shortest-Job-First(SJF) Scheduling
- 앞서 살펴본대로, 프로세스의 순서를 정하는 것은 전체 효율에 큰 영향을 끼친다.
- 특히, CPU에 burst time 길이가 가지는 영향이 크다. 이것이 중요하다. 이것을 이용해보자
	- Use these lengths to schedule the process with the shortest time
	# Example of SJF (NON-Preemptive)
[image omitted: personal or temporary Notion asset]
# Example of Preemptie SJF
[image omitted: personal or temporary Notion asset]

---

# 7️⃣ 7주차

# PC Assembly - 명령어 요약 (예시)
# PC Assembly - 코딩 요약
```javascript
CODE SEGMENT //SEGMENT 지정
ASSUME CS:CODE

	MOV AH, 12H //명령어
	MOV AL, 34H //명령어
	ADD AH, AL //명령어
	
	MOV AH 4CH //명령어
	INT 21H //interrupt
	
	CODE ENDS
	
	END
```
\<Int 21H - 02\>
💡 System call 21H sub function2 💡
▶️ 입력 : AH = 2
	          DL = ASCII 값
▶️ 출력 : 화면에 글자를 하나 출력
- SEGMENT 방식을 사용 → CODE를 가지고 있음 CODE SEGMENT
	                                         DATA를 가지고 있음 DATA SEGMENT 등..

---

# 11주차 

# Chapter 6. Process Synchronization
= 무언가를 주고받고자 하는 것
\<목차\>
- Background
- The Critical-Section Problem
- Peterson’s Soultion
- Synchronization Hardware
- Mutex Locks
- Semaphores
- Classic Problems of Synchronization
- Monitors
- Synchronixation Examples
- Alternative Approaches
\<  background 예시\>
## Bounded-Buffer
[image omitted: personal or temporary Notion asset]
→ 끊임없이 쌓아줄 수 있기 떄문에 원형 큐를 사용한다
→ consumer라고 하는 애가 하나씩 빼간다 (여러개가 돌아가는데 각자 자기 일을 한다)
→ 원형 queue는 rear과 front 필요 
	원형 queue 장점 = 데이터 블록을 옮기는 정비 과정 필요 없음
	원형 queue 단점 = rear와 front가 만나는 순간 = end(원형queue의 데이터가 비었다)
→ counter는 몇개의 데이터가 들어있는지의 개수
→ 그림에서는 3개의 프로그램이 같은 데이터를 쓰고있음
\<producer process\>
[image omitted: personal or temporary Notion asset]
→ counter == buffer_size ⇒ 원형 큐가 꽉 찼다는 의미
→ 하나를 비워야 한다.
→ producer는 데이터 하나를 채우고 counter를 하나 더하겠다라는 의미의 코드
\<consumer process\>
[image omitted: personal or temporary Notion asset]
→ 원래는 rear==front로 해야하는데 하나를 비워야하기 때문에 counter 값이 0인지로 확인한다.
→ consumer는 하나 빼고 counter를 하나 줄이겠다 하는 의미의 코드.
<callout icon="💡" color="gray_bg">
	지금까지 counter가 있으면 좋다는 것을 설명
</callout>
[image omitted: personal or temporary Notion asset]
→ counter를 증가시키는게 cpu 입장에서는 하나의 명령이 아니다. 
	=코드가 언제 끊길지 모른다  = atomic(원자 = 쪼개지지 않는다) 이라고 말함.
	= cpu입장에서는 쪼개지지 않기 때문에 atomic이라고 한다.
→ counter++, —는 고급언어에서는 명령어지만 cpu입장에서는 명령어가 아니다.
[image omitted: personal or temporary Notion asset]
→ counter++와 —를 어셈블리어로 표현하면 위와 같다.
→ counter의 원래값이 5라면 6으로 올리고 원래 있던 번지에 6으로 저장해야한다. 
→ 1) 번지 불러오고 2) 올리고 3) 번지에 다시 저장 ⇒ cpu 입장에서는 여러개의 명령어
→ 위 코드 6개가 운이 안 좋게 꼬여버린다면 (아래 사진)
[image omitted: personal or temporary Notion asset]
1. res1 에서 5를 가져옴
2. res1에서 5의 값을 하나로 증가 6으로 만든다 (아직 counter에 6으로 저장은 안 한 상태)
3. context swiching 되어 comsumer로 가서 res2에 counter(=5)를 읽어옴
4. res2에서 5의 값을 하나 감소하여 4로 만든다.
5. counter에 res1값으로 6을 넣고
6. counter에 res2값으로 4를 넣는다. 
→ counter의 마지막 값은 4가 들어간다. 
→ counter를 공유하기 때문에 생긴 일
[image omitted: personal or temporary Notion asset]
→ 결론적으로 프로세스들은 동시에 시작될 수 있다.
→ 그러한 프로세스들이 같은 res값을 사용하고 있다면 문제가 생길 수 있다.
> ⇒ 이러한 문제는 atomic하지 않아서 생긴 문제이다. 이를 atomically하게 해야한다면?<br><br>= 기본적인 해결방법은 atomic하게 하면 된다 = 운영체제의 도움이 필요
[image omitted: personal or temporary Notion asset]
→ bounded = 제한이 있는 (buffer 크기에 제한이 있다)
→ 어셈블리어 명령어 수준에서 서로 섞일 수 있다.
→<span color="red"> 항상 그런게 아니라 상황에 따라 다를 수 있다.</span>
[image omitted: personal or temporary Notion asset]
→ 경쟁상태는 아래와 같이, 새로운 프로세스를 생성할 때(fork)에서도 발행할 수 있다.
→ Process P0 and P are creating child processes using the fork() system call
→ Race condition on kernel variable nex_available_pid which represents the next avilable process identifier(pid)
[image omitted: personal or temporary Notion asset]
→ 문제가 생기지 않기 위해 다른 방향으로 가는 것도 안된다. 
→ 너무 atomic 하게 가는건 현재 반하는 일이다.
- 프로세스 동기화 하는 실제 많은 문제를 해결하는 방법이고, 그 과정을 코드로 확인할 수 있다.
- 이러닝 동영상에 코드도 보여주고, 설명도 상세하게 하고 있으니 실제 코드를 보면서 문제 이해의 폭을 넓히자.
\<이 순서로 진도나갈 예정\>
- 클라우드 (요약)
- 동기화 (유저모드, 커널모드)
- 교착상태 → 외나무 다리에서 만났을 때 (서로가 못가는 경우)
- 뮤텍스 실습 
- 메모리 관리 
- 가상 메모리 관리 → 메모리의 한계가 있기에 가상 메모리가 있음
어셈블리 - 4문제
internet사용 불가

---

# 11주차 - 2

# Solution to Critical-Section Problem
[image omitted: personal or temporary Notion asset]
1. 상호배제(Mutual Exclusion) - 어떤 프로세스가 임계구역에서 실행된다면 다른 프로세스는 임계구역에서 실행될 수 없음 (<span color="red">= 1개만 가능</span>)
2. 진행(Progress) - 아무도 <span color="red">임계구역에 없는 상태</span>에서 임계구역으로 진입하려고 하는 프로세스들이 있으면 자유구역에서 실행되고 있지 않은 프로세스들만 다음에 임계구역으로 진입 될 수 있는 대상이 되고, 이 구역은 무한하게 연기할 수 없음.
3. 한계대기(Bounded Waiting) - <span color="red">대기하는 시간의 한계(한도)가 있어야 함</span>.  프로세스가 임계구역 진입에 대한 요청을 보낸 후 다른 프로세스들이 임계구역에 진입하도록 허용하는 시간 간격도 한계를 두어야 함. 무한할 수는 없다.
	- 이 각 프로세스들은 0이 아닌 속도로 가정하고 있음 각 프로세스들은 기다리는 것이 아닌 <span color="yellow_bg">“진행”</span>을 하고 있어야한다.
## Algorithm 1
[image omitted: personal or temporary Notion asset]
<span color="yellow_bg">알고리즘 1 설명</span>
→ 공유변수 turn이 있고 프로세스가 2개(pi,pj) 있는 경우
→ trun이 i와 다를 때 whlie문 안에서 갇혀 있고, pi가 critical section을 끝내고 turn을 j로 바꾸게 된다. 그 순간 공유변수 turn의 값이 바뀌면서 pj는 critical section으로 들어 감. pi는 while안에서 대기 중. 
✅ Mutual Exclusion 을 만족?
	→ 한번에 한 프로세스만 임계영역에 들어갈 수 있으니 가능
✅ Progress와 bounded waiting 만족?
	→ progress는 만족하지 않음
	→ pj가 먼저 실행이 된다면 turn은 0(==i)이기 때문에 turn과 j가 달라서 pj는 기다린다. pi가 들어와서 critical section을 진행 후 turn 값을 j로 바꿔줄 때까지 기다림. pj는 critical section에 들어가고자 하지만 critical section엔 아무도 없고 다만 turn이 다르니 실행이 안 되서 기다린다면 progress와 bounded waiting 둘 다 만족하지 않음.
+) 또 다른 문제는 pi가 실행하다가 오류가 생겨서 나가버리면 두번 다시 실행되지 못한다는 문제 또한 존재함.
## Algorithm 2
[image omitted: personal or temporary Notion asset]
<span color="yellow_bg">알고리즘 2 설명</span>
→ 공유변수 (배열) = 총 2개  flag[2] → flag[0], flag[1] = false
→ flag[i] = true로 pi는 critical section으로 들어간다
→ do while부분에서 자기 자신으로true로 만들고 pj가 false면 무한루프를 하지 않고 critical section으로 간다. 그 후에 i를 false로 바꾼다. 만약 pj가 또 실행되지 않는다면 pi는 또 실행될 수 있다.  이는
= <span color="red">pi와 pj가 번갈아서 실행될 필요가 없다.  → 둘다 critical section에 가지 않음</span>
→ pi가 끝나고 false로 되면 pj는 while에서 벗어나서 pi가 remainder section에 있는 동안  동시에 pj는 critical section으로 가는 것이다.
→ do while에서 pj가 실행되었을 경우 flag[j]도 true가 되고(flag[i]도 현재 true) while에서 flag[i]가 true인지 false인지 보고 아직 flag[i]가 true이기 때문에 pj는 기다린다. (아직 pi가 critical section 즉 임계영역에 있음) 
→ 또 pj가 critical section에 있는 동안에 pi가 reamainder section을 다 끝나고 while로 가면 아직 pj가 critical section에 있으니 기다리게 된다. 근데 pj가 나오면서 flag[j]를 false로 만들면 또 pi가 critical section으로 간다.
✅ 문제점이 될만한 것
→ pi와 pj가 짧은 시간에 실행된다고 하면 pi가 critical section으로 넘어가기 전에 pj도 true로 되어버리면 pi와 pj가 둘다 무한루프를 돈다. = 둘 다 대기
무한히 기다리면 progress나 bounded waiting에 문제가 있다.
### Algorithm 3- Peterson’s Solution
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
✅ pi 또는 pj 하나만 가지고도 잘 돌아가나?
→  잘 돌아감
✅ 한 프로세스가 critical section에서 진행되고 있는 동안 다른 프로세스 Mutual Exclusive하게 안 들어가 있는지?
→ 맞음
✅ 한 프로세스가 다 돌고 빠져나왔을 때 다른 프로세스는 들어갈 수 있는지?
→ 있음
✅ 하나가 어딘가에서 잘못되어 응답이 없을 때도 잘 돌아가는지(bounded waiting) 
→ 잘 돌아감
✅ 빠른 스위칭이 일어나더라도 정상작동을 하는지?
→ 가능
# Bakery Algorithm
[image omitted: personal or temporary Notion asset]
→ 앞에서는 2개의 process만 살펴보았다.
→ 지금은 2개 이상의 process가 동작을 할 때의 해결책 
→ <span color="blue">임계영역에 들어가기 전에 프로세스는 번호를 받게 된다. 가장 낮은 번호를 받는 프로세스가 먼저 임계영역에 진입</span>
→ 여러 프로세스가 동시에 번호를 요청한다면 i\<j이면 pi가 pj보다 먼저 받음
→ 번호표는 우연히 같을 수도 있다. (번호표 장치가 여러개면 같을 수 있음)
[image omitted: personal or temporary Notion asset]
→ (a,b) \< (c,d)  ⇒ a는 c와, b는 d와 각각 비교를 한다.
→ max(a0,… an-1)는 k라는 숫자 (k는 a보다 작지마 그중 가장 큰 값을 말한다)
→ 공유데이터는 2개 ⇒ choosing[n] , int number[n] 모두 초기값은 false와 0
[image omitted: personal or temporary Notion asset]
→ 무조건 이해해야함 (중요)
⭐ 모든 프로세스는 이러한 구조를 내부에 돌고 있다고 전제 ⭐
→ 가장 위 3줄 중 choosing은 번호를 부여받는 과정이다. choosing이 되기 전에는 true, 값이 정해지면 false로 다시 바꾼다.
→ for문은 n개의 번호표를 차례로 훓어본다. 번호가 0이면 critical section을 진행할 의사가 없는 프로세스이다.
→이때 번호표는 같을 수 있는데 번호표를 부여하는 곳이 critical section이 아니기 때문에 프로세스마다 달라서 번호표가 같을 수 있음.
→ number이 0이 아님과 동시에 자기의 번호표보다 작은 값이라면 그냥 돌아간다. 
→ 첫번째 while에서는 번호표가 다 부여받았는지를 확인받는 것이다 (choosing이 false면 빠져나옴)
→ 두번째 while에서 번호표가 0이 아님과 동시에 이것이 자기의 번호표보다 작은값인지를 확인한다 만일 작은 값이거나 같은 값이더라도 프로세스의 번호는 다름.
→ 만일 번호가 자신보다 작다면 루프는 그냥 돌아감 ⇒ 아직은 자기가 critical section에 들어갈때 X
→ 만일 자신의 번호가 작거나 프로세스 번호가 더 작다면 모든 Loop에서 벗어나서 critical section으로 들어갈 수 있는 기득권을 얻음
<callout icon="💡" color="gray_bg">
	기본적으로는 번호표가 작은 것이 우선이나 번호표 기계가 여러개이기 때문에 같은 번호가 있을 수 있다. 이럴때는 프로세스 번호는 고유한 값이기 때문에 프로세스 번호가 작은 것을 먼저 critical section에 들어갈 수 있도록 한다.
</callout>
→ critical section을 나오면 number[i]=0으로 만든다. (0은 critcal section에 들어갈 생각이 없다!)
[image omitted: personal or temporary Notion asset]
문제 : 이 알고리즘은 너무 SW적인 구현이라 처리가 복잡함. ⇒ 프로그램 만들기가 너무 어려움
→ 좀 더 쉬웠으면 좋겠다.
→ 위의 것들을 제공하는 hw가 있으면 좋겠다. 또

---

# 13주차

# Deadlocks
- system Model
- Deadlock Characterization
- Methods for Handling Deadlocks
- Deadlocks Prevention (예방) -교착상태를 예방 1️⃣
- Deadlocks Avoidance (회피) -교착상태를 회피 2️⃣
- Deadlocks Detection (탐지) - 교착상태가 생기면 해결 3️⃣
- Recovery from Deadlock (회복) - 및 회복
- Combined Approach to Deadlock Handling
## Deadlock Characterization
[image omitted: personal or temporary Notion asset]
→ 교착상태가 생기는 4가지 원인 
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
→ 돌아가는 원리 알기
# Memory Management
- Background
- Swapping
- Contiguous Allocation
- <span color="yellow_bg">Paging</span>
- Segmentation
- Segmentation with Paging
## (상식) Binding of Instructions and Data to Memory
### 바인딩
= 절대 주소가 언제 생기는지
- 컴파일 시간 바인딩
	- 컴파일 할 때, 실행시의 실제 주소가 미리 정해짐
	- 컴파일러는 절대코드를 생성
	- 만일, 이 위치가 변경되어야 한다면, 이 코드는 다시 컴파일 되어야 함
- 적재 시간 바인딩
	- 로더 책임 하에 주소 부여
	- 컴파일러는 일단 재배치 가능 코드로 만듦
	- 심볼과 진짜 번지와의 바인딩은 프로그램이 실제로 적재되는 시간에 이루어지게 됨
- 실행 시간 바인딩
	- 실행될 때, 프로세스의 적재위치가 확정되는 경우, 그 때 바인딩이 실행된다.
	- CPU가 주소를 샐성할 떄마다 Binding 을 점검
	- 바인딩이 반드시 실행 시간 까지 연기가 되어야 함
	- 이것이 가능하려면, 특별한 하드웨어를 이용해야 함 
	[image omitted: personal or temporary Notion asset]
→ 필요할때 마다 올리는 것
[image omitted: personal or temporary Notion asset]
→ 올라와 있는 애를 언제 어떻게 연결시킬까 (필요시마다 linking)
[image omitted: personal or temporary Notion asset]
→ usb는 파일이지만 닌텐도는 메모리 그 방식이 overlays (바꾸어 끼울 수 있는 부분만 비워둔다)
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
→ 시스템의 총 합은 660이 남아있는데 나는 400을 넣고자 하지만 연속된 메모리가 없음
= 메모리를 옮기자
→ 각각 떨어져 있는 것을 fragmentation
→ 메모리를 옮기면 좀 더 효율적
→ 어떻게 옮기면 이동이 적어질까?
→ 움직이는 양이 작은 방향으로
→ page를 쓰는 방법을 paging frame 
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
→ physical memory 부분에서는 실제로 쪼개서 사용 하지만 사용자는 logical memory를 봐서 연속인줄 알고 있음.
[image omitted: personal or temporary Notion asset]
→ tlb에 해쉬를 사용할 수도 있음
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
### virtual Memory That is Larger Than Phtsical Memory
[image omitted: personal or temporary Notion asset]
→ 원래는 physical memory 에 써야하는데 
→ dsk store는 physical memory에 옮겨야함
### Stemp in Handling a Page Fault(Cont)
[image omitted: personal or temporary Notion asset]
→ 700번지를 가져오는 물리적인 시간으로 인해 cpu는 아무것도 못하고 있음
→ 해결책을 알기.

---

# 14주차

# Virtual Memory
[image omitted: personal or temporary Notion asset]
가상 메모리는 물리적 메모리에서 사용자 논리 메모리를 분리해서 사용한다.
= 물리 메모리는 모르는 채 사용하게 한다
- 실행을 위해서 메모리는 프로그램의 일부분만 있으면 된다.
- 따라서 논리적인 주소 공간은 물리적인 주소 공간보다 클 수 있다.
- 프로세스 입장에서는 물리적 주소를 몰라도 된다.
- 그러면 논리적 주소가 훨씬 커져도 괜찮지 않나 → 중간에 관리만 잘 하면
- 좀 모자라면 2차 disk를 사용하자
- 여러 프로세스가 주소를 공유하도록 허용한다
- 좀 더 효율적인 프로세스 생성이 가능해짐 (작으니까)
	→ 전체를 다 올려놓고 쓰는 것이 아니라
	→ 실행을 하더라도 일부분만 가져와서 프로세스를 생성했다라고 생각하기 때문
	→  쓸 수 있는 page가 작아진다 ⇒ 빨리빨리 만들어진다.
- 동시에 실행할 수 있는 프로그램 개수는 늘어난다.
- 프로세스를 로드하거나 교채할 때 사용할 i/o가 감소한다
→ 가상 주소 공간 (virtual address space)
= 실제 컴퓨터 시스템이 크지 않은 물리 메모리를 가지고 있다 하더라도 자기보다 훨씬 더 큰 유저 프로세스를 받아드릴 수 있게 해주는 방법이 된다.
총정리 → 가상공간이라고 하는 것은 말그대로 가상이긴 한데 물리 메모리를 쓰지만 실제 프로세스는 물리 메모리가 아니라 논리 메모리를 알고 거기만 접근한다. 그럼 운영체제가 메모리 관리하는 쪽에서 그 논리 메모리하고 물리 메모리를 연결시켜 줄 것이고, 모자라는 부분은 (물리메모리 중) swap 디스크를 통해서 대체하도록 해주어야한다. 그 모든걸 밑단에서 알아서 해주고 나면 프로세스나 개발자들은 논리 메모리만 따지면 된다. = 가상메모리, 가상메모리 관리
## Virtual memory
### Virtual address space
[image omitted: personal or temporary Notion asset]
- 프로세스가 메모리에 저장되는 방식에 대한 이야기 ⇒  논리적관점 이야기
- 일반적으로 가상 주소 공간은 주소 0부터 시작, 공간이 끝날 때 까지 연속적인 주소를 가지게 된다.
- 거기에 대응하는 물리적 메모리는 page frame 단위로 나누어진다. ⇒ 연속적이지 않음
- 메모리를 관리하는 MMU가 반드시 논리적 공간에서 물리적 공간으로 맵핑 시켜야한다.
- 가상 메모리는 다음을 통해 구현할 수 있음
	1. demand paging = 요구 페이징
	2. demand segmentation = 요구 세그멘테이션 → 세그먼트와 뜻은 같으나 크기가 동일한게 
	                                                                                아니라 크기가 좀 가변적인 세그멘테이션이다.
	-  memory map → virtual memory  와 물리적 메모리를 연결
- backing store = 일반 하드디스크 → 물리적 메모리와 backing store 두개가 모여서 일반 메모리처럼 동작
- 만약 실제 메모리를 읽어야하는데 물리 메모리에 없다고 하면 →  backing store  (디스크에 있을 것이다)
- backing store에서 찾은 것을 물리 메모리에 집어넣어야한다.  어디에? 어떻게? 
- 일단 하나를 찾고 집어넣는다. 
- 이 모든 일은 hidden 숨어져 있는 공간에서 하기에 프로세스와 개발자는 모르게 한다.
- 스케줄링이 이상한 곳에서 생긴다. (왜냐 실행하다가 물리 메모리에 없다는 것을 알기 때문에)
- 그렇기 때문에 가상 메모리 구현이 복잡해짐
-
[image omitted: personal or temporary Notion asset]
- 가상 메모리는 주소 0부터 시작해서 연속적이다
- 물리 메모리는 연속적이지 않고 이 사이를 연결시켜주는 것이 MMU
- 일반적으로 stack 은 주소가 큰 곳부터 아래로 진행된다.
- 그다음 heap 은 code 영역, data 영역이 다 차지하고 난 뒤 그 끝부터 위로 번지가 증가된다.
- stack은 아래쪽 heap은 위쪽 (양쪽으로 진행) = 주소 공간 사용을 극대화하기 위해서
- 비워있는 공간을 hole이라고 함.
- sparse (듬성듬성 있다)= virtual address space에서의 hole → stack, heap, 동적 라이브러리 link 
[image omitted: personal or temporary Notion asset]
- 가상메모리는 page공유를 통해서 둘 이상의 프로세스가 file이나 메모리를 공유할 수 있는데, 그 방법을 그림으로 나타냄
- 두 프로세스가 있다. 이 둘이 쓰는 라이브러리가 있을 때 그것이 자신의 가상 공간의 일부라고 생각하고 진행하겠지만 실제로는 라이브러리가 존재하는 물리 프레임은 모든 프로세스들에게 공유될 수 있다. 
- 읽기전용만 된다. (쓰기전용이 되면 양쪽에서 써버리니까 문제가 생김)
- (shared pages에서 맵핑)프로세스의 맵핑 페이지를 통해서 공유 메모리를 가상 주소공간에서 읽고쓰기를 한다.
- 각 프로세스는 맵핑 페이지만 가지니까 효율적인 프로세스 생성이 가능해진다.
- 공유 하면서 프ㅜ로세스 작아지고 효율적 ㅅ프로세스 스위칭 할떄도 효율적 빨라짐
- 가상 메모리;를 쓴다는 것은 일반 프로세스의 모든 것을 빠르게 해줌
[image omitted: personal or temporary Notion asset]
- 우리가 배워야 할 것은 가상 주소를 어떻게 물리 주소로 변환을 시키느냐
- 가상 주소가 물리 주소로 변환이 될 때 swap 디바이스 보다 ram 에 들어가기를 원한다
- swap 디바이스를 억세스 하는 횟수를 최대한 줄이는 방향으로 가도록 해야한다.
- 따라서 이상적인 요구 페이징은 앞으로 사용될 페이지와 사용되지 않을 페이지를 미리 알고, 물리 메모리로 불러들이던가 swap 디바이스로 내보내는 걸 말한다 (==예측한다)
- 앞에있는 것이 진행되는 동안 backgorund 에서는 미리 올려놓고 안 쓸 것 같다고 하면 다른 거 하는동안 물리 메모리에 있는 것을 swap 디바이스로 내려보낸다.
=  이상적인 요구 페이지 동작 (모르게 동작해야함)
- page table은 ram에 없을 때 (현재 상주하고 있지 않을 때) 현재 메모리에 없다는 것을 표시할 수 있어야한다.=  swap 디바이스에 있다는 뜻
- 실제 물리메모리에 없다라고 할 때  swap 디바이스에서 찾아내야 한다. 
	- → 찾아내는 방법을 page table이 가지고 있음
- 물리 메모리에 있다면 물리 메모리에 어디 있는지를, 물리 메모리에 없다면 물리 메모리에 없다는 것과 swap  디바이스 있다는것, swap 디바이스 중에 어디 있다는 것을 page table에 표시할 수 있어야한다.
- 물리메모리와 디스크 메모리를 왔다갔다 할 때 예측만 잘할 수 있다면 모든 일을 back ground에서 처리하게 되니까 실제로 느리고 싼 저장소를 이용한다고 해도 ram처럼 잘 사용할 수 있다
	- 중요한 조건 : 예측이 가능한다면
- 만약 예측이 실패하게 되면 → 갔다놓은 것이 필요 없을 때 = 다시 갔다와야한다.
	- → 더 많은 일을 해야한다. (오히려 더 안 좋아지는 상황)
	- 이때 발생하는 것을 trashing이라고 한다 =잘못되었다.(꽝이고 다시 가져와야해!)
- 그럼 demand paging이 효과가 있을까? ⇒ Locality 가 핵심 이유로 효과가 있음
= 코드들은 지역성이 있기 때문에 demand pasing에서 자주 쓰이는 것은 메모리에서 쓰이도록 하고 자주 안 쓰이는 것들만 예측해서 잠깐잠깐 갔다놓고 없으면 다시 내려놓고.
[image omitted: personal or temporary Notion asset]
- demand pasing은 load시에 전체 메모리를 메모리에 가져올 수도 있다.
- 또는 필요할 때만 필요한 페이지를 메모리에 가져올 수도 있다.
- 근데 작게 가져올 수록 좋다
- i/o도 적게 쓰고, 필요없는 i/o도 안 쓰게 된다. = 다른 장치들이 그 시간에 i/o를 쓸 수 있음
- 적재 하는 메모리가 적게된다. = 무언가가 적어진다는 것은 그만큼 응답이 빨라짐
	- = 동시에 쓸 수 있는 프로세스의 개수도 늘어난다.
	- = 훨씬 더 많은 프로세스, 혹은 사용자의 응답을 해줄 수 있다.
- swapping 하는 것과 유사하지만 중간에 일이 많음
- 그 복잡한 문제까지 해결하는 것이 demand pasing이 할 일이다.
[image omitted: personal or temporary Notion asset]
- 또  demand pasing은 페이지가 필요하면 그때 참조하면 된다.
- 잘못된 참조가 있다면 중단하면 된다.
- 물리 메모리에 없으면 swap 디바이스에서 물리 메모리로 가져오면 된다.
- 페이지가 필요하지 않는 한 페이지를 메모리로 swap하지는 않는다. 
	- 예측을 한다고 했지만 어쨋든 필요한 순간에 가져오기 때문에 = demand pasing을 Lazy swapper(필요할 때만 하고 그외에는 하지 않는다 = 게으르다)라는 용어로도 부른다.
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
- demand pasing의 컨셉 
- pager는 다시 swap out 즉 내보내기 전에 어느 페이지를 사용할지를 미리 추측을 한다. 그래서 페이지 전체를 swap in하는 대신 필요하다고 판단되는 해당 페이지만 메모리로 가져오게 된다.
- 시간과 공간의 낭비를 줄이기 위해서
- demand pasing을 구현할 새로운 mmu 기능이 hw적으로 필요하다
- 메모리 기법에서 사용된 유효, 무효 비트를 좀 더 확장해서 써야한다.
	- 물리적 메모리에 있다, 어디에? 
	- 물리적 메모리에 없다 → swap에 있다 → 어디에?
	= 있으면 어디에 있다, 없으면 어디에 있다 이 부분이 확장이 되어야 한다.
	= 유효하는 의미는 해당 페이지가 메모리에 있다.
	= 무효하다는 의미는 해당 페이지가 메인 메모리에 없다.
	\<다시 3가지로 정리\>
	1. 아예 무효하다 : 안 쓴다.
	2. 쓴다 → 어디에 있다?  → 물리 메모리에 있다.
	3. 쓴다 → 어디에 있다? → 물리 메모리에 없다 → 어디에? → swap메모리에 있음 → 어디에?
- 필요한 페이지가 이미 메모리에 상주해있는 경우라고 하면
	- demand 페이징이 있는 것과 없는 것(아닌 것)의 차이는 없다.
- 페이지가 필요한데 만약에 메모리에 상주하지 않았다?
	- 페이지가 메모리에 올라와야한다. 이때는 페이지를 detect하고  swap 디스크에서 메모리로 로드를 해야한다. ⇒ 이렇게 처리함으로써 프로그램 동작을 변경할 필요가 없다.
\<무효 유효 비트를 어떻게 확장해야하는지\>
[image omitted: personal or temporary Notion asset]
- 각 페이지 테이블 항목에는 유효, 무효 bit가 할당된다 → v,(메모리에 있다), i(메모리에 없다)로 표현  
- 이것이 가상 메모리할 때는 물리메모리에 있으면 그대로 되겠지만 물리 메모리에 없는 경우에는 없다가 아니라 swap disk에 있는지 없는지, 물리 메모리에 있는지, 어디에 있는지 swap 디스크도 어디에 있는지 이런 것들을 해야한다.
- i라고 하는 것은 물리 메모리에 없다는 것 = disk에 있는 것을 빨리 메모리에 가져다 놓고 해당 번지로 연결시켜줘야한다. → 그럴때 물리 번지에 없어라고 해야하는데 그 없어라고 해야하는 것을 pase fault라고 표현한다. ⇒ trap이 된다. (sw interrupt) 
- 코드가 실행되다가 번지 없다면 swap disk에서부터 빨리 가지고 와서 물리 메모리에 가져다놓고 그 메모리를 읽어서  그 메모리의 bit i를 v 로바꿔놓고 그 메모리를 읽어서 코드 실행하다 멈췄던 곳으로 다시 가야한다. ⇒ 시간 소요된다.  = 이 과정이 수행되는 동안 기다려야한다. 
	- 전기적으로 수행되다가 갑자기 물리적으로 수행되는 동안 걸리는 시간을 기다려야 하기때문에 이것을 page fault라고 한다. 
[image omitted: personal or temporary Notion asset]
- 몇몇 페이지는 메모리에 있고, 몇몇 페이지는 메모리에 없을 때 (위 상황) 어떨떄 일이 벌어지나?
- 논리 메모리는 page로 나누어져 있다. 
- 중간에 테이블이 있음, 테이블은 0, 2, 5번을 쓰고 있고, 각각의 frame은 4번, 6번, 9번이다.
- 쓰고 있는 부분은 v로 안 쓰고 있는 부분은 i로 세팅되어있음
- 논리 메모리에 있느 모든 페이지는 backing store에 똑같이 있다.
- D를 하려고 했는데 현재 물리 메모리에 없다 = page fault 발생 (내부적으로 발생되고 os가 처리하기 때문에 trap이다.)
- page fault가 생겼을 때 backing store에 가서 물리 메모리로 올려놓고 처리하는 것을 demand paging이 한다.
- 그래서 가상 메모리에서 page fault가 생기면  demand paging이 동작을 해서 물리적 메모리에 가져온다.
\<page fault 처리 순서\>
[image omitted: personal or temporary Notion asset]
- page fault를 처리하는 step
- 어떻게 처리할 것인가?
- interrupt관점에서 보면 page fault가 뜨면 os는 인터럽트가 발생한다(trap) 인터럽트가 생겼으니까 ISR이 실행된다. ISR 을 page fault handler(page fault  처리하는 핸들러)라고 한다.
- 핸들러는 프로그램이다. 핸들러가 동작할 때는 당연히 fault를 만든 프로세스의 수행은 중단되어야한다. 인터럽트가 생기면 원래 하던 일을 stop하고 저장하고 다른 일을 해야한다.  
- 프로그램이 실행되는 것은 전자적인 시간이고 page fault가 생겨서 disk에서 읽어오는 시간은 물리적인 시간이니까 엄청난 차이가 난다.
- 그 기다리는 시간동안 waiting을 시키지 않으면 아무것도 못하게 된다. 그렇기 때문에 인터럽트 처리와 똑같이 저장해놓고 다 읽어 올 때까지 기다려준다. (그 시간동안은 중단)
- 문맥교환을 하기 위해 전부 저장해놔야한다.
- 그러면 그 프로세스는 결국  block상태로 된다. waiting상태 또는 sleep상태라고 표현할 수 있다.
- 현재 수행중인 프로세스가 블록이 되고 페이지 fault 핸들러가 뜨게 된다. 
- 페이지 fault 핸들러는 dma 컨트롤러 (메모리간에 막 복사하는 것) 에게 해당 페이지에 주소를 던져주고 dma를 시작하게 된다. → 외부 메모리에서 내부 메모리로 연속적으로 읽어온다. 
- 그 후에 swap 디바이스에서 물리 메모리로 내용을 쭉 읽어오게 된다.
- 이런 흐름으로 page fault를 처리하게 된다. 
\< 위 과정을 그림으로 표현\>
[image omitted: personal or temporary Notion asset]
1. 페이지에 대한 참조가 생김 
2. 운영체제가 보니까 물리적 메모리에 페이지가 없다 = page fault(mmu가 os에게 trap 발생)
3. 해당 페이지는 swap 디바이스에 다 있음 → backing store에 있는 것을 찾아온다.
4. 물리 메모리에서 free frame을 찾아온다. (빈곳을 찾아내서 거기에다가 가져놔야함)
	→ 비어있는 프레임 = free frame
	디스크 허락(비어있다)을 받았을 때 swap한다. 이때 dma가 동작
5. 복사가 끝나면 너가 원하는 페이지가 있다는 것을 알려주기 위해  table에 i를 v로 바꿔놓는다.
6. 준비가 다 되었으니 원래 상태로 돌아오면 그 메모리를 읽어서 원래 동작을 그대로 한다.
	\<but 바로 이어지는 것이 아님 2\~5 순서가 동작할 때 waiting을 하고 있었기 때문에 다 했어 라고 알려주면 그 때 waiting이 ready로 넘어가서 ready에 있다가 자기 차례가 되면 그때 실행이 된다.
	[image omitted: personal or temporary Notion asset]
- 메모리에 page가 없을 떄( backing store에 있다는 것) 프로세스를 시작하는 경우가 있다.
- os에서 처음 실행 시키는 순간에는 메인메모리에 없음.
- 처음에는 page fault 오류가 생길 수 밖에 없음
- 일단 필요한 모든 페이지를 메모리에 적재시키고 나면 page fault 오류는 처리가 된다.
- 이러한 경우를  pure demand paging 이라고 한다.
- 즉, 어떤 페이지가 필요해지기 전에는 그 페이지를 메모리로 적재하지 않는다 
	= pure demand paging이라고 한다.
- 전혀 없어도 실행할 수 있다 = 필요할 때만 부르면 된다.
- 어떤 명령이 한 명령에서 여러 페이지를 access하는 경우
=어떤 한 명령을 수행할 때도 여러 페이지 fault 오류가 발생할 수 있다.
ex) 메모리에 어떤 명령이 있는데 그 명령이 두개의 숫자를 더한뒤에 그 결과를 메모리에 다시 저장하는 명령이다. 
	1. 메모리에서 명령어를 가지고 온다 (=fatch)
	2. 그 명령을 해석을 해야한다 (= decording)
	3. 이 명령은 여러개의  page에 access 한다는 것을 알 수 있다.
	4. 시스템의 성능이 저하된다. (이것저것 페이지를 해대면 효율 떨어짐)  하지만 이런 성능 저하는  locality 라는 성질로 이론상은 그렇다 하더라도 실제로는 문제가 잘 나타나지 않는다.
		= 페이지를 여러번 참조하더라도 여기저기 떨어져있는 페이지일 가능성은 떨어진다.
		= 데이터와 명령이 같은 page나 주변 page에 보통 옹기종기 모여있음
		→ 이것을 무시하는 경우 = 내가 프로그래밍을 잘 못하는 경우
		ex) 명령이 여기저기 점프하는 경우 (page가 여러개 필요함) 
			데이터가 페이지를 벗아는 경우? → 메모리 참조를 auto변수를 했다가 지역변수도 했다가 전역 변수도 했다가 (변수 자체를 여기저기 씀) , 긴 데이터(배열)를 순서대로 읽지 않고 여기저기 점프하면서 읽을 때  = 효율이 떨어짐
- demand paging을 잘 이용하려면 hw 지원이 필요하다.
	→ 유효, 무효 비트가 있는 페이지 테이블 
	→ 보조 메모리
	→ 명령어 재시작 지원
\<명령어 재시작\>
[image omitted: personal or temporary Notion asset]
- 중요한 내용 : interrupt 
- 인터럽트가 생겻다는 것을 인지하는 시점은? → 바로 인지가 되지는 않음 (delay있음)
	→ 언제? cpu가 명령어 a를 처리하고 있는데 그 순간에 interrupt가 생기면 명령어가 중간에 끊기지 않는다. 명령어가 수행이 다 종료되고 나면 새로운 명령어가 수행되기 전에 그때 인터럽트를 처리한다. (명령어 수행 중간에는 인터럽트가 오건 말건 명령어 자체는 중지되지 않는다)
		= 우리가 쓰는 명령어들은  atomic하다 (중간에 끊기지 않는다)
		= 몇 clock을 사용하든 그clock은 보장이 된다.
- page fault도 인터럽트이다.
- 앞에서 명렁어가 처리되고 있을 때 그 명령이 메모리를 참조하는 것을 가지고 있다. 마무리 하려고 보니까 다른 메모리를 읽어야한다 하지만 그 메모리는 page가 올라와있지 않다. 그 순간 page fault 라는 인터럽트가 생긴다. 하지만 명령어는 뜯어지지 않음→ 어떻게 되는지?
- 명령어가 끝나야 인터럽트가 실행되는데 명령어가 끝나려면 page fault가 처리되어야 한다.
- MOV (SP)+, -(R2) 
	=어떤 레지스터에서 어떤 레지스터를 읽는데 레지스터가 아니고 그 값을 읽어온다. (= 메모리 접근이 있다)
	= +,- 위치에 따라 r2를 감소시키고 sr를 나중에 증가시키고 
	= 명령은 처리해야하는데 메모리 access해야하는 경우가 있다. 
	= page가 다 다르면 page fault 여러번 생김
	→ 해결방안? →   micro code 로 메모리를 읽어올 페이지에 양 블록에 두 끝을  넘어가는지 안넘어가는지 미리 계산을 한다. 페이지가 메모리를 읽지 않는다면 먼저 명령어를 처리하기 전에 page fault 륾 먼저 발생시킨다. 필요하다고 생각되는 메모리를 먼저 갖다놓음.
	미리 갖다 놓았으니까 명령 수행중에는 page fault 가 생기지않음
- 이건 미리 예측을 해야하고 메모리 쓰는 명령마다 이것들을 따로따로 돌려야하니까 조금 효율이 떨어질 수 있으나 해결방안중 하나임
- 다른 해결책 →혹시 명령어 처리를 하다가 명령이 페이지 부재때문에 앞에서 했더니 효율이 떨어진다 → 페이지 부재가 생기면 명령을 취소하면 되겠다 (아니면 이전  상태를 저장할 수 있으면 되겠다)
- 저장해놓고(멈춰놓고) 페이지 부재를 다 해결한 뒤에 그때부터 다시 명령을 처리하면 되겠다.
- 매번 검사하는 것보다는 나을 수 있음
= 프로그램이나 개발자는 몰라야하기 때문에 동작이 스무스해야한다.
이런것 들을 할 수 있는 가장 대표적인 방법 = 명령어 재시작
- 명령어 하다가 페이지 부재 나서 멈추면 페이지 부재 먼저 처리하고 이전에 하던 명령을 원상태로 돌려서 다시 시작해야 한다. → 하드웨어 적으로 동작되어야한다. 
[image omitted: personal or temporary Notion asset]
[image omitted: personal or temporary Notion asset]
- 페이지에 부재가 발생하면 운영체제에서는 보조기억장치에서 원하는 페이지를 주메모리로 가져와야한다. (가져와도 보조기억장치에는 그대로 남아있음)
- 운영체제는 이러한 요구를 충족시키기 위해서 언제든지 할당해서 사용할 수 있는 free frame 집단이 있음
- zero-fill-on-demand → 할당하기 전에 frame을 0으로 만든다.
