---
description: O atributo cutpoint especifica quando uma transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. O valor é relativo ao início da transição.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Atributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087631"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="45561-104">Atributo cutpoint</span><span class="sxs-lookup"><span data-stu-id="45561-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="45561-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="45561-105">\[Deprecated.</span></span> <span data-ttu-id="45561-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45561-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="45561-107">O `cutpoint` atributo especifica quando uma transição corta de uma origem para a próxima, se a transição for renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="45561-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="45561-108">O valor é relativo ao início da transição.</span><span class="sxs-lookup"><span data-stu-id="45561-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="45561-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="45561-109">Possible Values</span></span>

<span data-ttu-id="45561-110">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="45561-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="45561-111">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="45561-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="45561-112">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="45561-112">Leading units can be omitted.</span></span> <span data-ttu-id="45561-113">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="45561-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="45561-114">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="45561-114">Applies To</span></span>

[<span data-ttu-id="45561-115">**transição**</span><span class="sxs-lookup"><span data-stu-id="45561-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="45561-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="45561-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45561-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="45561-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="45561-118">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="45561-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



