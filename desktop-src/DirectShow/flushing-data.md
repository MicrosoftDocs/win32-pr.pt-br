---
description: Liberando dados
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Liberando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645683"
---
# <a name="flushing-data"></a>Liberando dados

O pseudocódigo a seguir mostra como implementar o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



Quando a liberação é iniciada, o método **BeginFlush** pega o bloqueio de filtro, que serializa a alteração de estado. Ainda não é seguro pegar o bloqueio de streaming, porque a liberação ocorre no thread do aplicativo, e o thread de streaming pode estar no meio de uma chamada de **recebimento** . O PIN precisa garantir que **Receive** não seja bloqueado e que todas as chamadas subseqüentes a serem **recebidas** falharão. O método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) define um sinalizador interno, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Quando o sinalizador for **true**, o método **Receive** falhará.

Ao entregar o downstream de chamada **BeginFlush** , o PIN garante que todos os filtros downstream liberem suas amostras e retornem de chamadas **Receive** . Isso, por sua vez, garante que o PIN de entrada não seja bloqueado aguardando **GetBuffer** ou **Receive**. Se o método **Receive** de seu PIN nunca aguardar um evento (por exemplo, para obter recursos), o método **BeginFlush** deverá forçar a espera para terminar definindo o evento. Neste ponto, o método **Receive** é garantido para retornar e o sinalizador **m \_ bFlushing** impede que novas chamadas **Receive** façam qualquer trabalho.

Para alguns filtros, isso é tudo o que o **BeginFlush** precisa fazer. O método **EndFlush** sinalizará ao filtro que ele pode começar a receber amostras novamente. Outros filtros podem precisar usar variáveis ou recursos em **BeginFlush** que também são usados em **Receive**. Nesse caso, o filtro deve manter o bloqueio de streaming primeiro. Certifique-se de não fazer isso antes de qualquer uma das etapas anteriores, porque você pode causar um deadlock.

O método **EndFlush** mantém o bloqueio de filtro e propaga o downstream de chamada:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



O método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) redefine o sinalizador **m \_ bFlushing** como **false**, o que permite que o método **Receive** comece a receber amostras novamente. Essa deve ser a última etapa em **EndFlush**, porque o PIN não deve receber amostras até que a liberação esteja concluída e todos os filtros de downstream sejam notificados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



