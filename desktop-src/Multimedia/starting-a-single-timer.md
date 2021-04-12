---
title: Iniciando um único evento de temporizador
description: Iniciando um único evento de temporizador
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- temporizadores de multimídia, iniciando eventos
- temporizadores, iniciando eventos
- função timeSetEvent
- Iniciando eventos de timer
- eventos de temporizador único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365892"
---
# <a name="starting-a-single-timer-event"></a>Iniciando um único evento de temporizador

> [!Note]  
> Este tópico descreve uma função obsoleta. Os novos aplicativos devem usar a função [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.

 

Para iniciar um único evento de temporizador, chame a função [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , especificando a quantidade de tempo antes que o retorno de chamada ocorra, a resolução, o endereço da função de retorno de chamada (consulte [**timeproc**](/previous-versions//dd757631(v=vs.85))) e os dados do usuário para fornecer com a função de retorno de chamada. Um aplicativo pode usar uma função como a seguinte para iniciar um único evento de temporizador.


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



Para obter um exemplo da função de retorno de chamada OneShotCallback, consulte [escrevendo uma função de retorno de chamada do temporizador](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando temporizadores de multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 