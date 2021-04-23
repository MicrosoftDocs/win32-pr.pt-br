---
description: O elemento at define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: no elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909824"
---
# <a name="at-element"></a><span data-ttu-id="346cf-103">no elemento</span><span class="sxs-lookup"><span data-stu-id="346cf-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="346cf-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="346cf-104">\[Deprecated.</span></span> <span data-ttu-id="346cf-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="346cf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="346cf-106">O `at` elemento define o valor de um elemento [**param**](param-element.md) em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="346cf-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="346cf-107">O `at` elemento faz com que o parâmetro salte abruptamente para o novo valor no momento determinado.</span><span class="sxs-lookup"><span data-stu-id="346cf-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="346cf-108">Para uma progressão suave para um novo valor, use o elemento [**linear**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="346cf-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="346cf-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="346cf-109">Attributes</span></span>

<span data-ttu-id="346cf-110">[**tempo**](time-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="346cf-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="346cf-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="346cf-111">Parent/Child Information</span></span>



| <span data-ttu-id="346cf-112">Label</span><span class="sxs-lookup"><span data-stu-id="346cf-112">Label</span></span> | <span data-ttu-id="346cf-113">Valor</span><span class="sxs-lookup"><span data-stu-id="346cf-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="346cf-114">Pai</span><span class="sxs-lookup"><span data-stu-id="346cf-114">Parent</span></span>   | [<span data-ttu-id="346cf-115">**param**</span><span class="sxs-lookup"><span data-stu-id="346cf-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="346cf-116">Children</span><span class="sxs-lookup"><span data-stu-id="346cf-116">Children</span></span> | <span data-ttu-id="346cf-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="346cf-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="346cf-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="346cf-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="346cf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="346cf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346cf-120">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="346cf-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



