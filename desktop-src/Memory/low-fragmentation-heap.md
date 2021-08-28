---
description: A fragmentação de heap é um estado no qual a memória disponível é dividida em blocos pequenos e não contíguos.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap de baixa fragmentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d4cc6f7f0e2427a20532f5e32cc1460f9b6601d1e6dddf0de603757895005e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067736"
---
# <a name="low-fragmentation-heap"></a>Heap de baixa fragmentação

\[As informações neste tópico se aplica ao Windows Server 2003 e Windows XP. A partir do Windows Vista, o sistema usa o LFH (heap de baixa fragmentação) conforme necessário para as solicitações de alocação de memória de serviço. Os aplicativos não precisam habilitar o LFH para seus heaps.\]

A fragmentação de heap é um estado no qual a memória disponível é dividida em blocos pequenos e não contíguos. Quando um heap é fragmentado, a alocação de memória pode falhar mesmo quando a memória total disponível no heap é suficiente para atender a uma solicitação, porque nenhum único bloco de memória é grande o suficiente. O LFH (heap de baixa fragmentação) ajuda a reduzir a fragmentação do heap.

O LFH não é um heap separado. Em vez disso, é uma política que os aplicativos podem habilitar para seus heaps. Quando o LFH está habilitado, o sistema aloca memória em determinados tamanhos predeterminados. Quando um aplicativo solicita uma alocação de memória de um heap que tem o LFH habilitado, o sistema aloca o menor bloco de memória que é grande o suficiente para conter o tamanho solicitado. O sistema não usa o LFH para alocações maiores que 16 KB, independentemente de o LFH ser habilitado ou não.

Um aplicativo deve habilitar o LFH somente para o heap padrão do processo de chamada ou para [heaps](heap-functions.md) privados que o aplicativo criou. Para habilitar o LFH para um heap, use a função [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) para obter um lidar com o heap padrão do processo de chamada ou use o alça para um heap privado criado pela função [**HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) Em seguida, chame [**a função HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) com o handle.

O LFH não pode ser habilitado para heaps criados com **HEAP \_ NO \_ SERIALIZE** ou para heaps criados com um tamanho fixo. O LFH também não poderá ser habilitado se você estiver usando as ferramentas de depuração de heap nas Ferramentas [de Depuração para Windows](/windows-hardware/drivers/debugger/) ou Microsoft [Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Depois que o LFH tiver sido habilitado para um heap, ele não poderá ser desabilitado.

Os aplicativos que mais se beneficiam do LFH são aplicativos multithread que alocam memória com frequência e usam uma variedade de tamanhos de alocação abaixo de 16 KB. No entanto, nem todos os aplicativos se beneficiam do LFH. Para avaliar os efeitos da habilitação do LFH em seu aplicativo, use os dados de criação de perfil de desempenho.

 

 
