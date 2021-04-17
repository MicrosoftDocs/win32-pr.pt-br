---
description: O atributo Stop especifica a hora de parada de um objeto, em relação ao objeto pai.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: parar atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761749"
---
# <a name="stop-attribute"></a><span data-ttu-id="6d5e8-103">parar atributo</span><span class="sxs-lookup"><span data-stu-id="6d5e8-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="6d5e8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-104">\[Deprecated.</span></span> <span data-ttu-id="6d5e8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d5e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d5e8-106">O `stop` atributo especifica a hora de parada de um objeto, em relação ao objeto pai.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="6d5e8-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6d5e8-107">Possible Values</span></span>

<span data-ttu-id="6d5e8-108">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="6d5e8-109">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="6d5e8-110">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-110">Leading units can be omitted.</span></span> <span data-ttu-id="6d5e8-111">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="6d5e8-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6d5e8-112">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="6d5e8-112">Applies To</span></span>

<span data-ttu-id="6d5e8-113">[**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="6d5e8-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="6d5e8-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d5e8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5e8-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="6d5e8-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d5e8-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="6d5e8-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



