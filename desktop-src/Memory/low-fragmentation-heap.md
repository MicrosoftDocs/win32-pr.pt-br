---
description: A fragmentação de heap é um estado no qual a memória disponível é quebrada em blocos pequenos e não contíguos.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap de baixa fragmentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792503"
---
# <a name="low-fragmentation-heap"></a>Heap de baixa fragmentação

\[As informações neste tópico se aplicam ao Windows Server 2003 e ao Windows XP. A partir do Windows Vista, o sistema usa o LFH (heap de baixa fragmentação) conforme necessário para solicitações de alocação de memória de serviço. Os aplicativos não precisam habilitar o LFH para seus heaps.\]

A fragmentação de heap é um estado no qual a memória disponível é quebrada em blocos pequenos e não contíguos. Quando um heap é fragmentado, a alocação de memória pode falhar mesmo quando a memória total disponível no heap é suficiente para atender a uma solicitação, porque nenhum bloco de memória é grande o suficiente. O heap de baixa fragmentação (LFH) ajuda a reduzir a fragmentação do heap.

O LFH não é um heap separado. Em vez disso, é uma política que os aplicativos podem habilitar para seus heaps. Quando o LFH está habilitado, o sistema aloca memória em determinados tamanhos predeterminados. Quando um aplicativo solicita uma alocação de memória de um heap que tem o LFH habilitado, o sistema aloca o menor bloco de memória que é grande o suficiente para conter o tamanho solicitado. O sistema não usa o LFH para alocações com mais de 16 KB, independentemente de o LFH estar ou não habilitado.

Um aplicativo deve habilitar o LFH somente para o heap padrão do processo de chamada ou para [heaps particulares](heap-functions.md) que o aplicativo criou. Para habilitar o LFH para um heap, use a função [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) para obter um identificador para o heap padrão do processo de chamada ou use o identificador para um heap privado criado pela função [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) . Em seguida, chame a função [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) com a alça.

O LFH não pode ser habilitado para heaps criados com **heap \_ sem \_ serialização** ou para heaps criados com um tamanho fixo. O LFH também não poderá ser habilitado se você estiver usando as ferramentas de depuração de heap em [ferramentas de depuração para Windows](/windows-hardware/drivers/debugger/) ou [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Depois que o LFH tiver sido habilitado para um heap, ele não poderá ser desabilitado.

Aplicativos que se beneficiam mais do LFH são aplicativos multissegmentados que alocam memória com frequência e usam uma variedade de tamanhos de alocação abaixo de 16 KB. No entanto, nem todos os aplicativos se beneficiam do LFH. Para avaliar os efeitos de habilitar o LFH em seu aplicativo, use dados de criação de perfil de desempenho.

 

 
