---
title: Sobre timers de multimídia
description: Sobre timers de multimídia
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Multimídia do Windows, temporizadores
- multimídia, Timers
- entrada de multimídia, temporizadores
- Timers de multimídia, sobre
- Timers, About
- temporizadores de multimídia, eventos de agendamento
- temporizadores, eventos de agendamento
- agendando eventos de timer
- tempo de alta resolução
- Função SetTimer
- Função CreateWaitableTimer
- WM_TIMER mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007485"
---
# <a name="about-multimedia-timers"></a><span data-ttu-id="b37d9-115">Sobre timers de multimídia</span><span class="sxs-lookup"><span data-stu-id="b37d9-115">About Multimedia Timers</span></span>

<span data-ttu-id="b37d9-116">Os serviços de timer de multimídia permitem que os aplicativos agendem eventos de timer com a maior resolução (ou precisão) possível para a plataforma de hardware.</span><span class="sxs-lookup"><span data-stu-id="b37d9-116">Multimedia timer services allow applications to schedule timer events with the greatest resolution (or accuracy) possible for the hardware platform.</span></span> <span data-ttu-id="b37d9-117">Esses serviços de timer de multimídia permitem que você agende eventos de timer em uma resolução mais alta do que outros serviços de timer.</span><span class="sxs-lookup"><span data-stu-id="b37d9-117">These multimedia timer services allow you to schedule timer events at a higher resolution than other timer services.</span></span>

<span data-ttu-id="b37d9-118">Esses serviços de timer são úteis para aplicativos que exigem tempo de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="b37d9-118">These timer services are useful for applications that demand high-resolution timing.</span></span> <span data-ttu-id="b37d9-119">Por exemplo, um sequenciador MIDI requer um temporizador de alta resolução porque ele deve manter o ritmo dos eventos MIDI dentro de uma resolução de 1 milissegundo.</span><span class="sxs-lookup"><span data-stu-id="b37d9-119">For example, a MIDI sequencer requires a high-resolution timer because it must maintain the pace of MIDI events within a resolution of 1 millisecond.</span></span>

<span data-ttu-id="b37d9-120">Os aplicativos que não usam o tempo de alta resolução devem usar a função [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) em vez de serviços de timer de multimídia.</span><span class="sxs-lookup"><span data-stu-id="b37d9-120">Applications that do not use high-resolution timing should use the [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) function instead of multimedia timer services.</span></span> <span data-ttu-id="b37d9-121">Os serviços de temporizador fornecidos por mensagens de [ \_ temporizador do WM](../winmsg/wm-timer.md) do **webtimer** post para uma fila de mensagens, enquanto os serviços de timer de multimídia chamam uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b37d9-121">The timer services provided by **SetTimer** post [WM\_TIMER](../winmsg/wm-timer.md) messages to a message queue, while the multimedia timer services call a callback function.</span></span> <span data-ttu-id="b37d9-122">Os aplicativos que desejam um temporizador que pode ser aguardado devem usar a função [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .</span><span class="sxs-lookup"><span data-stu-id="b37d9-122">Applications that want a waitable timer should use the [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function.</span></span>

 

 