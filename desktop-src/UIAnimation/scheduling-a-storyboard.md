---
title: Agendar um storyboard
description: Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Animação de storyboards do Windows, agendamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004959"
---
# <a name="schedule-a-storyboard"></a><span data-ttu-id="09acc-104">Agendar um storyboard</span><span class="sxs-lookup"><span data-stu-id="09acc-104">Schedule a Storyboard</span></span>

<span data-ttu-id="09acc-105">Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="09acc-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="09acc-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="09acc-106">Overview</span></span>

<span data-ttu-id="09acc-107">Por padrão, cada Storyboard começa imediatamente quando está agendado.</span><span class="sxs-lookup"><span data-stu-id="09acc-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="09acc-108">Isso significa que, quando um storyboard começa a animar uma ou mais variáveis, ele pode interromper qualquer outro storyboard animando as mesmas variáveis.</span><span class="sxs-lookup"><span data-stu-id="09acc-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="09acc-109">No entanto, um aplicativo pode especificar outros comportamentos determinando a prioridade relativa entre storyboards.</span><span class="sxs-lookup"><span data-stu-id="09acc-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="09acc-110">Depois que um storyboard tiver sido agendado, ele não poderá mais ser alterado.</span><span class="sxs-lookup"><span data-stu-id="09acc-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="09acc-111">No entanto, depois que um storyboard tiver sido removido da agenda, ele poderá ser agendado para reprodução novamente.</span><span class="sxs-lookup"><span data-stu-id="09acc-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="09acc-112">Os desenvolvedores devem ter cuidado ao reutilizar storyboards, pois isso só deve ser feito quando não há nenhuma chance de que o mesmo storyboard precise ser colocado na fila devido a uma ação do usuário quando ele já está em execução ou na fila na agenda.</span><span class="sxs-lookup"><span data-stu-id="09acc-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="09acc-113">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="09acc-113">Example Code</span></span>

<span data-ttu-id="09acc-114">O código de exemplo a seguir é extraído de MainWindow. cpp [na animação de](application-driven-animation-sample.md) exemplos de animação do Windows e [animação orientada por temporizador](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="09acc-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="09acc-115">Ele usa o método [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para agendar o storyboard.</span><span class="sxs-lookup"><span data-stu-id="09acc-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="09acc-116">Esse método requer a hora atual como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="09acc-116">This method requires the current time as a parameter.</span></span>


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a><span data-ttu-id="09acc-117">Etapa anterior</span><span class="sxs-lookup"><span data-stu-id="09acc-117">Previous Step</span></span>

<span data-ttu-id="09acc-118">Antes de iniciar esta etapa, você deve ter concluído esta etapa: [criar um storyboard e adicionar transições](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="09acc-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09acc-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09acc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09acc-120">**IUIAnimationStoryboard:: Schedule**</span><span class="sxs-lookup"><span data-stu-id="09acc-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="09acc-121">**IUIAnimationTimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="09acc-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="09acc-122">Visão geral do storyboard</span><span class="sxs-lookup"><span data-stu-id="09acc-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




