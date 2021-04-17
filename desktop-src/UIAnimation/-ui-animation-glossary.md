---
title: Glossário de animação do Windows
description: Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Animação das janelas de animação do Windows, Glossário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b7f276b0f20efc35057a9ee7c006c3cf170ac3
ms.sourcegitcommit: fdd00b445ee88366e9cdd1eed0cb3e42e2a73eca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104498967"
---
# <a name="windows-animation-glossary"></a><span data-ttu-id="a45f0-104">Glossário de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="a45f0-104">Windows Animation Glossary</span></span>

<span data-ttu-id="a45f0-105">Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="a45f0-105">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span>

<dl> <dt>

<span data-ttu-id="a45f0-106"><span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**animação**</span><span class="sxs-lookup"><span data-stu-id="a45f0-106"><span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span> **animation**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-107">Uma sequência de imagens sintéticas e sucessivas que produz uma ilusão de movimento quando reproduzidas.</span><span class="sxs-lookup"><span data-stu-id="a45f0-107">A sequence of synthetic, successive still images that produces an illusion of movement when played back.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-108"><span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**Gerenciador de animação**</span><span class="sxs-lookup"><span data-stu-id="a45f0-108"><span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span> **animation manager**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-109">Um componente principal da animação do Windows e a interface de programação central para gerenciar (criar, agendar e controlar) animações.</span><span class="sxs-lookup"><span data-stu-id="a45f0-109">A core component of Windows Animation and the central programmatic interface for managing (creating, scheduling, and controlling) animations.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-110"><span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**temporizador de animação**</span><span class="sxs-lookup"><span data-stu-id="a45f0-110"><span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**animation timer**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-111">Um componente para fornecer serviços de tempo que podem ser usados em conjunto com o Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="a45f0-111">A component to provide timing services that can be used in conjunction with the animation manager.</span></span> <span data-ttu-id="a45f0-112">Ele acelera dinamicamente a taxa de quadros com base no aplicativo e na carga do sistema ou no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="a45f0-112">It dynamically throttles the frame rate based on application and system load or in low-power mode.</span></span> <span data-ttu-id="a45f0-113">Consulte também: limitação.</span><span class="sxs-lookup"><span data-stu-id="a45f0-113">See also: throttling.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-114"><span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**variável de animação**</span><span class="sxs-lookup"><span data-stu-id="a45f0-114"><span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span> **animation variable**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-115">Um valor que pode ser animado.</span><span class="sxs-lookup"><span data-stu-id="a45f0-115">A value that can be animated.</span></span> <span data-ttu-id="a45f0-116">As variáveis de animação podem ser usadas para representar a posição, o tamanho, a rotação, a transparência e outras qualidades dos objetos visíveis.</span><span class="sxs-lookup"><span data-stu-id="a45f0-116">Animation variables may be used to represent the position, size, rotation, transparency and other qualities of visible objects.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-117"><span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**cancelamento**</span><span class="sxs-lookup"><span data-stu-id="a45f0-117"><span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**cancellation**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-118">O processo de remover um storyboard do agendamento antes que ele comece a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="a45f0-118">The process of removing a storyboard from the schedule before it has started playing.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-119"><span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**çã**</span><span class="sxs-lookup"><span data-stu-id="a45f0-119"><span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**compression**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-120">Uma distorção da percepção de tempo de um Storyboard.</span><span class="sxs-lookup"><span data-stu-id="a45f0-120">A warping of a storyboard's perception of time.</span></span> <span data-ttu-id="a45f0-121">O sistema aumenta a taxa em que o storyboard progride passando valores de tempo de entrada que aumentam mais rápido do que o relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="a45f0-121">The system increases the rate at which the storyboard progresses by passing input time values that increase faster than the system clock.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-122"><span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**final**</span><span class="sxs-lookup"><span data-stu-id="a45f0-122"><span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**conclusion**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-123">O processo de direcionar um Storyboard para sair de qualquer loop indefinido.</span><span class="sxs-lookup"><span data-stu-id="a45f0-123">The process of directing a storyboard to exit any indefinite loops.</span></span> <span data-ttu-id="a45f0-124">Se o loop tiver começado, a iteração atual será concluída e o restante do storyboard será tocado.</span><span class="sxs-lookup"><span data-stu-id="a45f0-124">If the loop has begun, the current iteration will complete and the remainder of the storyboard will then play.</span></span> <span data-ttu-id="a45f0-125">Caso contrário, a parte em loop do storyboard será ignorada inteiramente.</span><span class="sxs-lookup"><span data-stu-id="a45f0-125">Otherwise, the looped portion of the storyboard will be skipped entirely.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-126"><span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**quadro**</span><span class="sxs-lookup"><span data-stu-id="a45f0-126"><span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span> **frame**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-127">Uma única imagem em um filme ou em uma animação.</span><span class="sxs-lookup"><span data-stu-id="a45f0-127">A single image in a movie or an animation.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-128"><span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**taxa de quadros**</span><span class="sxs-lookup"><span data-stu-id="a45f0-128"><span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span> **frame rate**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-129">O número de quadros exibidos por segundo.</span><span class="sxs-lookup"><span data-stu-id="a45f0-129">The number of frames displayed per second.</span></span> <span data-ttu-id="a45f0-130">Taxas de quadros mais altas geralmente produzem movimento mais suave na imagem.</span><span class="sxs-lookup"><span data-stu-id="a45f0-130">Higher frame rates generally produce smoother movement in the picture.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-131"><span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolador**</span><span class="sxs-lookup"><span data-stu-id="a45f0-131"><span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**interpolator**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-132">O objeto de programação que faz a interpolação matemática do valor e a velocidade de uma variável para uma transição.</span><span class="sxs-lookup"><span data-stu-id="a45f0-132">The programming object that does the mathematical interpolation of the value and velocity of a variable for a transition.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-133"><span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**Keyframe**</span><span class="sxs-lookup"><span data-stu-id="a45f0-133"><span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**keyframe**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-134">Um momento no tempo dentro de um storyboard, que pode ser especificado em relação ao início do storyboard, em relação a outro quadro-chave, ou na hora de término de uma transição e usado para especificar a hora de início e de término de outras transições ou um ciclo dentro do storyboard.</span><span class="sxs-lookup"><span data-stu-id="a45f0-134">A moment in time within a storyboard, which can be specified relative to the start of the storyboard, relative to another keyframe, or at the end time of a transition, and used to specify the start and end time of other transitions or a cycle within the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-135"><span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**While**</span><span class="sxs-lookup"><span data-stu-id="a45f0-135"><span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**loop**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-136">Uma seção de um storyboard entre dois quadros-chave que é reproduzido repetidamente.</span><span class="sxs-lookup"><span data-stu-id="a45f0-136">A section of a storyboard between two keyframes that is played repeatedly.</span></span> <span data-ttu-id="a45f0-137">Um loop pode reproduzir um número finito de vezes ou indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="a45f0-137">A loop may play a finite number of times or indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-138"><span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**comparação de prioridade**</span><span class="sxs-lookup"><span data-stu-id="a45f0-138"><span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span> **priority comparison**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-139">Código definido pelo cliente que compara dois storyboards, um já agendado e o outro a ser agendado, para determinar sua prioridade relativa.</span><span class="sxs-lookup"><span data-stu-id="a45f0-139">Client-defined code that compares two storyboards, one already scheduled and the other about to be scheduled, to determine their relative priority.</span></span> <span data-ttu-id="a45f0-140">Um storyboard agendado pode ser cortado, compactado, cancelado ou concluído para habilitar o agendamento do storyboard com prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="a45f0-140">A scheduled storyboard may be trimmed, compressed, canceled, or concluded to enable scheduling of the storyboard with higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-141"><span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**storyboard**</span><span class="sxs-lookup"><span data-stu-id="a45f0-141"><span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span> **storyboard**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-142">Um grupo de transições de animação sincronizadas em relação umas às outras.</span><span class="sxs-lookup"><span data-stu-id="a45f0-142">A group of animation transitions synchronized relative to one another.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-143"><span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**marca** de</span><span class="sxs-lookup"><span data-stu-id="a45f0-143"><span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span> **tag**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-144">Um par que consiste em uma ID de inteiro e um objeto COM usado por um aplicativo para identificar as variáveis de animação e os storyboards dentro do escopo de um Gerenciador de animação específico.</span><span class="sxs-lookup"><span data-stu-id="a45f0-144">A pair consisting of an integer ID and a COM object used by an application to identify animation variables and storyboards within the scope of a specific animation manager.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-145"><span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**limitação**</span><span class="sxs-lookup"><span data-stu-id="a45f0-145"><span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span> **throttling**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-146">Ajuste dinâmico da taxa de quadros de uma animação para atender a determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="a45f0-146">Dynamically adjusting the frame rate of an animation to meet certain requirements.</span></span> <span data-ttu-id="a45f0-147">A limitação ajuda a garantir que as animações sejam renderizadas em uma taxa de quadros consistente, minimizando o uso de recursos do sistema para renderização a uma taxa que está além do que é necessário ou útil.</span><span class="sxs-lookup"><span data-stu-id="a45f0-147">Throttling helps to ensure that animations are rendered at a consistent frame rate while minimizing the use of system resources for rendering at a rate that is beyond what is needed or useful.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-148"><span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**escala**</span><span class="sxs-lookup"><span data-stu-id="a45f0-148"><span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span> **tick**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-149">Um evento de temporizador que normalmente dispara a renderização de um único quadro.</span><span class="sxs-lookup"><span data-stu-id="a45f0-149">A timer event that typically triggers the rendering of a single frame.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-150"><span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**transição**</span><span class="sxs-lookup"><span data-stu-id="a45f0-150"><span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span> **transition**</span></span> 
</dt> <dd>

<span data-ttu-id="a45f0-151">Um constructo que define atualizações progressivas para uma variável de animação em um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="a45f0-151">A construct that defines progressive updates for an animation variable over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-152"><span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**restrições**</span><span class="sxs-lookup"><span data-stu-id="a45f0-152"><span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**trimming**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-153">Preempção do controle de um storyboard de uma variável de animação com um storyboard de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="a45f0-153">Preempting a storyboard's control of an animation variable with a higher-priority storyboard.</span></span> <span data-ttu-id="a45f0-154">Se o corte de um storyboard em uma ou mais variáveis fizer com que o storyboard termine prematuramente, ele será considerado truncado.</span><span class="sxs-lookup"><span data-stu-id="a45f0-154">If trimming a storyboard on one or more variables causes the storyboard to end prematurely, it is considered truncated.</span></span> <span data-ttu-id="a45f0-155">Consulte também: truncamento.</span><span class="sxs-lookup"><span data-stu-id="a45f0-155">See also: truncation.</span></span>

</dd> <dt>

<span data-ttu-id="a45f0-156"><span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**truncamento**</span><span class="sxs-lookup"><span data-stu-id="a45f0-156"><span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**truncation**</span></span>
</dt> <dd>

<span data-ttu-id="a45f0-157">Terminar um storyboard prematuramente ao apropriar o controle de uma ou mais das variáveis que ele anima com um ou mais storyboards de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="a45f0-157">Ending a storyboard prematurely by preempting control of one or more of the variables that it animates with one or more higher-priority storyboards.</span></span> <span data-ttu-id="a45f0-158">Consulte também: corte.</span><span class="sxs-lookup"><span data-stu-id="a45f0-158">See also: trimming.</span></span>

</dd> </dl>

 

 




