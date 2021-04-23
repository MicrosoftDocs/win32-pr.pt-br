---
description: O elemento Transition define um objeto de transição. Uma transição é uma transformação de duas entradas que resulta em uma transição de um fluxo (como uma composição ou faixa) para outra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento Transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910034"
---
# <a name="transition-element"></a><span data-ttu-id="6d1e9-104">Elemento Transition</span><span class="sxs-lookup"><span data-stu-id="6d1e9-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="6d1e9-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-105">\[Deprecated.</span></span> <span data-ttu-id="6d1e9-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d1e9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d1e9-107">O `transition` elemento define um objeto de transição.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="6d1e9-108">Uma transição é uma transformação de duas entradas que resulta em uma transição de um fluxo (como uma composição ou faixa) para outra.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="6d1e9-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d1e9-109">Attributes</span></span>

<span data-ttu-id="6d1e9-110">[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**mudo**](mute-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="6d1e9-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="6d1e9-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="6d1e9-111">Parent/Child Information</span></span>



| <span data-ttu-id="6d1e9-112">Label</span><span class="sxs-lookup"><span data-stu-id="6d1e9-112">Label</span></span> | <span data-ttu-id="6d1e9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6d1e9-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="6d1e9-114">Pai</span><span class="sxs-lookup"><span data-stu-id="6d1e9-114">Parent</span></span>   | <span data-ttu-id="6d1e9-115">[**composto**](composite-element.md), [ **faixa**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="6d1e9-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="6d1e9-116">Children</span><span class="sxs-lookup"><span data-stu-id="6d1e9-116">Children</span></span> | [<span data-ttu-id="6d1e9-117">**param**</span><span class="sxs-lookup"><span data-stu-id="6d1e9-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="6d1e9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d1e9-118">Remarks</span></span>

<span data-ttu-id="6d1e9-119">O atributo **CLSID** especifica o subobjeto que cria a transição.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="6d1e9-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d1e9-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="6d1e9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d1e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1e9-122">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="6d1e9-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



