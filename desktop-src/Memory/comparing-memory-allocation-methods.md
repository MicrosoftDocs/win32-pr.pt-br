---
Description: Veja a seguir uma breve comparação dos vários métodos de alocação de memória.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Comparando métodos de alocação de memória
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103930527"
---
# <a name="comparing-memory-allocation-methods"></a>Comparando métodos de alocação de memória

Veja a seguir uma breve comparação dos vários métodos de alocação de memória:

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **Novo**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Embora as funções [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) alocam, por fim, a memória do mesmo heap, cada uma delas fornece um conjunto de funcionalidades um pouco diferente. Por exemplo, **HeapAlloc** pode ser instruído a gerar uma exceção se a memória não puder ser alocada, um recurso não disponível com **LocalAlloc**. O **LocalAlloc** dá suporte à alocação de identificadores que permitem que a memória subjacente seja movida por uma realocação sem alterar o valor do identificador, um recurso não disponível com **HeapAlloc**.

Começando com o Windows de 32 bits, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) são implementados como funções de wrapper que chamam [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) usando um identificador para o heap padrão do processo. Portanto, **GlobalAlloc** e **LocalAlloc** têm maior sobrecarga do que o **HeapAlloc**.

Como os alocadores de heap diferentes fornecem funcionalidade distinta usando mecanismos diferentes, você deve liberar memória com a função correta. Por exemplo, a memória alocada com [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) deve ser liberada com [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) e não [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) ou [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). A memória alocada com [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) deve ser consultada, validada e liberada com a função global ou local correspondente.

A função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) permite que você especifique opções adicionais para a alocação de memória. No entanto, suas alocações usam uma granularidade de página, portanto, usar o **VirtualAlloc** pode resultar em maior uso de memória.

A função **malloc** tem a desvantagem de ser dependente do tempo de execução. O **novo** operador tem a desvantagem de ser dependente do compilador e dependente do idioma.

A função [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) tem a vantagem de funcionar bem em C, C++ ou Visual Basic. Também é a única maneira de compartilhar memória em um aplicativo baseado em COM, pois MIDL usa **CoTaskMemAlloc** e [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para empacotar a memória.


## <a name="examples"></a>Exemplos

* [Reservando e confirmando memória](./reserving-and-committing-memory.md)

* [Exemplo de AWE](./awe-example.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções globais e locais](global-and-local-functions.md)
</dt> <dt>

[Funções de heap](heap-functions.md)
</dt> <dt>

[Funções de memória virtual](virtual-memory-functions.md)
</dt> </dl>

 

 