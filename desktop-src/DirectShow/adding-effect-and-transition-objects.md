---
description: Adicionando objetos de efeito e transição
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Adicionando objetos de efeito e transição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009952"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="b759d-103">Adicionando objetos de efeito e transição</span><span class="sxs-lookup"><span data-stu-id="b759d-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="b759d-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="b759d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b759d-105">No DES, um efeito ou uma transição é representado por dois objetos:</span><span class="sxs-lookup"><span data-stu-id="b759d-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="b759d-106">Um *objeto de linha do tempo* representa o efeito ou a transição dentro da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="b759d-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="b759d-107">Para efeitos, o objeto Timeline dá suporte à interface [**IAMTimelineEffect**](iamtimelineeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="b759d-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="b759d-108">Para transições, ele dá suporte à interface [**IAMTimelineTrans**](iamtimelinetrans.md) .</span><span class="sxs-lookup"><span data-stu-id="b759d-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="b759d-109">Os dois tipos dão suporte à interface [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="b759d-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="b759d-110">O *subobjeto* é um objeto que implementa o processamento de dados para o efeito ou a transição.</span><span class="sxs-lookup"><span data-stu-id="b759d-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="b759d-111">O objeto Timeline contém um ponteiro para o subobjeto.</span><span class="sxs-lookup"><span data-stu-id="b759d-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="b759d-112">Para adicionar um efeito ou uma transição, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b759d-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="b759d-113">**1. criar o objeto de linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="b759d-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="b759d-114">Para criar o objeto Timeline, chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="b759d-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="b759d-115">Defina o tipo igual ao **\_ efeito de \_ tipo \_ principal da linha do tempo** para um efeito ou para a **\_ \_ \_ transição de tipo principal da linha do tempo** para uma transição.</span><span class="sxs-lookup"><span data-stu-id="b759d-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="b759d-116">O exemplo a seguir cria um objeto de transição:</span><span class="sxs-lookup"><span data-stu-id="b759d-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="b759d-117">**2. Especifique o subobjeto**</span><span class="sxs-lookup"><span data-stu-id="b759d-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="b759d-118">O objeto Timeline atua como um wrapper para outro objeto, chamado de *subobjeto*, que faz o trabalho real.</span><span class="sxs-lookup"><span data-stu-id="b759d-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="b759d-119">O subobjeto implementa uma transformação de dados que produz o efeito ou a transição desejada.</span><span class="sxs-lookup"><span data-stu-id="b759d-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="b759d-120">Para obter uma lista de transições e efeitos fornecidos com o DES, consulte [transições e efeitos](transitions-and-effects.md).</span><span class="sxs-lookup"><span data-stu-id="b759d-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="b759d-121">Para definir o subobjeto, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) no objeto Timeline, passando-o identificador de classe (CLSID) do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="b759d-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="b759d-122">O DirectShow fornece um enumerador para efeitos de vídeo e transições de vídeo, que você pode usar para obter o CLSID.</span><span class="sxs-lookup"><span data-stu-id="b759d-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="b759d-123">Para obter mais informações, consulte [enumerando efeitos e transições](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="b759d-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="b759d-124">O exemplo a seguir define a [transição de apagamento SMPTE](smpte-wipe-transition.md) como o subobjeto:</span><span class="sxs-lookup"><span data-stu-id="b759d-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="b759d-125">**3. definir os horários de início e de término**</span><span class="sxs-lookup"><span data-stu-id="b759d-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="b759d-126">Para definir os horários de início e de parada, chame o método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="b759d-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="b759d-127">Esses tempos são relativos à hora de início do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="b759d-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="b759d-128">Os efeitos podem se sobrepor dentro do mesmo objeto, mas as transições não podem.</span><span class="sxs-lookup"><span data-stu-id="b759d-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="b759d-129">O exemplo a seguir define a hora de início como 5 segundos e a hora de término como 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="b759d-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="b759d-130">Quando uma transição é renderizada, o progresso da transição em cada quadro é calculado com base em uma propriedade **Progress** , que é normalizada para um intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="b759d-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="b759d-131">O DES usa a hora de início de cada quadro para calcular o valor de progresso.</span><span class="sxs-lookup"><span data-stu-id="b759d-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="b759d-132">Isso significa que se a hora de parada da transição for igual à hora de parada da origem, o valor de **progresso** nunca alcançará exatamente 1,0, pois a hora de início do último quadro será um pouco diferente da hora de parada.</span><span class="sxs-lookup"><span data-stu-id="b759d-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="b759d-133">Para fazer com que a transição alcance 1,0, defina a hora de parada da transição como pelo menos um quadro anterior à hora de parada da origem.</span><span class="sxs-lookup"><span data-stu-id="b759d-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="b759d-134">**4. inserir o objeto na linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="b759d-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="b759d-135">Para inserir o objeto na linha do tempo, chame um dos seguintes métodos no pai, dependendo do tipo de objeto:</span><span class="sxs-lookup"><span data-stu-id="b759d-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="b759d-136">Efeitos: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="b759d-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="b759d-137">Transições: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="b759d-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="b759d-138">No método [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , você deve especificar a prioridade do efeito.</span><span class="sxs-lookup"><span data-stu-id="b759d-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="b759d-139">Quando os efeitos se sobrepõem no mesmo objeto, eles são aplicados em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b759d-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="b759d-140">O efeito de áudio de envelope de volume é uma exceção; consulte a referência de [efeito de envelope de volume](volume-envelope-effect.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b759d-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="b759d-141">Em uma composição, todas as faixas de áudio são misturadas antes que os efeitos de áudio para essa composição sejam aplicados.</span><span class="sxs-lookup"><span data-stu-id="b759d-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="b759d-142">Como as transições não podem se sobrepor no mesmo objeto, elas não têm um valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b759d-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="b759d-143">O exemplo a seguir adiciona o objeto de transição a uma faixa:</span><span class="sxs-lookup"><span data-stu-id="b759d-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="b759d-144">O exemplo consulta o objeto Track para a interface [**IAMTimelineTransable**](iamtimelinetransable.md) antes de chamar addTrans.</span><span class="sxs-lookup"><span data-stu-id="b759d-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="b759d-145">**5. definir propriedades**</span><span class="sxs-lookup"><span data-stu-id="b759d-145">**5. Set Properties**</span></span>

<span data-ttu-id="b759d-146">Muitos efeitos e transições dão suporte a propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b759d-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="b759d-147">Para obter informações, consulte [definindo propriedades em efeitos e transições](setting-properties-on-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="b759d-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="b759d-148">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b759d-148">Example</span></span>

<span data-ttu-id="b759d-149">O exemplo de código a seguir adiciona uma [transição de apagamento SMPTE](smpte-wipe-transition.md) a uma faixa. Ele pressupõe que o objeto Track já existe na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="b759d-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="b759d-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b759d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b759d-151">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="b759d-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



