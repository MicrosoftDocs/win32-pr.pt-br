---
description: O atributo time especifica a hora em que um parâmetro assume um novo valor, em relação ao início da transição ou efeito.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Atributo de tempo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172189"
---
# <a name="time-attribute"></a><span data-ttu-id="b3c3b-103">Atributo de tempo</span><span class="sxs-lookup"><span data-stu-id="b3c3b-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="b3c3b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-104">\[Deprecated.</span></span> <span data-ttu-id="b3c3b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3c3b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b3c3b-106">O `time` atributo especifica a hora em que um parâmetro assume um novo valor, em relação ao início da transição ou efeito.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="b3c3b-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b3c3b-107">Possible Values</span></span>

<span data-ttu-id="b3c3b-108">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="b3c3b-109">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="b3c3b-110">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-110">Leading units can be omitted.</span></span> <span data-ttu-id="b3c3b-111">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="b3c3b-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b3c3b-112">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="b3c3b-112">Applies To</span></span>

<span data-ttu-id="b3c3b-113">[**em**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="b3c3b-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="b3c3b-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3c3b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c3b-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="b3c3b-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



