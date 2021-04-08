---
description: O atributo mLength especifica a duração de um arquivo de origem. Esse valor deve ser a duração real ou erros de renderização podem ocorrer.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mLength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919677"
---
# <a name="mlength-attribute"></a><span data-ttu-id="2a17e-104">Atributo mLength</span><span class="sxs-lookup"><span data-stu-id="2a17e-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="2a17e-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2a17e-105">\[Deprecated.</span></span> <span data-ttu-id="2a17e-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a17e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2a17e-107">O `mlength` atributo especifica a duração de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="2a17e-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="2a17e-108">Esse valor deve ser a duração real ou erros de renderização podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="2a17e-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2a17e-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="2a17e-109">Applies To</span></span>

[<span data-ttu-id="2a17e-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="2a17e-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="2a17e-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2a17e-111">Possible Values</span></span>

<span data-ttu-id="2a17e-112">Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos.</span><span class="sxs-lookup"><span data-stu-id="2a17e-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="2a17e-113">Exemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="2a17e-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="2a17e-114">As unidades à esquerda podem ser omitidas.</span><span class="sxs-lookup"><span data-stu-id="2a17e-114">Leading units can be omitted.</span></span> <span data-ttu-id="2a17e-115">Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.</span><span class="sxs-lookup"><span data-stu-id="2a17e-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a17e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a17e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a17e-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="2a17e-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="2a17e-118">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="2a17e-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



