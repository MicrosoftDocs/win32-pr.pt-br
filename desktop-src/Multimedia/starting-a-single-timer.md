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
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="6ac50-110">Iniciando um único evento de temporizador</span><span class="sxs-lookup"><span data-stu-id="6ac50-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="6ac50-111">Este tópico descreve uma função obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6ac50-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="6ac50-112">Os novos aplicativos devem usar a função [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) para criar temporizadores.</span><span class="sxs-lookup"><span data-stu-id="6ac50-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="6ac50-113">Para iniciar um único evento de temporizador, chame a função [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) , especificando a quantidade de tempo antes que o retorno de chamada ocorra, a resolução, o endereço da função de retorno de chamada (consulte [**timeproc**](/previous-versions//dd757631(v=vs.85))) e os dados do usuário para fornecer com a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6ac50-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="6ac50-114">Um aplicativo pode usar uma função como a seguinte para iniciar um único evento de temporizador.</span><span class="sxs-lookup"><span data-stu-id="6ac50-114">An application can use a function like the following to start a single timer event.</span></span>


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



<span data-ttu-id="6ac50-115">Para obter um exemplo da função de retorno de chamada OneShotCallback, consulte [escrevendo uma função de retorno de chamada do temporizador](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="6ac50-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ac50-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ac50-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ac50-117">Usando temporizadores de multimídia</span><span class="sxs-lookup"><span data-stu-id="6ac50-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 