---
description: Cada processo tem um heap padrão fornecido pelo sistema. Os aplicativos que fazem alocações frequentes do heap podem melhorar o desempenho usando heaps particulares.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funções de heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828260"
---
# <a name="heap-functions"></a>Funções de heap

Cada processo tem um heap padrão fornecido pelo sistema. Os aplicativos que fazem alocações frequentes do heap podem melhorar o desempenho usando heaps particulares.

Um heap privado é um bloco de uma ou mais páginas no espaço de endereço do processo de chamada. Depois de criar o heap privado, o processo usa funções como [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) e [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) para gerenciar a memória nesse heap.

As funções de heap também podem ser usadas para gerenciar a memória no heap padrão do processo, usando o identificador retornado pela função [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) . Os novos aplicativos devem usar as funções de heap em vez das [funções globais e locais](global-and-local-functions.md) para essa finalidade.

Não há nenhuma diferença entre a memória alocada de um heap privado e alocada usando as outras funções de alocação de memória. Para obter uma lista completa de funções, consulte a tabela em [funções de gerenciamento de memória](memory-management-functions.md).

> [!Note]  
> Um thread deve chamar funções de heap somente para o heap padrão do processo e heaps privados que o thread cria e gerencia, usando identificadores retornados pela função [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) ou [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) .

 

A função [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) cria um objeto heap privado do qual o processo de chamada pode alocar blocos de memória usando a função [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) . **HeapCreate** especifica um tamanho inicial e um tamanho máximo para o heap. O tamanho inicial determina o número de páginas confirmadas de leitura/gravação inicialmente alocadas para o heap. O tamanho máximo determina o número total de páginas reservadas. Essas páginas criam um bloco contíguo no espaço de endereço virtual de um processo no qual o heap pode crescer. Páginas adicionais serão confirmadas automaticamente desse espaço reservado se as solicitações por **HeapAlloc** excederem o tamanho atual das páginas confirmadas, supondo que o armazenamento físico para ela esteja disponível. Depois que as páginas são confirmadas, elas não são confirmadas até que o processo seja encerrado ou até que o heap seja destruído chamando a função [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) .

A memória de um objeto heap privado é acessível somente para o processo que o criou. Se uma DLL (biblioteca de vínculo dinâmico) criar um heap privado, ele fará isso no espaço de endereço do processo que chamou a DLL. Ele só pode ser acessado por esse processo.

A função [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) aloca um número especificado de bytes de um heap privado e retorna um ponteiro para o bloco alocado. Esse ponteiro pode ser usado nas funções [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**heapsize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)e [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) .

A memória alocada por [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) não é móvel. O endereço retornado por **HeapAlloc** é válido até que o bloco de memória seja liberado ou realocado; o bloco de memória não precisa ser bloqueado.

Como o sistema não pode compactar um heap privado, ele pode se tornar fragmentado. Os aplicativos que alocam grandes quantidades de memória em vários tamanhos de alocação podem usar o [heap de baixa fragmentação](low-fragmentation-heap.md) para reduzir a fragmentação de heap.

Um possível uso para as funções de heap é criar um heap privado quando um processo é iniciado, especificando um tamanho inicial suficiente para atender aos requisitos de memória do processo. Se a chamada para a função [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) falhar, o processo poderá encerrar ou notificar o usuário sobre a falta de memória; no entanto, se tiver sucesso, o processo será garantido de ter a memória de que precisa.

A memória solicitada por [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) pode ou não ser contígua. A memória alocada em um heap por [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) é contígua. Você não deve gravar na memória ou lê-la em um heap, exceto pelo que foi alocado por **HeapAlloc**, nem deve assumir qualquer relação entre duas áreas de memória alocadas por **HeapAlloc**.

Você não deve se referir a nenhuma forma de memória que foi liberada por [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree). Depois que a memória é liberada, todas as informações que podem estar em si não são feitas para sempre. Se você precisar de informações, não Libere memória que contenha as informações. As chamadas de função que retornam informações sobre a memória (como [**heapsize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) não podem ser usadas com memória liberada, pois podem retornar dados falsos.

A função [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) destrói um objeto heap privado. Ele desconfirma e libera Todas as páginas do objeto heap e invalida o identificador para o heap.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



