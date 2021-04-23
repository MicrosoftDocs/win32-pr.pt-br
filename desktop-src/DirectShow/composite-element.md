---
description: O elemento composto define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908834"
---
# <a name="composite-element"></a><span data-ttu-id="d9f22-103">Elemento composto</span><span class="sxs-lookup"><span data-stu-id="d9f22-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="d9f22-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d9f22-104">\[Deprecated.</span></span> <span data-ttu-id="d9f22-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9f22-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9f22-106">O `composite` elemento define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.</span><span class="sxs-lookup"><span data-stu-id="d9f22-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="d9f22-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9f22-107">Attributes</span></span>

<span data-ttu-id="d9f22-108">[**Lock**](lock-attribute.md), [**mudo**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="d9f22-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="d9f22-109">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="d9f22-109">Parent/Child Information</span></span>



| <span data-ttu-id="d9f22-110">Label</span><span class="sxs-lookup"><span data-stu-id="d9f22-110">Label</span></span> | <span data-ttu-id="d9f22-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d9f22-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f22-112">Pai</span><span class="sxs-lookup"><span data-stu-id="d9f22-112">Parent</span></span>   | <span data-ttu-id="d9f22-113">`composite`, [ **grupo**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="d9f22-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="d9f22-114">Children</span><span class="sxs-lookup"><span data-stu-id="d9f22-114">Children</span></span> | <span data-ttu-id="d9f22-115">`composite`, [**efeito**](effect-element.md), [**controle**](track-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="d9f22-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d9f22-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9f22-116">Remarks</span></span>

<span data-ttu-id="d9f22-117">Dentro de um `composite` elemento, a prioridade de camadas aninhadas é determinada implicitamente pela ordem em que aparecem dentro do elemento.</span><span class="sxs-lookup"><span data-stu-id="d9f22-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="d9f22-118">A primeira camada tem a prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.</span><span class="sxs-lookup"><span data-stu-id="d9f22-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="d9f22-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d9f22-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="d9f22-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9f22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f22-121">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="d9f22-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



