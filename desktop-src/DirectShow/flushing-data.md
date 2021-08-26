---
description: Liberando dados
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Liberando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a435bf40ae9f71b35707935812c3a935a95df1904db00a652634b171f20a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965456"
---
# <a name="flushing-data"></a>Liberando dados

O pseudocódigo a seguir mostra como implementar o [**método IPin::BeginFlush:**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)


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



Quando a liberação é iniciada, **o método BeginFlush** recebe o bloqueio de filtro, que serializa a alteração de estado. Ainda não é seguro pegar o bloqueio de streaming, pois a liberação acontece no thread do aplicativo e o thread de streaming pode estar no meio de uma **chamada de** recebimento. O pin precisa garantir que **o Recebimento** não seja bloqueado e que as chamadas subsequentes para **Receber** falharão. O [**método CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) define um sinalizador interno, [**CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Quando o sinalizador é **TRUE,** o **método Receive** falha.

Ao entregar a **chamada BeginFlush** downstream, o pin garante que todos os filtros downstream liberem seus exemplos e retornem de **Receber** chamadas. Isso, por sua vez, garante que o pino de entrada não seja bloqueado aguardando **GetBuffer** ou **Receive**. Se o método **Receive** do pino aguardar um evento (por exemplo, para obter recursos), o **método BeginFlush** deverá forçar a espera para terminar definindo o evento. Neste ponto, o **método Receive** tem a garantia de retornar e  o sinalizador **m \_ bFlushing** impede que novas chamadas de recebimento funcionem.

Para alguns filtros, isso é tudo **o que BeginFlush** precisa fazer. O **método EndFlush** sinalizará ao filtro que ele pode começar a receber amostras novamente. Outros filtros podem precisar usar variáveis ou recursos **em BeginFlush** que também são usados em **Receber**. Nesse caso, o filtro deve manter o bloqueio de streaming primeiro. Não faça isso antes de qualquer uma das etapas anteriores, pois você pode causar um deadlock.

O **método EndFlush** mantém o bloqueio de filtro e propaga a chamada downstream:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



O [**método CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) redefine o **sinalizador m \_ bFlushing** como **FALSE,** que permite que o método **Receive** comece a receber amostras novamente. Essa deve ser a última etapa em **EndFlush,** porque o pino não deve receber amostras até que a liberação seja concluída e todos os filtros downstream sejam notificados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



