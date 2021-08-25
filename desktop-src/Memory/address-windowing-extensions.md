---
description: AWE (Extensões de Janela de Endereço) é um conjunto de extensões que permite que um aplicativo manipule rapidamente a memória física maior que 4 GB.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Extensões de janela de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764406"
---
# <a name="address-windowing-extensions"></a>Extensões de janela de endereço

AWE (Extensões de Janela de Endereço) é um conjunto de extensões que permite que um aplicativo manipule rapidamente a memória física maior que 4 GB. Determinados aplicativos com uso intensivo de dados, como sistemas de gerenciamento de banco de dados e software científico e de engenharia, precisam de acesso a caches muito grandes de dados. No caso de conjuntos de dados muito grandes, restringir o cache para se ajustar aos 2 GB de espaço de endereço do usuário de um aplicativo é uma restrição grave. Nessas situações, o cache é muito pequeno para dar suporte corretamente ao aplicativo.

O AWE resolve esse problema permitindo que os aplicativos resolvam diretamente grandes quantidades de memória enquanto continuam a usar ponteiros de 32 bits. O AWE permite que os aplicativos tenham caches de dados maiores que 4 GB (em que há memória física suficiente). O AWE usa exibições físicas de memória e janela não papagadas de várias partes dessa memória física dentro de um espaço de endereço virtual de 32 bits.

O AWE coloca algumas restrições sobre como essa memória pode ser usada, principalmente porque essas restrições permitem mapeamento, remapeamento e liberação extremamente rápidos. O gerenciamento rápido de memória é importante para esses espaços de endereço potencialmente enormes.

-   Os intervalos de endereços virtuais alocados para o AWE não são compartilháveis com outros processos (e, portanto, não herdáveis). Na verdade, dois endereços virtuais AWE diferentes dentro do mesmo processo não têm permissão para mapear a mesma página física. Essas restrições fornecem remapeamento e limpeza rápidos quando a memória é liberada.
-   As páginas físicas que podem ser alocadas para uma região do AWE são limitadas pelo número de páginas físicas presentes no computador, pois essa memória nunca é paginada – ela é bloqueada até que o aplicativo a libera explicitamente ou sai. As páginas físicas alocadas para um determinado processo podem ser mapeadas para qualquer região virtual do AWE dentro do mesmo processo. Os aplicativos que usam o AWE devem ter cuidado para não levar tanto memória física que fazem com que outros aplicativos sejam páginados excessivamente ou impeçam a criação de novos processos ou threads devido à falta de recursos. Use a [**função GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) para monitorar o uso de memória física.
-   Os endereços virtuais do AWE são sempre de leitura/gravação e não podem ser protegidos por meio de chamadas para [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (ou seja, nenhuma memória somente leitura, memória sem acesso, páginas de proteção e outros como podem ser especificados).
-   Os intervalos de endereços AWE não podem ser usados para buffer de dados para gráficos ou chamadas de vídeo.
-   Um intervalo de memória do AWE não pode ser dividido, nem partes dele podem ser excluídas. Em vez disso, todo o intervalo de endereços virtuais deve ser excluído como uma unidade quando a exclusão é necessária. Isso significa que você deve especificar **MEM \_ RELEASE** ao chamar [**VirtualFree.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)
-   Os aplicativos podem mapear várias regiões simultaneamente, desde que não se sobreponham.
-   Não há suporte para aplicativos que usam a AWE no modo de emulação. Ou seja, um aplicativo x86 que usa funções AWE deve ser recompilado para ser executado em outro processador, enquanto a maioria dos aplicativos pode ser executado sem recompilar em um emulador em outras plataformas.

Essa solução resolve os problemas de memória física de maneira muito geral e amplamente aplicável. Alguns dos benefícios do AWE são:

-   Um pequeno grupo de novas funções é definido para manipular a memória AWE.
-   O AWE fornece uma funcionalidade de remapeamento muito rápida. O remapeamento é feito manipulando tabelas de memória virtual, não movendo dados na memória física.
-   O AWE fornece granularidade de tamanho de página apropriada para o processador (por exemplo, 4 KB em x86), que é mais útil para aplicativos do que páginas grandes (por exemplo, 2 MB ou 4 MB em x86).

Um aplicativo deve ter o privilégio Bloquear Páginas na Memória para usar o AWE. Para obter esse privilégio, um administrador deve adicionar **Páginas de Bloqueio na** Memória às Atribuições de Direitos de Usuário do **usuário.** Para obter mais informações sobre como fazer isso, consulte "Direitos de usuário" na ajuda do sistema operacional.

As funções a seguir comem a API AWE (Extensões de Janela de Endereço).



| Função                                                                          | Descrição                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserve uma parte do espaço de endereço virtual a ser usada para o AWE, usando **MEM \_ PHYSICAL.**                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Alocar memória física para uso com o AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Mapeie (ou invalide) endereços virtuais do AWE em qualquer conjunto de páginas físicas obtidas com [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Mapeie (ou invalide) endereços virtuais do AWE em qualquer conjunto de páginas físicas obtidas com [**AllocateUserPhysicalPages,**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)mas com um controle mais fino do que o fornecido por [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Memória física livre que foi usada para o AWE.                                                                                                                                                                                                               |



 

 

 
