---
description: Entregando o fim do fluxo
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entregando o fim do fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825551"
---
# <a name="delivering-the-end-of-stream"></a>Entregando o fim do fluxo

Quando o PIN de entrada recebe uma notificação de fim de fluxo, ele propaga a chamada downstream. Todos os filtros downstream que recebem dados desse PIN de entrada também devem obter a notificação de fim de fluxo. Novamente, faça o bloqueio de streaming e não o bloqueio de filtro. Se o filtro tiver dados pendentes que ainda não foram entregues, o filtro deverá entregá-lo agora, antes de enviar a notificação de fim de fluxo. Ele não deve enviar dados após o final do fluxo.


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



O método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) chama [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada downstream.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



