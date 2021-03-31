---
title: Resolução do temporizador
description: Resolução do temporizador
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
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
- função timeEndPeriod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "103634732"
---
# <a name="timer-resolution"></a><span data-ttu-id="9b070-114">Resolução do temporizador</span><span class="sxs-lookup"><span data-stu-id="9b070-114">Timer Resolution</span></span>

<span data-ttu-id="9b070-115">Para determinar as resoluções de temporizador mínimo e máximo com suporte nos serviços de timer, use a função [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="9b070-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="9b070-116">Essa função preenche os membros **wPeriodMin** e **wPeriodMax** da estrutura [**timecaps**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) com as resoluções mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="9b070-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="9b070-117">Esse intervalo pode variar entre computadores e plataformas Windows.</span><span class="sxs-lookup"><span data-stu-id="9b070-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="9b070-118">Depois de determinar as resoluções de temporizador mínimo e máximo disponíveis, você deve estabelecer a resolução mínima que deseja que seu aplicativo use.</span><span class="sxs-lookup"><span data-stu-id="9b070-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="9b070-119">Use as funções [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) para definir e limpar essa resolução.</span><span class="sxs-lookup"><span data-stu-id="9b070-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="9b070-120">Você deve corresponder a cada chamada para **timeBeginPeriod** com uma chamada para **timeEndPeriod**, especificando a mesma resolução mínima em ambas as chamadas.</span><span class="sxs-lookup"><span data-stu-id="9b070-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="9b070-121">Um aplicativo pode fazer várias chamadas **timeBeginPeriod** , contanto que cada chamada seja correspondida com uma chamada para **timeEndPeriod**.</span><span class="sxs-lookup"><span data-stu-id="9b070-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="9b070-122">Em [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), o parâmetro *uPeriod* indica a resolução mínima do timer, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="9b070-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="9b070-123">Você pode especificar qualquer valor de resolução do temporizador dentro do intervalo com suporte pelo temporizador.</span><span class="sxs-lookup"><span data-stu-id="9b070-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b070-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b070-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b070-125">Sobre timers de multimídia</span><span class="sxs-lookup"><span data-stu-id="9b070-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




