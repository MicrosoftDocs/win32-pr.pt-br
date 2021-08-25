---
title: Escrevendo uma função de retorno de chamada de temporizador
description: Escrevendo uma função de retorno de chamada de temporizador
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- temporizadores de multimídia, funções de retorno de chamada
- temporizadores, funções de retorno de chamada
- escrevendo funções de retorno de chamada de temporizador
- temporizadores multimídia, escrevendo funções de retorno de chamada
- temporizadores, escrevendo funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b8680fc4d697c33514276276daaa2a4d75577bfbd78fa3caffc7f426ca9d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891776"
---
# <a name="writing-a-timer-callback-function"></a>Escrevendo uma função de retorno de chamada de temporizador

> [!Note]  
> Este tópico descreve uma função obsoleta. Novos aplicativos devem usar a [**função CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.

 

A função de retorno de chamada a seguir, OneShotTimer, invalida o identificador do evento de temporizador único e chama uma rotina de temporizador para lidar com as tarefas específicas do aplicativo. Para obter mais informações, consulte [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando temporizadores multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 