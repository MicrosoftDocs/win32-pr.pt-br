---
description: O elemento linear define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760701"
---
# <a name="linear-element"></a><span data-ttu-id="2e637-103">Elemento linear</span><span class="sxs-lookup"><span data-stu-id="2e637-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="2e637-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2e637-104">\[Deprecated.</span></span> <span data-ttu-id="2e637-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e637-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e637-106">O elemento linear define o valor de um elemento [**param**](param-element.md) em um momento específico, em relação ao início da transição ou efeito que contém o elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="2e637-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="2e637-107">O `linear` elemento faz com que o parâmetro faça uma transição suave de seu valor anterior para o novo valor.</span><span class="sxs-lookup"><span data-stu-id="2e637-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="2e637-108">Para um salto instantâneo para um novo valor, use o elemento [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2e637-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="2e637-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e637-109">Attributes</span></span>

<span data-ttu-id="2e637-110">[**tempo**](time-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="2e637-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="2e637-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="2e637-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="2e637-112">Pai</span><span class="sxs-lookup"><span data-stu-id="2e637-112">Parent</span></span>   | [<span data-ttu-id="2e637-113">**param**</span><span class="sxs-lookup"><span data-stu-id="2e637-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="2e637-114">Children</span><span class="sxs-lookup"><span data-stu-id="2e637-114">Children</span></span> | <span data-ttu-id="2e637-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2e637-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="2e637-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e637-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="2e637-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e637-117">Requirements</span></span>



| <span data-ttu-id="2e637-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e637-118">Requirement</span></span> | <span data-ttu-id="2e637-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2e637-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e637-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e637-120">Header</span></span><br/> | <dl> <span data-ttu-id="2e637-121"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e637-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e637-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e637-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e637-123">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="2e637-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




