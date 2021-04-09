---
description: O atributo mudo especifica o estado de mudo do objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Atributo mudo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087732"
---
# <a name="mute-attribute"></a><span data-ttu-id="14d31-103">Atributo mudo</span><span class="sxs-lookup"><span data-stu-id="14d31-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="14d31-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="14d31-104">\[Deprecated.</span></span> <span data-ttu-id="14d31-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14d31-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="14d31-106">O `mute` atributo especifica o estado de mudo do objeto.</span><span class="sxs-lookup"><span data-stu-id="14d31-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="14d31-107">Se o valor for **true**, nem o objeto nem seus filhos serão renderizados.</span><span class="sxs-lookup"><span data-stu-id="14d31-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="14d31-108">Se o valor for **false**, o objeto será renderizado e seus filhos serão renderizados de acordo com seu próprio estado de mudo.</span><span class="sxs-lookup"><span data-stu-id="14d31-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="14d31-109">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="14d31-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="14d31-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="14d31-110">Possible Values</span></span>

<span data-ttu-id="14d31-111">Os valores a seguir são definidos como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="14d31-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="14d31-112">Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="14d31-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="14d31-113">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="14d31-113">Applies To</span></span>

<span data-ttu-id="14d31-114">[**clip**](clip-element.md), [**composto**](composite-element.md), [**efeito**](effect-element.md), [**grupo**](group-element.md), [**linha do tempo**](timeline-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="14d31-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="14d31-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="14d31-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d31-116">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="14d31-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="14d31-117">**IAMTimelineObj:: setmudod**</span><span class="sxs-lookup"><span data-stu-id="14d31-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



