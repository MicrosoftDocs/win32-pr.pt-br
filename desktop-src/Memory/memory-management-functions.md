---
description: 'Este tópico descreve as funções de gerenciamento de memória:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Funções de gerenciamento da memória
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: 43aef65e6563a56f35c019c5202827ab65772186
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "103642968"
---
# <a name="memory-management-functions"></a>Funções de gerenciamento da memória

- [Funções de memória geral](#general-memory-functions)
- [Funções de prevenção de execução de dados](#data-execution-prevention-functions)
- [Funções de mapeamento de arquivo](#file-mapping-functions)
- [Funções AWE](#awe-functions)
- [Funções heap](#heap-functions)
- [Funções de memória virtual](#virtual-memory-functions)
- [Funções globais e locais](#global-and-local-functions)
- [Funções de memória inadequadas](#bad-memory-functions)
- [Funções enclave](#enclave-functions)
- [Funções de conversão de ATL](#atl-thunk-functions)
- [Funções obsoletas](#obsolete-functions)

## <a name="general-memory-functions"></a>Funções de memória geral

| Função | Descrição |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registra uma função de chamada de retorno a ser chamada quando um intervalo de memória protegido é liberado ou suas proteções são alteradas. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Copia um bloco de memória de um local para outro. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Cria um objeto de notificação de recurso de memória. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Preenche um bloco de memória com um valor especificado. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Recupera o tamanho mínimo de uma página grande. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Recupera a quantidade de RAM instalada fisicamente no computador. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Recupera os limites de tamanho atuais para o conjunto de trabalho do cache do sistema. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Recupera os endereços das páginas que foram gravadas em uma região de memória virtual. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Obtém informações sobre o uso atual do sistema de memória física e virtual. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Move um bloco de memória de um local para outro. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Recupera o estado do objeto de recurso de memória especificado. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Cancela o registro de uma função de retorno de chamada que foi registrada anteriormente com a função [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) . |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Redefine o estado de rastreamento de gravação para uma região de memória virtual. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Uma função definida pelo aplicativo que é chamada quando um intervalo de memória protegida é liberado ou suas proteções são alteradas. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Preenche um bloco de memória com zeros. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Limita o tamanho do conjunto de trabalho para o cache do sistema de arquivos. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Preenche um bloco de memória com zeros. |

## <a name="data-execution-prevention-functions"></a>Funções de prevenção de execução de dados

Essas funções são usadas com a [prevenção de execução de dados](data-execution-prevention.md) (DEP).

| Função | Descrição |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Recupera as configurações de DEP para um processo. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Recupera as configurações de DEP para o sistema. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Altera as configurações de DEP para um processo. |

## <a name="file-mapping-functions"></a>Funções de mapeamento de arquivo

Essas funções são usadas no [mapeamento de arquivo](file-mapping.md).

| Função | Descrição |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado. Você pode especificar especificar um nó NUMA preferencial para a memória física como um parâmetro estendido; consulte o parâmetro *Extended* . |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado de um aplicativo da Windows Store. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado e especifica o nó NUMA para a memória física. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Grava no disco um intervalo de bytes dentro de uma exibição mapeada de um arquivo. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Verifica se o endereço especificado está dentro de um arquivo mapeado na memória no espaço de endereço do processo especificado. Nesse caso, a função retorna o nome do arquivo mapeado para a memória. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Mapeia uma exibição de um arquivo ou de uma seção com backup em arquivos de paginação no espaço de endereço do processo especificado. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Mapeia uma exibição de um arquivo ou de uma seção com backup em arquivos de paginação no espaço de endereço do processo especificado. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada de um aplicativo da Windows Store. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada. Um chamador pode opcionalmente especificar um endereço de memória sugerido para a exibição. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada e especifica o nó NUMA para a memória física. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada de um aplicativo da Windows Store. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Mapeia uma exibição de um arquivo ou de uma seção com backup em arquivos de paginação no espaço de endereço do processo especificado. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Abre um objeto de mapeamento de arquivo nomeado. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Abre um objeto de mapeamento de arquivo nomeado. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Cancela o mapeamento de uma exibição mapeada de um arquivo do espaço de endereço do processo de chamada. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Cancela o mapeamento de uma exibição mapeada anteriormente de um arquivo ou de uma seção com suporte de paginação. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Cancela o mapeamento de uma exibição mapeada anteriormente de um arquivo ou de uma seção com suporte de paginação. |

## <a name="awe-functions"></a>Funções AWE

Essas são as [funções AWE](address-windowing-extensions.md).

| Função | Descrição |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Aloca páginas de memória física a serem mapeadas e não mapeadas em qualquer região AWE do processo. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Aloca páginas de memória física a serem mapeadas e não mapeadas em qualquer região AWE do processo e especifica o nó NUMA para a memória física. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Libera as páginas de memória física alocadas anteriormente com [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages). |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Mapeia páginas de memória física alocadas anteriormente no endereço especificado em uma região AWE. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Mapeia páginas de memória física alocadas anteriormente no endereço especificado em uma região AWE. |

## <a name="heap-functions"></a>Funções heap

Essas são as [funções de heap](heap-functions.md).

| Função | Descrição |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Obtém um identificador para o heap do processo de chamada. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Obtém identificadores para todos os heaps que são válidos para o processo de chamada. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Aloca um bloco de memória de um heap. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Une blocos livres de memória adjacentes em um heap. |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Cria um objeto de heap. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Destrói o objeto de heap especificado. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Libera um bloco de memória alocado de um heap. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Tenta adquirir o bloqueio associado a um heap especificado. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Recupera informações sobre o heap especificado. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Realoca um bloco de memória de um heap. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Define informações de heap para o heap especificado. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Recupera o tamanho de um bloco de memória alocado de um heap. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Libera a propriedade do bloqueio associado a um heap especificado. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Tenta validar um heap especificado. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Enumera os blocos de memória em um heap especificado. |

## <a name="virtual-memory-functions"></a>Funções de memória virtual

Essas são as [funções de memória virtual](virtual-memory-functions.md).

| Função | Descrição |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Descarta o conteúdo de memória de um intervalo de páginas de memória, sem desconfirmar a memória. O conteúdo da memória descartada é indefinido e deve ser reescrito pelo aplicativo. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Indica que os dados contidos em um intervalo de páginas de memória não são mais necessários para o aplicativo e podem ser descartados pelo sistema, se necessário. |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Pré-busca intervalos de endereços virtuais na memória física. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Retorna informações sobre uma página ou um conjunto de páginas dentro do espaço de endereço virtual do processo especificado. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Recupera um intervalo de páginas de memória que foram oferecidas ao sistema com [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory). |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Fornece CFG com uma lista de destinos de chamada indireto válidos e especifica se eles devem ser marcados como válidos ou não. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Reserva ou confirma uma região de páginas no espaço de endereço virtual do processo de chamada. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Reserva, confirma ou altera o estado de uma região de memória dentro do espaço de endereço virtual de um processo especificado. A função inicializa a memória alocada para zero. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserva, confirma ou altera o estado de uma região de páginas no espaço de endereço virtual do processo de chamada. A memória alocada por essa função é inicializada automaticamente como zero. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserva ou confirma uma região de páginas no espaço de endereço virtual do processo especificado. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Reserva ou confirma uma região de memória dentro do espaço de endereço virtual do processo especificado e especifica o nó NUMA para a memória física. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserva, confirma ou altera o estado de uma região de páginas no espaço de endereço virtual do processo de chamada. A memória alocada por essa função é inicializada automaticamente como zero. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Libera ou desconfirma uma região de páginas dentro do espaço de endereço virtual do processo de chamada. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Libera ou desconfirma uma região de memória dentro do espaço de endereço virtual de um processo especificado. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Bloqueia a região especificada do espaço de endereço virtual do processo na memória física. |
| [**Usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Altera a proteção de acesso em uma região de páginas confirmadas no espaço de endereço virtual do processo de chamada. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Altera a proteção de acesso em uma região de páginas confirmadas no espaço de endereço virtual do processo de chamada. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Altera a proteção em uma região de páginas confirmadas no espaço de endereço virtual do processo de chamada. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Fornece informações sobre um intervalo de páginas no espaço de endereço virtual do processo de chamada. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Fornece informações sobre um intervalo de páginas no espaço de endereço virtual do processo de chamada. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Desbloqueia um intervalo de páginas especificado no espaço de endereço virtual de um processo. |

## <a name="global-and-local-functions"></a>Funções globais e locais

Consulte também [funções globais e locais](global-and-local-functions.md). Essas funções são fornecidas para compatibilidade com o Windows de 16 bits e são usadas com troca dinâmica de dados (DDE), as funções da área de transferência e os objetos de dados OLE. A menos que a documentação declare especificamente que uma função global ou local deve ser usada, novos aplicativos devem usar a [função de heap](heap-functions.md) correspondente com o identificador retornado por [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Para obter a funcionalidade equivalente à função global ou local, defina o parâmetro *dwFlags* da função de heap como 0.

| Função | Descrição | Função de heap correspondente |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Aloca o número especificado de bytes a partir do heap. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Descarta o bloco de memória global especificado. | Não aplicável. |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Retorna informações sobre o objeto de memória global especificado. | Não aplicável. Use [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) para validar o heap. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Libera o objeto de memória global especificado. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Recupera o identificador associado ao ponteiro especificado para um bloco de memória global. Essa função deve ser usada somente com funções OLE e de área de transferência que a exigem. | Não aplicável. |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Bloqueia um objeto de memória global e retorna um ponteiro para o primeiro byte do bloco de memória do objeto. | Não aplicável. |
| [**GlobalRealloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Altera o tamanho ou os atributos de um objeto de memória global especificado. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **Localize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Recupera o tamanho atual do objeto de memória global especificado. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Decrementa a contagem de bloqueios associada a um objeto de memória. Essa função deve ser usada somente com funções OLE e de área de transferência que a exigem. | Não aplicável. |

## <a name="bad-memory-functions"></a>Funções de memória inadequadas

| Função | Descrição |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Uma função definida pelo aplicativo registrada com a função [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) que é chamada quando uma ou mais páginas de memória inválidos são detectadas. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Obtém os recursos de tratamento de erro de memória do sistema. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registra uma notificação de memória inadequada que é chamada quando uma ou mais páginas de memória inválidos são detectadas. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Fecha o identificador de notificação de memória insuficiente especificado. |

## <a name="enclave-functions"></a>Funções enclave

| Função | Descrição |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Cria um novo enclave não inicializado. Um enclave é uma região isolada de código e dados dentro do espaço de endereço de um aplicativo. Somente o código que é executado no enclave pode acessar dados dentro do mesmo enclave. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Inicializa um enclave que você criou e carregou com dados. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Recupera se há suporte para o tipo especificado de enclave. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Carrega dados em um enclave não inicializado que você criou chamando [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave). |

## <a name="atl-thunk-functions"></a>Funções de conversão de ATL

| Função | Descrição |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Aloca espaço na memória para uma conversão ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Retorna uma função executável correspondente ao parâmetro AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Libera a memória associada a uma conversão ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Inicializa uma conversão ATL. |

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows:

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

A função abaixo pode retornar informações incorretas e não deve ser usada. Em vez disso, use a função [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) .

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)