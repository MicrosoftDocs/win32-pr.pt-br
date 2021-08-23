---
description: A função SELECT é usada para determinar o status de um ou mais soquetes em um conjunto. Para cada soquete, o chamador pode solicitar informações sobre o status de leitura, gravação ou erro. Um conjunto de soquetes é indicado por uma \_ estrutura de conjunto FD.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Restrições de vários provedores em Select
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec5c89c6dd2db809a356f5b53212fd019e32fd9e348c298bcab7f567ee2d0fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569626"
---
# <a name="multiple-provider-restrictions-on-select"></a>Restrições de vários provedores em Select

A função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) é usada para determinar o status de um ou mais soquetes em um conjunto. Para cada soquete, o chamador pode solicitar informações sobre o status de leitura, gravação ou erro. Um conjunto de soquetes é indicado por uma estrutura de [**\_ conjunto FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

Windows Os soquetes 2 permitem que um aplicativo use mais de um provedor de serviços, mas a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) é limitada a um conjunto de soquetes associados a um único provedor de serviços. Isso não, de forma alguma, impedir que um aplicativo tenha vários soquetes abertos por meio de vários provedores.

Há duas maneiras de determinar o status de um conjunto de soquetes que abrange mais de um provedor de serviços:

-   Usar as funções [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ao bloquear a semântica de bloqueio é empregado.
-   usar a função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) quando operações de não bloqueio são empregadas e o aplicativo já está usando um Windows bomba de mensagem.

Quando um aplicativo precisa usar a semântica de bloqueio em um conjunto de soquetes que abrange vários provedores, o [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) é recomendado. O aplicativo também pode usar a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , que permite que os \_ eventos de rede do FD xxx (consulte [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) sejam associados a um objeto de evento e sejam tratados de dentro do paradigma do objeto de evento (descrito em [objetos de evento e e/s sobrepostos](overlapped-i-o-and-event-objects-2.md)).

A função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) não está restrita a um único provedor porque usa um único descritor de soquete como um parâmetro de entrada. No entanto, observe que a função [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) oferece melhor desempenho e escalabilidade em relação a **WSAAsyncSelect** , uma vez que a sobrecarga de manter a bomba de mensagens com mensagens de evento do Winsock aumenta conforme o número total de soquetes usados aumenta.

 

 



