---
description: O atributo de início especifica a hora de início de um objeto, em relação ao objeto pai.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Atributo de início
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787133"
---
# <a name="start-attribute"></a><span data-ttu-id="c3bc4-103">Atributo de início</span><span class="sxs-lookup"><span data-stu-id="c3bc4-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="c3bc4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-104">\[Deprecated.</span></span> <span data-ttu-id="c3bc4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3bc4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c3bc4-106">O `start` atributo especifica a hora de início de um objeto, em relação ao objeto pai.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="c3bc4-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c3bc4-107">Possible Values</span></span>

<span data-ttu-id="c3bc4-108">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="c3bc4-109">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="c3bc4-110">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-110">Leading units can be omitted.</span></span> <span data-ttu-id="c3bc4-111">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="c3bc4-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3bc4-112">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="c3bc4-112">Applies To</span></span>

<span data-ttu-id="c3bc4-113">[**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="c3bc4-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="c3bc4-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3bc4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bc4-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="c3bc4-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3bc4-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="c3bc4-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



