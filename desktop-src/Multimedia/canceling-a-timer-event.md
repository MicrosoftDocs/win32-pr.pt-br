---
title: Cancelando um evento de temporizador
description: Cancelando um evento de temporizador
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- Função timeKillEvent
- cancelando eventos de temporizador
- temporizadores de multimídia, eventos de cancelamento
- temporizadores, eventos de cancelamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4e9a92a02dca8ffd4723685fc96cdb0f82fc34a0fa2e3481a71a51997c316
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691786"
---
# <a name="canceling-a-timer-event"></a>Cancelando um evento de temporizador

> [!Note]  
> Este tópico descreve uma função obsoleta. Novos aplicativos devem usar a [**função CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.

 

Para cada temporizador periódico que cria chamando [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), o aplicativo deve cancelar o temporizador chamando a função [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar a memória que contém a função de retorno de chamada. Para cancelar um evento de temporizador, ele pode chamar a função a seguir.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando temporizadores multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 