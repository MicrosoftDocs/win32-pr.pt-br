---
Description: A seguir, uma breve comparação dos vários métodos de alocação de memória.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparando métodos de alocação de memória
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 418ebbf96b1d6f714e1ae7f23f1c15e918ea0c6fa7eabdf7bb9157bb14808bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067896"
---
# <a name="comparing-memory-allocation-methods"></a>Comparando métodos de alocação de memória

Veja a seguir uma breve comparação dos vários métodos de alocação de memória:

-   [**Cotaskmemalloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**Globalalloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**Heapalloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**Localalloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **novo**
-   [**Virtualalloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Embora as funções [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc,**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) em última análise, aloquem memória do mesmo heap, cada uma fornece um conjunto ligeiramente diferente de funcionalidades. Por exemplo, **HeapAlloc** pode ser instruído a criar uma exceção se a memória não puder ser alocada, uma funcionalidade não disponível com **LocalAlloc**. **LocalAlloc dá** suporte à alocação de alças que permitem que a memória subjacente seja movida por uma realocação sem alterar o valor do handle, uma funcionalidade não disponível com **HeapAlloc**.

A partir do Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) são implementados como funções de wrapper que chamam [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando um handle para o heap padrão do processo. Portanto, **GlobalAlloc** e **LocalAlloc** têm maior sobrecarga do que **HeapAlloc.**

Como os alocadores de heap diferentes fornecem funcionalidades distintas usando mecanismos diferentes, você deve liberar memória com a função correta. Por exemplo, a memória alocada com [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve ser liberada [**com HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e não [**com LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ou [**GlobalFree.**](/windows/desktop/api/WinBase/nf-winbase-globalfree) A memória alocada [**com GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve ser consultada, validada e liberada com a função global ou local correspondente.

A [**função VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) permite que você especifique opções adicionais para alocação de memória. No entanto, suas alocações usam uma granularidade de página, portanto, usar **VirtualAlloc** pode resultar em maior uso de memória.

A **função malloc** tem a desvantagem de ser dependente de tempo de run-time. O **novo** operador tem a desvantagem de ser dependente do compilador e dependente de idioma.

A [**função CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tem a vantagem de funcionar bem em C, C++ ou Visual Basic. Também é a única maneira de compartilhar memória em um aplicativo baseado em COM, uma vez que MIDL usa **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para marshal de memória.


## <a name="examples"></a>Exemplos

* [Reservando e comando memória](./reserving-and-committing-memory.md)

* [Exemplo do AWE](./awe-example.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções globais e locais](global-and-local-functions.md)
</dt> <dt>

[Funções de heap](heap-functions.md)
</dt> <dt>

[Funções de memória virtual](virtual-memory-functions.md)
</dt> </dl>

 

 