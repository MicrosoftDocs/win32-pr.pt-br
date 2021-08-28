---
title: Pilha
description: Um heap rastreia um grupo de alocações que são liberadas como uma unidade.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Serviços Web de heap para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005926"
---
# <a name="heap"></a>Pilha

Um heap rastreia um grupo de alocações que são liberadas como uma unidade.

Isso permite evitar padrões complexos de alocação e desalocação de memória ao usar o WWSAPI.


Há um heap associado a cada mensagem. À medida que uma mensagem está sendo enviada ou quando uma mensagem está sendo recebida, o heap da mensagem é usado para todas as alocações relacionadas a essa mensagem específica. Depois que uma mensagem é enviada ou recebida, o heap é redefinido (o que limpa todas as alocações relacionadas à mensagem específica).

Heaps também podem ser usados para armazenar dados de mensagem separadamente do tempo de vida de uma mensagem. Muitas das especificações de autorização da API do heap a ser usada ao ler dados dão controle explícito sobre o tempo de vida de qualquer leitura de dados.

As alocações de um heap têm a garantia de serem alinhadas em pelo menos um limite de 8 byte.

As alocações de zero byte retornarão um ponteiro não NULL.

No Windows 7, se PageHeap estiver habilitado, um heap retornado de HeapCreate será usado para gerenciar a memória. Nesse caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) mapeia diretamente para HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) é mapeado para HeapDume.

A enumeração a seguir é usada com o heap:

-   [**ID DA \_ PROPRIEDADE HEAP \_ \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

As seguintes funções são usadas com o heap:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

O seguinte handle é usado com o heap:

-   [HEAP \_ do WS](ws-heap.md)

As seguintes estruturas são usadas com o heap:

-   [**PROPRIEDADES \_ DO HEAP \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**PROPRIEDADE \_ HEAP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




