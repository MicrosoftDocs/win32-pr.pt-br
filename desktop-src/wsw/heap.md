---
title: Pilha
description: Um heap rastreia um grupo de alocações que são liberadas como uma unidade.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Serviços Web de heap para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368959"
---
# <a name="heap"></a>Pilha

Um heap rastreia um grupo de alocações que são liberadas como uma unidade.

Isso permite que você evite padrões complexos de alocar e desalocar memória ao usar o WWSAPI.


Há um heap associado a cada mensagem. Como uma mensagem está sendo enviada, ou quando uma mensagem está sendo recebida, o heap da mensagem é usado para qualquer alocação relacionada a essa mensagem específica. Depois que uma mensagem é enviada ou recebida, o heap é redefinido (o que limpa todas as alocações relacionadas à mensagem específica).

Os heaps também podem ser usados para armazenar dados de mensagens separadamente do tempo de vida de uma mensagem. Muitas das especificações de permissão de API do heap a serem usadas na leitura de dados fornecem controle explícito durante o tempo de vida de qualquer leitura de dados.

As alocações de um heap têm a garantia de serem alinhadas em pelo menos um limite de 8 bytes.

As alocações de zero byte retornarão um ponteiro não nulo.

No Windows 7, se PageHeap estiver habilitado, um heap retornado de HeapCreate será usado para gerenciar a memória. Nesse caso, o [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) mapeia diretamente para HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) é mapeado para HeapDestroy.

A seguinte enumeração é usada com o heap:

-   [**\_ID da \_ propriedade da heap do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

As funções a seguir são usadas com o heap:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

O identificador a seguir é usado com o heap:

-   [HEAP do WS \_](ws-heap.md)

As seguintes estruturas são usadas com o heap:

-   [**\_Propriedades de heap do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_propriedade de heap WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




