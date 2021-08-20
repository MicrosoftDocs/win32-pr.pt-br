---
description: Cada processo tem um heap padrão fornecido pelo sistema. Aplicativos que fazem alocações frequentes do heap podem melhorar o desempenho usando heaps privados.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funções de heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8171b75abf879eb50204d55541557bdbf5359bd1e8f956d147e49a9d61656d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067816"
---
# <a name="heap-functions"></a>Funções de heap

Cada processo tem um heap padrão fornecido pelo sistema. Aplicativos que fazem alocações frequentes do heap podem melhorar o desempenho usando heaps privados.

Um heap privado é um bloco de uma ou mais páginas no espaço de endereço do processo de chamada. Depois de criar o heap privado, o processo usa funções como [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) e [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para gerenciar a memória nesse heap.

As funções de heap também podem ser usadas para gerenciar a memória no heap padrão do processo, usando o handle retornado pela [**função GetProcessHeap.**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) Novos aplicativos devem usar as funções de heap em vez das [funções globais](global-and-local-functions.md) e locais para essa finalidade.

Não há nenhuma diferença entre a memória alocada de um heap privado e a alocada usando as outras funções de alocação de memória. Para ver uma lista completa de funções, consulte a tabela em [Funções de Gerenciamento de Memória](memory-management-functions.md).

> [!Note]  
> Um thread deve chamar funções de heap somente para o heap padrão do processo e heaps privados que o thread cria e gerencia, usando os alças retornados pela [**função GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) ou [**HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate)

 

A [**função HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) cria um objeto heap privado do qual o processo de chamada pode alocar blocos de memória usando a [**função HeapAlloc.**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) **HeapCreate** especifica um tamanho inicial e um tamanho máximo para o heap. O tamanho inicial determina o número de páginas de leitura/gravação comprometidas inicialmente alocadas para o heap. O tamanho máximo determina o número total de páginas reservadas. Essas páginas criam um bloco contíguo no espaço de endereço virtual de um processo no qual o heap pode crescer. Páginas adicionais são confirmadas automaticamente desse espaço reservado se as solicitações por **HeapAlloc** excederem o tamanho atual das páginas confirmadas, supondo que o armazenamento físico para ele está disponível. Depois que as páginas são confirmadas, elas não são confirmadas até que o processo seja encerrado ou até que o heap seja destruído chamando a [**função HeapDume.**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy)

A memória de um objeto de heap privado só pode ser acessada pelo processo que o criou. Se uma DLL (biblioteca de vínculo dinâmico) cria um heap privado, ela faz isso no espaço de endereço do processo que chamou a DLL. Ele só pode ser acessado por esse processo.

A [**função HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) aloca um número especificado de bytes de um heap privado e retorna um ponteiro para o bloco alocado. Esse ponteiro pode ser usado nas funções [**HeapFree,**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) [**HeapReAlloc,**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)e [**HeapValidate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate)

A memória alocada [**por HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) não é móvel. O endereço retornado por **HeapAlloc é** válido até que o bloco de memória seja liberado ou realocado; O bloco de memória não precisa ser bloqueado.

Como o sistema não pode compactar um heap privado, ele pode se tornar fragmentado. Aplicativos que alocam grandes quantidades de memória em vários tamanhos de alocação podem usar o heap de [baixa fragmentação](low-fragmentation-heap.md) para reduzir a fragmentação do heap.

Um possível uso para as funções de heap é criar um heap privado quando um processo é iniciado, especificando um tamanho inicial suficiente para atender aos requisitos de memória do processo. Se a chamada para a [**função HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) falhar, o processo poderá encerrar ou notificar o usuário da falta de memória; se ele for bem-sucedido, no entanto, o processo terá a certeza de ter a memória de que precisa.

A memória solicitada pelo [**HeapCriar**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) pode ou não ser contígua. A memória alocada em um heap [**por HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) é contígua. Você não deve gravar ou ler da memória em um heap, exceto pelo alocado por **HeapAlloc,** nem deve assumir nenhuma relação entre duas áreas de memória alocadas por **HeapAlloc**.

Você não deve se referir de forma alguma à memória que tenha sido liberada pelo [**HeapFree.**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) Depois que a memória é liberada, todas as informações que podem ter estado nele se foram para sempre. Se você precisar de informações, não liberar memória contendo as informações. Chamadas de função que retornam informações sobre a memória (como [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) podem não ser usadas com memória liberada, pois podem retornar dados falsos.

A [**função HeapDumey**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) destrói um objeto de heap privado. Ele delimita e libera todas as páginas do objeto heap e invalida o identificador para o heap.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



