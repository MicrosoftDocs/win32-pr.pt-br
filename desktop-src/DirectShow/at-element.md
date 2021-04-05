---
description: O elemento at define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: no elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646090"
---
# <a name="at-element"></a><span data-ttu-id="e4d64-103">no elemento</span><span class="sxs-lookup"><span data-stu-id="e4d64-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="e4d64-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e4d64-104">\[Deprecated.</span></span> <span data-ttu-id="e4d64-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4d64-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e4d64-106">O `at` elemento define o valor de um elemento [**param**](param-element.md) em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e4d64-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="e4d64-107">O `at` elemento faz com que o parâmetro salte abruptamente para o novo valor no momento determinado.</span><span class="sxs-lookup"><span data-stu-id="e4d64-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="e4d64-108">Para uma progressão suave para um novo valor, use o elemento [**linear**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e4d64-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="e4d64-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="e4d64-109">Attributes</span></span>

<span data-ttu-id="e4d64-110">[**tempo**](time-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="e4d64-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="e4d64-111">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="e4d64-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="e4d64-112">Pai</span><span class="sxs-lookup"><span data-stu-id="e4d64-112">Parent</span></span>   | [<span data-ttu-id="e4d64-113">**param**</span><span class="sxs-lookup"><span data-stu-id="e4d64-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="e4d64-114">Children</span><span class="sxs-lookup"><span data-stu-id="e4d64-114">Children</span></span> | <span data-ttu-id="e4d64-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e4d64-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="e4d64-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4d64-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="e4d64-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4d64-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d64-118">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="e4d64-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



