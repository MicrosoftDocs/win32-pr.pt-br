---
description: Toda a memória que um processo aloca usando as funções de alocação de memória (HeapAlloc, VirtualAlloc, GlobalAlloc ou LocalAlloc) é acessível somente para o processo.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Escopo da memória alocada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164637"
---
# <a name="scope-of-allocated-memory"></a>Escopo da memória alocada

Toda a memória que um processo aloca usando as funções de alocação de memória ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) é acessível somente para o processo. No entanto, a memória alocada por uma DLL é alocada no espaço de endereço do processo que chamou a DLL e não pode ser acessada por outros processos usando a mesma DLL. Para criar a memória compartilhada, você deve usar o mapeamento de arquivo.

O mapeamento de arquivo nomeado fornece uma maneira fácil de criar um bloco de memória compartilhada. Um processo pode especificar um nome quando ele usa a função [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para criar um objeto de mapeamento de arquivo. Outros processos podem especificar o mesmo nome para a função **CreateFileMapping** ou [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) para obter um identificador para o objeto de mapeamento.

Cada processo especifica seu identificador para o objeto de mapeamento de arquivo na função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) para mapear uma exibição do arquivo para seu próprio espaço de endereço. As exibições de todos os processos para um único objeto de mapeamento de arquivo são mapeadas para as mesmas páginas compartilháveis do armazenamento físico. No entanto, os endereços virtuais das exibições mapeadas podem variar de um processo para outro, a menos que a função [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) seja usada para mapear a exibição em um endereço especificado. Embora compartilháveis, as páginas de armazenamento físico usadas para uma exibição de arquivo mapeada não são globais; Eles não podem ser acessados por processos que não mapearam uma exibição do arquivo.

Todas as páginas confirmadas por meio do mapeamento de uma exibição de um arquivo são liberadas quando o último processo com uma exibição do objeto de mapeamento termina ou desmapeia sua exibição chamando a função [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) . Neste momento, o arquivo especificado (se houver) associado ao objeto de mapeamento é atualizado. Um arquivo especificado também pode ser forçado a Atualizar chamando a função [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Para obter mais informações, consulte [mapeamento de arquivo](file-mapping.md). Para obter um exemplo de memória compartilhada em uma DLL, consulte [usando a memória compartilhada em uma biblioteca de Dynamic-Link](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Se vários processos tiverem acesso de gravação à memória compartilhada, você deverá sincronizar o acesso à memória. Para obter mais informações, consulte [sincronização](../sync/synchronization.md).

 

 
