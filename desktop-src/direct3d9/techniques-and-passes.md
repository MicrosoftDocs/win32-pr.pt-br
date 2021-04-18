---
description: As técnicas fornecem o capacidade de renderização. Uma técnica encapsula o estado de efeito que determina um estilo de renderização. Uma técnica é composta de uma ou mais passagens.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas e passagens (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760111"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="df33b-105">Técnicas e passagens (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="df33b-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="df33b-106">As técnicas fornecem o capacidade de renderização.</span><span class="sxs-lookup"><span data-stu-id="df33b-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="df33b-107">Uma técnica encapsula o estado de efeito que determina um estilo de renderização.</span><span class="sxs-lookup"><span data-stu-id="df33b-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="df33b-108">Uma técnica é composta de uma ou mais passagens.</span><span class="sxs-lookup"><span data-stu-id="df33b-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="df33b-109">Técnicas</span><span class="sxs-lookup"><span data-stu-id="df33b-109">Techniques</span></span>

<span data-ttu-id="df33b-110">A sintaxe para chamar uma técnica é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="df33b-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="df33b-111">Em que:</span><span class="sxs-lookup"><span data-stu-id="df33b-111">Where:</span></span>

-   <span data-ttu-id="df33b-112">ID é um nome exclusivo opcional.</span><span class="sxs-lookup"><span data-stu-id="df33b-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="df33b-113">a anotação é zero ou mais partes opcionais de informações específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="df33b-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="df33b-114">Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="df33b-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="df33b-115">as Pass (es) são zero ou mais passagens.</span><span class="sxs-lookup"><span data-stu-id="df33b-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="df33b-116">Cada passagem contém atribuições de estado.</span><span class="sxs-lookup"><span data-stu-id="df33b-116">Each pass contains state assignments.</span></span> <span data-ttu-id="df33b-117">Veja abaixo.</span><span class="sxs-lookup"><span data-stu-id="df33b-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="df33b-118">Passa</span><span class="sxs-lookup"><span data-stu-id="df33b-118">Passes</span></span>

<span data-ttu-id="df33b-119">Uma passagem contém as atribuições de estado necessárias para renderizar.</span><span class="sxs-lookup"><span data-stu-id="df33b-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="df33b-120">Em que:</span><span class="sxs-lookup"><span data-stu-id="df33b-120">Where:</span></span>

-   <span data-ttu-id="df33b-121">ID é um nome exclusivo opcional.</span><span class="sxs-lookup"><span data-stu-id="df33b-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="df33b-122">a anotação é uma ou mais informações adicionais específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="df33b-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="df33b-123">Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="df33b-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="df33b-124">a atribuição (ões) atribui zero ou mais valores de estado ou avalia uma ou mais expressões.</span><span class="sxs-lookup"><span data-stu-id="df33b-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="df33b-125">Consulte [Estados de efeito (Direct3D 9)](effect-states.md) e [expressões (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="df33b-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="df33b-126">Passa ignorar tudo, exceto a última atribuição em um conjunto de atribuições repetidas para o mesmo estado.</span><span class="sxs-lookup"><span data-stu-id="df33b-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df33b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df33b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df33b-128">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="df33b-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



