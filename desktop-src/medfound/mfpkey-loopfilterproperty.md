---
description: Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Propriedade MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810720"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="850fc-103">\_Propriedade MFPKEY LOOPFILTER</span><span class="sxs-lookup"><span data-stu-id="850fc-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="850fc-104">Especifica se o codec deve usar o filtro de desbloqueio no loop durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="850fc-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="850fc-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="850fc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="850fc-106">g \_ wszWMVCLoopFilter</span><span class="sxs-lookup"><span data-stu-id="850fc-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="850fc-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="850fc-107">Data Type</span></span>

<span data-ttu-id="850fc-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="850fc-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="850fc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="850fc-109">Remarks</span></span>

<span data-ttu-id="850fc-110">O filtro em loop é um método de debloqueio que é aplicado durante a codificação e decodificação, para reduzir os artefatos de bloqueio no tempo de codificação ("no loop") para que os quadros P e B futuros não os carreguem.</span><span class="sxs-lookup"><span data-stu-id="850fc-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="850fc-111">O efeito de aplicar o filtro em loop é que as bordas dos blocos de macro nos quadros de vídeo de saída são menos perceptíveis.</span><span class="sxs-lookup"><span data-stu-id="850fc-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="850fc-112">Ao mesmo tempo, a imagem pode se tornar mais suave na aparência.</span><span class="sxs-lookup"><span data-stu-id="850fc-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="850fc-113">Embora o filtro em loop possa levar a uma redução nos detalhes da imagem em alguns quadros, a qualidade geral do vídeo terá um benefício perceptível.</span><span class="sxs-lookup"><span data-stu-id="850fc-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="850fc-114">A maior desvantagem de usar a filtragem no loop é o custo adicional de decodificação de desempenho.</span><span class="sxs-lookup"><span data-stu-id="850fc-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="850fc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="850fc-115">Requirements</span></span>



| <span data-ttu-id="850fc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="850fc-116">Requirement</span></span> | <span data-ttu-id="850fc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="850fc-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="850fc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="850fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="850fc-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="850fc-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="850fc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="850fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="850fc-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="850fc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="850fc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="850fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="850fc-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="850fc-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="850fc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="850fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850fc-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="850fc-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




