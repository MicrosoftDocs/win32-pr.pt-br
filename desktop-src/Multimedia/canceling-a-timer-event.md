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
# <a name="canceling-a-timer-event"></a><span data-ttu-id="edf7b-109">Cancelando um evento de timer</span><span class="sxs-lookup"><span data-stu-id="edf7b-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="edf7b-110">Este tópico descreve uma função obsoleta.</span><span class="sxs-lookup"><span data-stu-id="edf7b-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="edf7b-111">Os novos aplicativos devem usar a função [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.</span><span class="sxs-lookup"><span data-stu-id="edf7b-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="edf7b-112">Para cada temporizador periódico criando chamando [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), o aplicativo deve cancelar o temporizador chamando a função [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) antes de liberar a memória que contém a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="edf7b-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="edf7b-113">Para cancelar um evento de timer, ele pode chamar a função a seguir.</span><span class="sxs-lookup"><span data-stu-id="edf7b-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="edf7b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edf7b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf7b-115">Usando temporizadores de multimídia</span><span class="sxs-lookup"><span data-stu-id="edf7b-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 