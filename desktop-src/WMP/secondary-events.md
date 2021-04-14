---
title: Eventos secundários
description: Eventos secundários
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Capas do Windows Media Player, eventos secundários
- capas, eventos secundários
- eventos, secundários
- escrevendo código para capas, eventos secundários
- eventos secundários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453684"
---
# <a name="secondary-events"></a><span data-ttu-id="beeca-108">Eventos secundários</span><span class="sxs-lookup"><span data-stu-id="beeca-108">Secondary Events</span></span>

<span data-ttu-id="beeca-109">Você pode determinar quais outros eventos estão ocorrendo quando um evento específico é disparado.</span><span class="sxs-lookup"><span data-stu-id="beeca-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="beeca-110">Por exemplo, quando um botão do mouse é clicado, talvez você queira saber se a tecla ALT estava inativa ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="beeca-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="beeca-111">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="beeca-111">Event Attributes</span></span>

<span data-ttu-id="beeca-112">Os seguintes atributos de evento têm suporte para capas:</span><span class="sxs-lookup"><span data-stu-id="beeca-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="beeca-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="beeca-113">**altKey**</span></span>
-   <span data-ttu-id="beeca-114">**Button**</span><span class="sxs-lookup"><span data-stu-id="beeca-114">**button**</span></span>
-   <span data-ttu-id="beeca-115">**clientX**</span><span class="sxs-lookup"><span data-stu-id="beeca-115">**clientX**</span></span>
-   <span data-ttu-id="beeca-116">**cliente**</span><span class="sxs-lookup"><span data-stu-id="beeca-116">**clientY**</span></span>
-   <span data-ttu-id="beeca-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="beeca-117">**ctrlKey**</span></span>
-   <span data-ttu-id="beeca-118">**deelement**</span><span class="sxs-lookup"><span data-stu-id="beeca-118">**fromElement**</span></span>
-   <span data-ttu-id="beeca-119">**offsetX**</span><span class="sxs-lookup"><span data-stu-id="beeca-119">**offsetX**</span></span>
-   <span data-ttu-id="beeca-120">**offsetY**</span><span class="sxs-lookup"><span data-stu-id="beeca-120">**offsetY**</span></span>
-   <span data-ttu-id="beeca-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="beeca-121">**screenX**</span></span>
-   <span data-ttu-id="beeca-122">**tela**</span><span class="sxs-lookup"><span data-stu-id="beeca-122">**screenY**</span></span>
-   <span data-ttu-id="beeca-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="beeca-123">**shiftKey**</span></span>
-   <span data-ttu-id="beeca-124">**srcElement**</span><span class="sxs-lookup"><span data-stu-id="beeca-124">**srcElement**</span></span>
-   <span data-ttu-id="beeca-125">**elemento**</span><span class="sxs-lookup"><span data-stu-id="beeca-125">**toElement**</span></span>
-   <span data-ttu-id="beeca-126">**x**</span><span class="sxs-lookup"><span data-stu-id="beeca-126">**x**</span></span>
-   <span data-ttu-id="beeca-127">**y**</span><span class="sxs-lookup"><span data-stu-id="beeca-127">**y**</span></span>
-   <span data-ttu-id="beeca-128">**KeyCode**</span><span class="sxs-lookup"><span data-stu-id="beeca-128">**keyCode**</span></span>

<span data-ttu-id="beeca-129">Para obter mais informações sobre esses atributos, consulte a [referência de programação de capa](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="beeca-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="beeca-130">Usando eventos secundários</span><span class="sxs-lookup"><span data-stu-id="beeca-130">Using Secondary Events</span></span>

<span data-ttu-id="beeca-131">Você só pode processar atributos de evento no código JScript.</span><span class="sxs-lookup"><span data-stu-id="beeca-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="beeca-132">Você deve usar a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="beeca-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="beeca-133">*eventattributename* é o nome do atributo de evento.</span><span class="sxs-lookup"><span data-stu-id="beeca-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="beeca-134">Por exemplo, para determinar se a tecla ALT foi pressionada durante um evento de clique, você pode usar as seguintes linhas em seu código JScript:</span><span class="sxs-lookup"><span data-stu-id="beeca-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="beeca-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beeca-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beeca-136">**Manipulando eventos**</span><span class="sxs-lookup"><span data-stu-id="beeca-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




