---
title: Obtendo e definindo a resolução do temporizador
description: Obtendo e definindo a resolução do temporizador
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- temporizadores de multimídia, resolução
- temporizadores, resolução
- resolução mínima do timer
- resolução máxima do timer
- temporizadores de multimídia, resolução máxima
- temporizadores, resolução máxima
- temporizadores de multimídia, resolução mínima
- temporizadores, resolução mínima
- função timeGetDevCaps
- função timeBeginPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761890"
---
# <a name="obtaining-and-setting-timer-resolution"></a>Obtendo e definindo a resolução do temporizador

O exemplo a seguir chama a função [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) para determinar as resoluções de temporizador mínimo e máximo com suporte nos serviços de timer. Antes de configurar qualquer evento de temporizador, o exemplo estabelece a resolução mínima do timer usando a função [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) .


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando temporizadores de multimídia](using-multimedia-timers.md)
</dt> </dl>

 

 




