---
description: O atributo PreviewMode especifica o modo de visualização para o grupo. Se o valor for TRUE, os quadros poderão ser removidos durante a visualização. Caso contrário, nenhum quadro será removido durante a visualização. O valor padrão é TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Atributo PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370191"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="2d21a-106">Atributo PreviewMode</span><span class="sxs-lookup"><span data-stu-id="2d21a-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="2d21a-107">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2d21a-107">\[Deprecated.</span></span> <span data-ttu-id="2d21a-108">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d21a-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d21a-109">O `previewmode` atributo especifica o modo de visualização para o grupo.</span><span class="sxs-lookup"><span data-stu-id="2d21a-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="2d21a-110">Se o valor for **true**, os quadros poderão ser removidos durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="2d21a-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="2d21a-111">Caso contrário, nenhum quadro será removido durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="2d21a-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="2d21a-112">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="2d21a-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="2d21a-113">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2d21a-113">Possible Values</span></span>

<span data-ttu-id="2d21a-114">Os valores a seguir são definidos como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="2d21a-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="2d21a-115">Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2d21a-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2d21a-116">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="2d21a-116">Applies To</span></span>

[<span data-ttu-id="2d21a-117">**Group**</span><span class="sxs-lookup"><span data-stu-id="2d21a-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="2d21a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d21a-118">Remarks</span></span>

<span data-ttu-id="2d21a-119">Na configuração padrão, os quadros são descartados durante a visualização de efeitos ou transições lentas, para manter o vídeo sincronizado com o áudio.</span><span class="sxs-lookup"><span data-stu-id="2d21a-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="2d21a-120">O vídeo pode parecer instável como resultado.</span><span class="sxs-lookup"><span data-stu-id="2d21a-120">The video might look choppy as a result.</span></span> <span data-ttu-id="2d21a-121">Definir esse atributo como **false** força cada quadro a ser renderizado durante a visualização, possivelmente resultando no vídeo ficando fora de sincronia com o áudio.</span><span class="sxs-lookup"><span data-stu-id="2d21a-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="2d21a-122">Os quadros nunca são descartados durante a gravação em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d21a-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d21a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d21a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d21a-124">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="2d21a-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="2d21a-125">**IAMTimelineGroup:: SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="2d21a-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



