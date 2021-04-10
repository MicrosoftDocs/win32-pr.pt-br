---
description: O atributo mstop especifica a hora de parada de um clipe, em relação ao arquivo de mídia original.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Atributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087255"
---
# <a name="mstop-attribute"></a><span data-ttu-id="0d653-103">Atributo mstop</span><span class="sxs-lookup"><span data-stu-id="0d653-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="0d653-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0d653-104">\[Deprecated.</span></span> <span data-ttu-id="0d653-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d653-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d653-106">O `mstop` atributo especifica a hora de parada de um clipe, em relação ao arquivo de mídia original.</span><span class="sxs-lookup"><span data-stu-id="0d653-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0d653-107">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="0d653-107">Applies To</span></span>

[<span data-ttu-id="0d653-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="0d653-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="0d653-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0d653-109">Possible Values</span></span>

<span data-ttu-id="0d653-110">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="0d653-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="0d653-111">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="0d653-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="0d653-112">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="0d653-112">Leading units can be omitted.</span></span> <span data-ttu-id="0d653-113">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="0d653-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d653-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d653-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d653-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="0d653-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d653-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="0d653-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



