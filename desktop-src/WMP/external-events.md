---
title: Eventos externos
description: Eventos externos
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Capas do Windows Media Player, eventos externos
- capas, eventos externos
- eventos, externos
- escrevendo código para capas, eventos externos
- eventos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810552"
---
# <a name="external-events"></a><span data-ttu-id="4659a-108">Eventos externos</span><span class="sxs-lookup"><span data-stu-id="4659a-108">External Events</span></span>

<span data-ttu-id="4659a-109">Quando os usuários clicam em um botão ou pressionam uma tecla, você pode responder à sua entrada com manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="4659a-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="4659a-110">Um manipulador de eventos é uma seção de código que é executada sempre que o evento é disparado.</span><span class="sxs-lookup"><span data-stu-id="4659a-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="4659a-111">Os seguintes eventos são suportados pelos elementos de capa:</span><span class="sxs-lookup"><span data-stu-id="4659a-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="4659a-112">**carga**</span><span class="sxs-lookup"><span data-stu-id="4659a-112">**load**</span></span>
-   <span data-ttu-id="4659a-113">**close**</span><span class="sxs-lookup"><span data-stu-id="4659a-113">**close**</span></span>
-   <span data-ttu-id="4659a-114">**alonga**</span><span class="sxs-lookup"><span data-stu-id="4659a-114">**resize**</span></span>
-   <span data-ttu-id="4659a-115">**tempo**</span><span class="sxs-lookup"><span data-stu-id="4659a-115">**timer**</span></span>
-   <span data-ttu-id="4659a-116">**Selecione**</span><span class="sxs-lookup"><span data-stu-id="4659a-116">**click**</span></span>
-   <span data-ttu-id="4659a-117">**DblClick**</span><span class="sxs-lookup"><span data-stu-id="4659a-117">**dblclick**</span></span>
-   <span data-ttu-id="4659a-118">**error**</span><span class="sxs-lookup"><span data-stu-id="4659a-118">**error**</span></span>
-   <span data-ttu-id="4659a-119">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="4659a-119">**mousedown**</span></span>
-   <span data-ttu-id="4659a-120">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="4659a-120">**mouseup**</span></span>
-   <span data-ttu-id="4659a-121">**ocorra**</span><span class="sxs-lookup"><span data-stu-id="4659a-121">**mousemove**</span></span>
-   <span data-ttu-id="4659a-122">**acima**</span><span class="sxs-lookup"><span data-stu-id="4659a-122">**mouseover**</span></span>
-   <span data-ttu-id="4659a-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="4659a-123">**mouseout**</span></span>
-   <span data-ttu-id="4659a-124">**pressionar**</span><span class="sxs-lookup"><span data-stu-id="4659a-124">**keypress**</span></span>
-   <span data-ttu-id="4659a-125">**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="4659a-125">**keydown**</span></span>
-   <span data-ttu-id="4659a-126">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="4659a-126">**keyup**</span></span>

<span data-ttu-id="4659a-127">Consulte a [referência de programação de capa](skin-programming-reference.md) para obter mais detalhes sobre eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="4659a-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="4659a-128">Um manipulador de eventos externos típico deve nomear o evento e definir o código que será executado.</span><span class="sxs-lookup"><span data-stu-id="4659a-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="4659a-129">Por exemplo, se você quiser criar código para iniciar o Windows Media Player quando o usuário clicar em um botão, você colocaria a linha a seguir em seu código de botão.</span><span class="sxs-lookup"><span data-stu-id="4659a-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="4659a-130">Isso irá reproduzir o arquivo chamado Laure. WMA.</span><span class="sxs-lookup"><span data-stu-id="4659a-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="4659a-131">Observe que você adiciona a palavra "on" a eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="4659a-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4659a-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4659a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4659a-133">**Manipulando eventos**</span><span class="sxs-lookup"><span data-stu-id="4659a-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




