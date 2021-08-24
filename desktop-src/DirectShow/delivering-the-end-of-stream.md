---
description: Entregando o fim do fluxo
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entregando o fim do fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebae0fe3238f32f630c0a2ecd0787f6bd9b75a9aed6342e202f187d3fe8dac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831346"
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

 

 



