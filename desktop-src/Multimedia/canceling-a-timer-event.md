---
title: Cancelando um evento de timer
description: Cancelando um evento de timer
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- função timeKillEvent
- Cancelando eventos de timer
- temporizadores de multimídia, cancelando eventos
- temporizadores, cancelando eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007511"
---
# <a name="canceling-a-timer-event"></a>Cancelando um evento de timer

> [!Note]  
> Este tópico descreve uma função obsoleta. Os novos aplicativos devem usar a função [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.

 

Para cada temporizador periódico criando chamando [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), o aplicativo deve cancelar o temporizador chamando a função [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar a memória que contém a função de retorno de chamada. Para cancelar um evento de timer, ele pode chamar a função a seguir.


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

[Usando temporizadores de multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 