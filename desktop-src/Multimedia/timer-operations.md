---
title: Operações de evento de timer
description: Operações de evento de timer
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- função timeSetEvent
- função timeKillEvent
- Iniciando eventos de timer
- eventos de temporizador único
- eventos de timer periódicos
- Cancelando eventos de timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640474"
---
# <a name="timer-event-operations"></a><span data-ttu-id="a57bd-111">Operações de evento de timer</span><span class="sxs-lookup"><span data-stu-id="a57bd-111">Timer Event Operations</span></span>

<span data-ttu-id="a57bd-112">Depois de estabelecer a resolução do timer do aplicativo, você pode iniciar eventos de timer usando a função [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a57bd-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="a57bd-113">Essa função retorna um identificador de temporizador que pode ser usado para parar ou identificar eventos de timer.</span><span class="sxs-lookup"><span data-stu-id="a57bd-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="a57bd-114">Um dos parâmetros da função é o endereço de uma função de retorno de chamada [**timeproc**](/previous-versions//dd757631(v=vs.85)) que é chamada quando o evento do temporizador ocorre.</span><span class="sxs-lookup"><span data-stu-id="a57bd-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="a57bd-115">Há dois tipos de eventos de temporizador: *único* e *periódico*.</span><span class="sxs-lookup"><span data-stu-id="a57bd-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="a57bd-116">Um único evento de temporizador ocorre uma vez, após um número especificado de milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a57bd-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="a57bd-117">Um evento de timer periódico ocorre sempre que um número especificado de milissegundos é decorrido.</span><span class="sxs-lookup"><span data-stu-id="a57bd-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="a57bd-118">O intervalo entre os eventos periódicos é chamado de *atraso de evento*.</span><span class="sxs-lookup"><span data-stu-id="a57bd-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="a57bd-119">Eventos de timer periódicos com atraso de evento de 10 milissegundos ou menos consomem uma parte significativa dos recursos da CPU.</span><span class="sxs-lookup"><span data-stu-id="a57bd-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="a57bd-120">A relação entre a resolução de um evento de temporizador e o comprimento do atraso do evento é importante em eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="a57bd-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="a57bd-121">Por exemplo, se você especificar uma resolução de 5 e um atraso de evento de 100, os serviços de timer notificarão a função de retorno de chamada após um intervalo que varia de 95 a 105 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="a57bd-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="a57bd-122">Você pode cancelar um evento de temporizador ativo a qualquer momento usando a função [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a57bd-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="a57bd-123">Lembre-se de cancelar todos os timers pendentes antes de liberar a memória que contém a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a57bd-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="a57bd-124">O temporizador multimídia é executado em seu próprio thread.</span><span class="sxs-lookup"><span data-stu-id="a57bd-124">The multimedia timer runs in its own thread.</span></span>

 

 

 