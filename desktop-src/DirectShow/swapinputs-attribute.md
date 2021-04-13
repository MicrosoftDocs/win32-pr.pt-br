---
description: O atributo swapinputs especifica se as entradas de transição devem ser trocadas. Se o valor for TRUE, as entradas serão trocadas. O valor padrão é FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Atributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297462"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="9f2f6-105">Atributo swapinputs</span><span class="sxs-lookup"><span data-stu-id="9f2f6-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="9f2f6-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-106">\[Deprecated.</span></span> <span data-ttu-id="9f2f6-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f2f6-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f2f6-108">O `swapinputs` atributo especifica se as entradas de transição devem ser trocadas.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="9f2f6-109">Se o valor for **true**, as entradas serão trocadas.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="9f2f6-110">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="9f2f6-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9f2f6-111">Possible Values</span></span>

<span data-ttu-id="9f2f6-112">Os valores a seguir são definidos como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="9f2f6-113">Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9f2f6-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9f2f6-114">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="9f2f6-114">Applies To</span></span>

[<span data-ttu-id="9f2f6-115">**transição**</span><span class="sxs-lookup"><span data-stu-id="9f2f6-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="9f2f6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f2f6-116">Remarks</span></span>

<span data-ttu-id="9f2f6-117">Por padrão, uma transição prossegue da composição de todas as camadas de prioridade inferior para a camada na qual reside a transição.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="9f2f6-118">Se o `swapinputs` atributo for 1, essa direção será invertida.</span><span class="sxs-lookup"><span data-stu-id="9f2f6-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="9f2f6-119">Para obter mais informações sobre o modelo de camadas usado pelo DES, consulte [o modelo de linha do tempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="9f2f6-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9f2f6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f2f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2f6-121">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="9f2f6-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="9f2f6-122">**IAMTimelineTrans::SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="9f2f6-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



