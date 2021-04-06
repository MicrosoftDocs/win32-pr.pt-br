---
description: Extensões AWE são um conjunto de extensões que permite que um aplicativo manipule rapidamente a memória física superior a 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Extensões de janelas de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cb311bf9ecef2de334018ca3f9982a31f0b072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828263"
---
# <a name="address-windowing-extensions"></a>Extensões de janelas de endereço

Extensões AWE são um conjunto de extensões que permite que um aplicativo manipule rapidamente a memória física superior a 4 GB. Determinados aplicativos com uso intensivo de dados, como sistemas de gerenciamento de bancos de dados e software científico e de engenharia, precisam de acesso a caches muito grandes de data. No caso de conjuntos de dados muito grandes, restringir o cache para se ajustar dentro de 2GB de espaço de endereço de usuário de um aplicativo é uma restrição severa. Nessas situações, o cache é muito pequeno para dar suporte adequado ao aplicativo.

O AWE resolve esse problema permitindo que os aplicativos resolvam diretamente enormes quantidades de memória enquanto continuam a usar ponteiros de 32 bits. O AWE permite que os aplicativos tenham caches de dados maiores que 4GB (em que há memória física suficiente). O AWE usa a memória física não paginável e exibições de janela de várias partes dessa memória física em um espaço de endereço virtual de 32 bits.

O AWE coloca algumas restrições sobre como essa memória pode ser usada, principalmente porque essas restrições permitem mapeamento extremamente rápido, remapeamento e liberação. O gerenciamento rápido de memória é importante para esses espaços de endereço potencialmente enormes.

-   Os intervalos de endereços virtuais alocados para o AWE não são compartilháveis com outros processos (e, portanto, não podem ser herdados). Na verdade, dois endereços virtuais AWE diferentes dentro do mesmo processo não têm permissão para mapear a mesma página física. Essas restrições fornecem remapeamento rápido e limpeza quando a memória é liberada.
-   As páginas físicas que podem ser alocadas para uma região AWE são limitadas pelo número de páginas físicas presentes no computador, já que essa memória nunca é paginada – ela é bloqueada até que o aplicativo a libere explicitamente ou saia. As páginas físicas alocadas para um determinado processo podem ser mapeadas para qualquer região virtual do AWE dentro do mesmo processo. Os aplicativos que usam o AWE devem ter cuidado para não tomar muita memória física que fazem com que outros aplicativos façam a página excessivamente ou impeçam a criação de novos processos ou threads devido à falta de recursos. Use a função [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) para monitorar o uso da memória física.
-   Os endereços virtuais AWE são sempre de leitura/gravação e não podem ser protegidos por meio de chamadas para [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (ou seja, nenhuma memória somente leitura, memória NoAccess, páginas de proteção e similares podem ser especificados).
-   Os intervalos de endereços AWE não podem ser usados para armazenar dados em buffer para chamadas de vídeo ou gráficos.
-   Um intervalo de memória AWE não pode ser dividido, nem pode ser excluído. Em vez disso, todo o intervalo de endereços virtuais deve ser excluído como uma unidade quando a exclusão é necessária. Isso significa que você deve especificar a **\_ versão mem** ao chamar [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree).
-   Os aplicativos podem mapear várias regiões simultaneamente, desde que elas não se sobreponham.
-   Não há suporte para aplicativos que usam AWE no modo de emulação. Ou seja, um aplicativo x86 que usa funções AWE deve ser recompilado para ser executado em outro processador, enquanto a maioria dos aplicativos pode ser executada sem a recompilação em um emulador em outras plataformas.

Essa solução resolve os problemas de memória física de maneira muito geral e amplamente aplicável. Alguns dos benefícios do AWE são:

-   Um pequeno grupo de novas funções é definido para manipular a memória AWE.
-   O AWE fornece um recurso de remapeamento muito rápido. O remapeamento é feito pela manipulação de tabelas de memória virtual, não pela movimentação de dados na memória física.
-   O AWE fornece granularidade de tamanho de página apropriada ao processador (por exemplo, 4 KB no x86), que é mais útil para aplicativos do que páginas grandes (por exemplo, 2 MB ou 4 MB no x86).

Um aplicativo deve ter o privilégio bloquear páginas na memória para usar o AWE. Para obter esse privilégio, um administrador deve adicionar **páginas de bloqueio na memória** para as **atribuições de direitos de usuário** do usuário. Para obter mais informações sobre como fazer isso, consulte "direitos de usuário" na ajuda do sistema operacional.

As funções a seguir compõem a API de extensões do Windows (AWE).



| Função                                                                          | Descrição                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserve uma parte do espaço de endereço virtual a ser usada para AWE, usando o **mem \_ físico**.                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Aloque memória física para uso com o AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Mapeie (ou invalidar) endereços virtuais AWE em qualquer conjunto de páginas físicas obtidas com [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Mapeie (ou invalida) endereços virtuais AWE em qualquer conjunto de páginas físicas obtidas com [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages), mas com um controle mais preciso do que o fornecido pelo [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memória física livre que foi usada para AWE.                                                                                                                                                                                                               |



 

 

 
