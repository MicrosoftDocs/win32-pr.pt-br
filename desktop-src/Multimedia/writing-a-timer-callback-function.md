---
title: Escrevendo uma função de retorno de chamada do temporizador
description: Escrevendo uma função de retorno de chamada do temporizador
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- temporizadores de multimídia, funções de retorno de chamada
- temporizadores, funções de retorno de chamada
- gravando funções de retorno de chamada do timer
- temporizadores de multimídia, gravando funções de retorno de chamada
- temporizadores, gravando funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917212"
---
# <a name="writing-a-timer-callback-function"></a>Escrevendo uma função de retorno de chamada do temporizador

> [!Note]  
> Este tópico descreve uma função obsoleta. Os novos aplicativos devem usar a função [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.

 

A seguinte função de retorno de chamada, OneShotTimer, invalida o identificador para o evento de temporizador único e chama uma rotina de temporizador para manipular as tarefas específicas do aplicativo. Para obter mais informações, consulte [**timeproc**](/previous-versions//dd757631(v=vs.85)).


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

[Usando temporizadores de multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 