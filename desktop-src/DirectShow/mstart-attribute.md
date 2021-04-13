---
description: O atributo mStart especifica a hora de início de um clipe, em relação ao arquivo de mídia original.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Atributo mStart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456384"
---
# <a name="mstart-attribute"></a><span data-ttu-id="9f398-103">Atributo mStart</span><span class="sxs-lookup"><span data-stu-id="9f398-103">mstart Attribute</span></span>

> [!Note]  
> <span data-ttu-id="9f398-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9f398-104">\[Deprecated.</span></span> <span data-ttu-id="9f398-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f398-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f398-106">O `mstart` atributo especifica a hora de início de um clipe, em relação ao arquivo de mídia original.</span><span class="sxs-lookup"><span data-stu-id="9f398-106">The `mstart` attribute specifies the start time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9f398-107">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="9f398-107">Applies To</span></span>

[<span data-ttu-id="9f398-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="9f398-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="9f398-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9f398-109">Possible Values</span></span>

<span data-ttu-id="9f398-110">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="9f398-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="9f398-111">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="9f398-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="9f398-112">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="9f398-112">Leading units can be omitted.</span></span> <span data-ttu-id="9f398-113">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="9f398-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f398-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f398-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f398-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="9f398-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="9f398-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="9f398-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



