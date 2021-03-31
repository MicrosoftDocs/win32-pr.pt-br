---
description: O atributo de taxa de quadros especifica uma taxa de quadros, em quadros por segundo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Atributo de taxa de quadros (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919885"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="0dfef-103">Atributo de taxa de quadros (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="0dfef-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="0dfef-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0dfef-104">\[Deprecated.</span></span> <span data-ttu-id="0dfef-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0dfef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0dfef-106">O `framerate` atributo especifica uma taxa de quadros, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="0dfef-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="0dfef-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0dfef-107">Possible Values</span></span>

<span data-ttu-id="0dfef-108">Valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="0dfef-108">Floating-point value.</span></span> <span data-ttu-id="0dfef-109">O valor deve incluir o zero à esquerda antes da casa decimal.</span><span class="sxs-lookup"><span data-stu-id="0dfef-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="0dfef-110">Por exemplo, 0,3, não. 3.</span><span class="sxs-lookup"><span data-stu-id="0dfef-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="0dfef-111">Não use mais de sete dígitos decimais.</span><span class="sxs-lookup"><span data-stu-id="0dfef-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0dfef-112">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="0dfef-112">Applies To</span></span>

<span data-ttu-id="0dfef-113">[**clip**](clip-element.md), [**grupo**](group-element.md), [**linha do tempo**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="0dfef-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dfef-114">Remarks</span></span>

<span data-ttu-id="0dfef-115">Para o elemento **clip** , esse atributo especifica a taxa de quadros padrão da origem.</span><span class="sxs-lookup"><span data-stu-id="0dfef-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="0dfef-116">Especifique o atributo para imagens que ainda andDIB sequências.</span><span class="sxs-lookup"><span data-stu-id="0dfef-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="0dfef-117">Para uma imagem ainda, defina o valor como zero.</span><span class="sxs-lookup"><span data-stu-id="0dfef-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="0dfef-118">Para uma sequência DIB, use um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0dfef-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="0dfef-119">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="0dfef-119">The default value is zero.</span></span>

<span data-ttu-id="0dfef-120">Para o elemento **Group** , esse atributo especifica a taxa de quadros de saída para o grupo.</span><span class="sxs-lookup"><span data-stu-id="0dfef-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="0dfef-121">Para o elemento **Timeline** , esse atributo especifica a taxa de quadros padrão para todos os grupos.</span><span class="sxs-lookup"><span data-stu-id="0dfef-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dfef-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0dfef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dfef-123">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="0dfef-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="0dfef-124">**IAMTimelineSrc::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="0dfef-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="0dfef-125">**IAMTimelineGroup::SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="0dfef-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="0dfef-126">**IAMTimeline::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="0dfef-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



