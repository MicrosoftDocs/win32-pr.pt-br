---
description: Recebendo e entregando exemplos
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Recebendo e entregando exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825699"
---
# <a name="receiving-and-delivering-samples"></a>Recebendo e entregando exemplos

O pseudocódigo a seguir mostra como implementar o método **IMemInput:: Receive** :


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



O método **Receive** mantém o bloqueio de streaming, não o bloqueio de filtro. O filtro pode precisar aguardar algum evento antes de poder processar os dados, mostrados aqui pela chamada para **WaitForSingleObject**. Nem todo filtro precisará fazer isso. O método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica algumas condições gerais de streaming. Ele retornará o \_ estado VFW E \_ incorreto \_ se o filtro for interrompido, S \_ false se o filtro estiver sendo liberado e assim por diante. Qualquer código de retorno diferente de S \_ OK indica que o método **Receive** deve retornar imediatamente e não processar o exemplo.

Depois que o exemplo for processado, entregue-o ao filtro downstream chamando [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md). Esse método auxiliar chama **IMemInputPin:: Receive** no pino de entrada downstream. Um filtro pode fornecer amostras para vários Pins.

 

 



