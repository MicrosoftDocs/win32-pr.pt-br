---
description: O conjunto de trabalho de um processo é o conjunto de páginas no espaço de endereço virtual do processo que estão atualmente residentes na memória física.
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: Conjunto de Trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4985e7eb526d5dda8469ccc2f46bfe6fd050c745
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549888"
---
# <a name="working-set"></a>Conjunto de Trabalho

O conjunto de trabalho de um processo é o conjunto de páginas no espaço de endereço virtual do processo que estão atualmente residentes na memória física. O conjunto de trabalho contém apenas alocações de memória paginável; as alocações de memória não paginável, como [extensões](address-windowing-extensions.md) AWE ou de [página grande](large-page-support.md) , não são incluídas no conjunto de trabalho do.

Quando um processo faz referência à memória paginável que não está em seu conjunto de trabalho no momento, ocorre uma *falha de página* . O manipulador de falhas de página do sistema tenta resolver a falha de página e, se tiver sucesso, a página será adicionada ao conjunto de trabalho. (O acesso às alocações AWE ou de página grande nunca causa uma falha de página, pois essas alocações não são paginável.)

Uma *falha de página de hardware* deve ser resolvida lendo o conteúdo da página no *repositório de backup* da página, que é o arquivo de paginação do sistema ou um arquivo mapeado por memória criado pelo processo. Uma *falha de página flexível* pode ser resolvida sem acessar o armazenamento de backup. Uma falha de página flexível ocorre quando:

-   A página está no conjunto de trabalho de algum outro processo, portanto, ela já está residente na memória.
-   A página está em transição, pois ela foi removida dos conjuntos de trabalho de todos os processos que estavam usando a página e ainda não foi realocada ou já está residente como resultado de uma operação de pré-busca do Gerenciador de memória.
-   Um processo faz referência a uma página virtual alocada pela primeira vez (às vezes chamado de *falha de demanda zero*).

As páginas podem ser removidas de um conjunto de trabalho de processo como resultado das seguintes ações:

-   O processo reduz ou esvazia o conjunto de trabalho chamando a função [**SetProcessWorkingSetSize**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize), [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) ou [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) .
-   O processo chama a função [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) em um intervalo de memória que não está bloqueado.
-   O processo cancela o mapeamento de uma exibição mapeada de um arquivo usando a função [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) .
-   O Gerenciador de memória corta as páginas do conjunto de trabalho para criar mais memória disponível.
-   O Gerenciador de memória deve remover uma página do conjunto de trabalho para liberar espaço para uma nova página (por exemplo, porque o conjunto de trabalho está em seu tamanho máximo).

Se vários processos compartilharem uma página, a remoção da página do conjunto de trabalho de um processo não afetará outros processos. Depois que uma página é removida dos conjuntos de trabalho de todos os processos que o estavam usando, a página se torna uma *página de transição*. As páginas de transição permanecem armazenadas em cache na RAM até que a página seja referenciada novamente por algum processo ou seja realocada (por exemplo, preenchida com zeros e dada a outro processo). Se uma página de transição tiver sido modificada desde a última gravação no disco (ou seja, se a página for "suja"), a página deverá ser gravada em seu repositório de backup antes de poder ser realocada. O sistema pode começar a gravar páginas de transição sujas em seu armazenamento de backup assim que essas páginas ficarem disponíveis.

Cada processo tem um tamanho de conjunto de trabalho mínimo e máximo que afeta o comportamento de paginação da memória virtual do processo. Para obter o tamanho atual do conjunto de trabalho de um processo especificado, use a função [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) . Para obter ou alterar os tamanhos mínimo e máximo do conjunto de trabalho, use as funções [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) e [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) .

A interface de programação de aplicativo de status do processo (PSAPI) fornece várias funções que retornam informações detalhadas sobre o conjunto de trabalho de um processo. Para obter detalhes, consulte [informações do conjunto de trabalho](../psapi/working-set-information.md).

 

 
